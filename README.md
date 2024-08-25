Navigation system for visually impaired pedestrians 

Project Overview:

This project aims to create a navigation system tailored specifically for blind and visually impaired pedestrians. The system provides real-time walking directions based on the shortest path, taking into account current traffic conditions to ensure safe and efficient travel.

Key Features:

Real-Time Traffic Integration:

Utilizes the TomTom Traffic API to incorporate real-time traffic data into pedestrian route planning, helping users avoid congested or closed roads.
Shortest Path Calculation:

Uses OSMnx and NetworkX to calculate the shortest walking route between two points. The route is optimized for pedestrian paths.

Map Visualization:

Routes are visualized on an interactive map using Folium. Users can view the route, starting and ending points, and additional map details.
Audio Navigation Instructions:

Provides step-by-step audio navigation instructions to guide the user along the route. The instructions are generated dynamically based on the calculated route and traffic conditions.

Dynamic Routing Based on Traffic Data:

The system updates the pedestrian network with travel times influenced by real-time traffic data, ensuring that routes are dynamically adjusted for current conditions.
Project Components

Pedestrian Graph Extraction:

The pedestrian network of a specific area (e.g., Manhattan, New York) is extracted using OSMnx and converted into a format suitable for routing.

Traffic Data Integration:

Traffic data is fetched for a grid of latitude and longitude points across the target area using the TomTom Traffic API. This data is then spatially joined with the pedestrian network to adjust edge weights based on current traffic conditions.

Routing and Instructions:

The system calculates the shortest path using Dijkstra's algorithm and generates human-readable navigation instructions. These instructions are also converted to audio using the gTTS library.

Map Rendering:

The calculated route is plotted on an interactive Folium map, which is saved as an HTML file and can be viewed in any web browser.

Usage Instructions:

Install Dependencies:

Install the required Python libraries using pip:

!pip install osmnx pyttsx3 folium gtts

Set Up API Keys:

Replace 'your_api_key_here' in the code with your actual TomTom API key.

Run the Notebook:

Execute the Google Colab cell to calculate the route and generate navigation instructions.

View the Map:

The route is saved as an HTML file (route_map.html). Open this file in a web browser to view the map.

Listen to Instructions:

The navigation instructions are provided as an MP3 file, which can be played directly from the notebook or downloaded.

Future Enhancements:

Mobile App Integration:

Expanding the system to work within a mobile application for real-time pedestrian navigation.

Customizable Navigation Options:

Allow users to set preferences such as avoiding high-traffic areas or prioritizing certain types of routes (e.g., quieter streets, scenic paths).

Expanded Geographic Coverage:

Scaling the system to work in multiple cities and regions, with options to select specific areas dynamically.





