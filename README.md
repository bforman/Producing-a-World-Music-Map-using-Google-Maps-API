# Producing-a-World-Music-Map-using-Google-Maps-API
This repository provides an overview into how to approach producing a world map or perhaps a map of a portion of the world using the Google Maps Engine API for Python. This inquiry takes a look at an existing world music maps and expresses the limitations of the existing projects and how they might be improved. We will also incorporate how some of the aspects of existing projects can be used in our own version of the World Music Map. The process of installing the Python client library and obtaining a Google Maps Engine API key is covered as well. This project assumes that users already have a google mail account as it is required to sign onto the Google Developer's Console.

# Problem
We want to begin creating an effective and interactive world music map using the Google Maps Engine API for Python.
We are looking to form a World Music Map that will provide:
1. A world map layout
2. information about the origin of the music from different countries and territories/provinces within countries
3. possibly information about the individual artists or groups from different countries
4. the capability to listen to the music directly from the map

# Questions
1. What are the preliminary steps in getting the project up and running?
2. What Interactive World Music Maps already exist? (using Google Maps Engine API or not)
3. What are the some of the faults and limitations of the existing project(s) and how can they be improved?

# Resources
1. Getting started with Google Maps Engine API
  1. [Installing Google Maps Engine API Client Library for  Python](https://developers.google.com/api-client-library/python/apis/mapsengine/v1)
  2. [Obtaining an API key for the Google Maps Engine API](https://developers.google.com/api-client-library/python/guide/aaa_apikeys)

2. Existing World Music Map Projects
  1. [Tunemap](http://www.tunemap.net/)
  2. [Moran Ed World Music Map](http://www.moraneducation.com/world-music-map)
  3. [Spotify's "Music of the World" App(link)](http://www.spin.com/articles/spotify-map-music-of-the-world-app-playlists/)

3. Question 3 is an analysis question, and the answer will accompany the mini abstract for each given existing world music map project.

1.1. Mini abstract and Relevance of [Installing Google Maps Engine API Client Library for Python]
     This link provides a couple different means of getting the Google Maps Engine API Python Client Library installed. The Google Developer Console offers options for managed install (preffered), which has two sub-options for install, as well as a manual install which involves downloading a zip file and unzipping it via command line in your project directory.
     - For managed install (which might require running **sudo** first):
     - You can use the **pip** command:
        $ pip install --upgrade google-api-python-client
     Or you can go the **easy_install** route:
        $ easy_install --upgrade google-api-python-client
     For manual install you can visit the link, download the **latest client library for Python** and run the     following command at the command line:
        python setup.py install
     You must also install the App Engine which can be done by visiting the link and selecting the most current package from a list of downloads.
     This resource answers question 1: What are the preliminary steps in getting the project up and running?

1.2. Mini Abstract and Relevance of [Obtaining an API key for the Google Maps Engine API]
    Now that we've got all the essentials installed for getting the Google Maps Python Client Library set up, we need to obtain an API key before we can do anything using the Google Maps Engine API. [Obtaining an API key for the Google Maps Engine API] walks through step by step on how to obtain your distinct API key. 
    In shorthand you will: 
    * sign onto the Google Developer Console
    * create a new project
    * go to the credentials section
    * create a new key, being sure to select the appropriate type based on the criteria listed.
    * pass key to the build() function for use
    
More specific detail on that procedure is offered in the link.
This resource also answers question 1: What are the preliminary steps in getting the project up and running?

2.1 Mini Abstract and Analysis of [TuneMap]
Tunemap is a world music map that is powered by google maps api and is written in javascipt. The map is laid out nicely from a scaling standpoint. You can zoom all the way out to get an entire world view, or zoom in a little to get a hemisphere view, or even zoom all the way down into a country and view different counties/provinces. The creator of this map did an outstanding job of scaling the map so that no matter how far in or out the user is zoomed, the map looks just as sharp. Another thing the creator did well was the inclusion of a small overlay window which displays the current song being listened to, as well as information about: country, climate zone, list of artists, and even an artist density ratio. I found that to be an awesome piece to include as it provides specifics of the area. Tunemap features several different pinpoints that denote an area for which they have "native" music on log. The biggest downfall for this project is that none of the music actually plays! Now, it should be noted that the creator of this project denotes in the source code that it is no longer working because cloudmade (his host) no longer offers free plans, but it is still a shame that no music actually plays. Another limitation of this project is that it offers no real bio on the artists or information on the origins of the music displayed across the globe. Educational Information accompanying the music would be a great asset because the user would be able to not only become exposed to other music from countries around the world, but they would learn a thing or two about the culture of the people who created the piece theyre listening to. Another thing I noticed about Tunemap is that all of the countries are white, theres no color involved whatsoever, which could cause users to view the map as dull or unaesthetically pleasing. To improve on the above limitations I would a) make sure that the music actually plays! and b) come up with some sort of color grade to incorporate into the map and give it some life. With those limitations aside, the layout of this map is superb and offers as a good resource to tend to when beginning to think about how we want our world music map to be presented. This resource answers question 2: What Interactive World Music Maps already exist? (using Google Maps Engine API or not) & analysis provided answers question 3: What are the some of the faults and limitations of the existing project(s) and how can they be improved?

2.2 Mini Abstract and Analysis of [Moran Ed World Music Map]
This world music map took an interesting approach. In the user view there are two different interlaced windows, one that displays a region of the world blown up, and another smaller window in the bottom right corner of the main view that displays the entire world and allows the user to move a box from region to region to be blown up. This approach provides a different way for laying out the map which may be useful when making decisions on how our map should look. This map, unlike the Tunemap, provided a color scheme that assigned each country with a specific color (or no color at all). Although, there is not provided a good legend for the color grade which serves as a limitation of this map. For each country they only have one song to be played and you have to leave the page in order to listen to the piece, which also serves as a fault of this music map. It would be much more efficient to be able to play the piece directly from the map. One thing that the creator did an outstanding job on was providing the user with profound information about the music of that given area. The information provided included: most involved instruments, musical style, and a brief history of the music's origin. The aspect of including a color scale and the depth of information provided by this music map are concepts that I find appealing and will likely be used in our world music map. Aside from being able to play music from the map itself, I would improve the map by including a key that describes what each color used signifies. It would give the user a better grasp of what they are looking at. This map was not powered by Google Maps Engine API. This resource answers question 2: What Interactive World Music Maps already exist? (using Google Maps Engine API or not) & analysis provided answers question 3: What are the some of the faults and limitations of the existing project(s) and how can they be improved?

2.3 Mini Abstract and Analysis of [Spotify's "Music of the World" App(link)]
Spotify is no doubt one of, if not the largest music streaming services in the world. So of course they have their own version of the world music map. The "Music of the World" app is powered by the Google Maps Engine API as denoted by the Google logo in the bottom left corner or the view. The app uses the X5 Music Group, which is a plug-in that allows playlists, and albums to be accessed for over 220 countries, territories, and regions. As you take a look at the app you'll notice that the layout is very aesthetically pleasing. They used very vibrant colors and the black background makes those colors standout even more. Another interesting aspect of the app is the "album art", if you will, that they created and applied to given world music playlists. The idea of forming playlists is a nice aspect, but also serves as a limitation. Sure it would be nice to just listen to a playlist of music from different countries around the globe, and this may be a great feature to try and include in our own world map, but it takes away from the specifcality that we are aiming for. We want to be able to pinpoint specific places on the map where a certain cultures music originates, and provide a foundation of information about the music from that area. In a sense Spotifys' "Music of the World" is too broad of a representation for what we are looking for. Another limitation of Spotify's app is that likewise it does not offer the information about the music of given cultures like we wish to do. It does offer biographical notes pertaining to a specific song or artist, but not the music of a given culture in general. How we could improve that limitation is simply expand the information provided to encompass insight into the formation, and cultural origin of the music being presented. Aside from those limitations this app is amazingly built. It looks great, it runs smoothly, and provides a wide base of music to listen to. When planning the layout of our music map the use of vibrant colors will be strongly considered as I found that to be a strong point from an aesthetics view. This resource answers question 2: What Interactive World Music Maps already exist? (using Google Maps Engine API or not) & analysis provided answers question 3: What are the some of the faults and limitations of the existing project(s) and how can they be improved?

