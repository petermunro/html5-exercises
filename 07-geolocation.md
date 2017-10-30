# Geolocation

1. Load the page http://html5demos.com/geo/
2. In the console, explore the geolocation object:

        navigator.geolocation.getCurrentPosition(
        	pos => console.dir(pos),
        	() => console.log('error')
        );
