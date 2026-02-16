🌤️ SkyCast Weather Dashboard – Project Description


	Introduction
SkyCast is a modern, real-time weather dashboard built as part of the ALA-5 API Integration project. It provides users with up-to-date weather information for any city worldwide. The application features a sleek glass-morphism user interface with smooth animations and a fully responsive design that works seamlessly on all devices – from desktop monitors to mobile phones.
The primary goal of SkyCast is to demonstrate the integration of third-party APIs to fetch and display live weather data in an interactive and visually appealing manner. It showcases current weather conditions, hourly forecasts, and a 5 day extended forecast.
	2. Technology Stack
•	HTML5: Structure and semantic layout of the web page.
•	CSS3: Styling, including custom properties (CSS variables) for theme management, glass-morphism effects, responsive design, and keyframe animations.
•	JavaScript (ES6+): Dynamic functionality, API calls, DOM manipulation, and event handling.
•	OpenWeatherMap API: The core data source for all weather information.






	3. API Integration
The application uses the OpenWeatherMap API, a popular and comprehensive weather service. The following endpoints are utilized:
•	Geocoding API (/geo/1.0/direct): Converts a city name (e.g., "Bhavnagar, Gujarat") into precise geographical coordinates (latitude and longitude). It also provides the full location name including state and country.
•	Current Weather Data (/data/2.5/weather): Fetches real-time weather conditions for the given coordinates, including temperature, humidity, wind speed, pressure, and weather description.
•	5 Day / 3 Hour Forecast (/data/2.5/forecast): Retrieves weather predictions at 3 hour intervals for the next five days. This data is used to generate both the hourly forecast (next 24 hours) and the 5 day daily summary.
An API key (f5cb0b965ea1564c50c6f1b74534d823) is used to authenticate requests.
	4. Key Features
•	City Search: Users can enter any city name (with optional state and country) to get its weather. A debounced auto suggestion feature helps users find correct locations.
•	Default City: On first load, the dashboard displays weather for Bhavnagar, Gujarat, while the search bar remains empty for a clean user experience.
•	Current Weather Display:
o	City name with location details.
o	Large temperature reading with a descriptive icon (e.g., ☀️ for Clear).
o	"Feels like" temperature, humidity, wind speed, and atmospheric pressure.


•	Hourly Forecast:
o	The first card shows "Now" , using the exact current weather data to ensure consistency with the main display.
o	Seven additional cards show forecasts for the next 3 hour intervals (e.g., 3 PM, 6 PM, etc.).
•	5 Day Forecast:
o	Summarizes each day with an average temperature, dominant weather condition, and a representative icon.
o	Includes day names (e.g., Mon, Tue) for easy reference.
•	Theme Toggle: Users can switch between light and dark themes. The preference is saved in localStorage for persistence.
•	Responsive Design: The layout adapts gracefully to various screen sizes – from large desktops (1440px+) down to small mobile devices (320px).
•	Animated Background: Floating particles with subtle animations create a dynamic, engaging backdrop.
•	Informational Modals: Pop up windows provide details about the project, the development team, and the API integration.
	5. How It Works (User Flow)
1.	When the page loads, fetchWeather('Bhavnagar, Gujarat') is called.
2.	The Geocoding API converts "Bhavnagar, Gujarat" into coordinates.
3.	Using these coordinates, the Current Weather API and Forecast API are called simultaneously.
4.	The returned data populates all sections: current weather, hourly forecast (with a "Now" card), and 5 day forecast.
5.	If a user types in the search box, suggestions appear. Clicking a suggestion triggers a new weather search for that city.
6.	Clicking the "Get Weather" button or pressing Enter also performs a search.
7.	The theme toggle button switches between light and dark modes instantly.
	6. Visual Design Highlights
•	Glass-morphism: Semi transparent panels with backdrop filter blur, subtle borders, and box shadows.
•	Gradient Text: The main temperature and headings use CSS gradients for a vibrant look.
•	Smooth Animations: Elements fade and slide into view on load. Icons have floating animations. The theme toggle has a smooth sliding transition.
•	Custom Scrollbar: The horizontal hourly forecast container has a styled scrollbar that matches the theme color.
	Challenges & Fixes Applied
During development, several issues were identified and resolved:
•	Inconsistent Data: Initially, the "Now" temperature in the hourly forecast did not match the main temperature. This was fixed by creating the "Now" card using the current weather data instead of the forecast data.
•	Empty Search Bar Requirement: The user requested that the search bar be empty by default, even though Bhavnagar weather loads. This was achieved by setting cityInput.value = '' in the initialization while still calling fetchWeather with the default city.
•	Location Accuracy: For Indian cities like those in Gujarat, a country hint (&country=IN) was added to the Geocoding API request to prioritize results from India.
•	Full City Name Display: CSS word-break: break-word ensures long location names (including state and country) wrap correctly without overflowing.


	Conclusion
SkyCast successfully demonstrates a professional-grade API integration project. It combines functional weather fetching with a polished, user friendly interface. The application is not only a tool for checking the weather but also a showcase of modern web development techniques – including asynchronous JavaScript, responsive design, CSS animations, and theme management.
The project meets all specified requirements:
•	✅ Real-time weather data from OpenWeatherMap.
•	✅ Accurate location search with suggestions.
•	✅ Consistent data across current and forecast views.
•	✅ Default city (Bhavnagar) with empty search bar.
•	✅ Fully responsive and theme switchable.
•	✅ Clear documentation within the code (comments) and this description.
SkyCast is a robust, ready to deploy weather dashboard that can be easily extended with additional features like radar maps, air quality index, or multi language support in the future.
<img width="468" height="648" alt="image" src="https://github.com/user-attachments/assets/be23b1b3-626a-47cd-9cdc-67d7d4762601" />
