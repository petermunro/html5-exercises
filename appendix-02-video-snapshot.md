# Make a video snapshot tool

Here you will create an HTML page with a video element and a canvas element. The canvas element will be used to take a snapshot of the currently-playing video.

1. Start with your HTML page. Include in it:

``` html
<video src="big_buck_bunny.ogv" controls="controls" width="600"></video>
<canvas id="snapview" width="300" height="200"></canvas>
<button id="snapshot">Snap</button>
```

2. Now create your JavaScript:

    1. Create the button event handler:


            document.getElementById('snapshot').addEventListener('click'(event => {

            });

    2. Inside the event handler, declare variables for width and height:

            let width = 0;
            let height = 0;

    3. Get the canvas context. While we’re at it, we’ll get the video element too:

            let canvas = document.getElementById('snapview');
            let ctx = canvas.getContext('2d');

            let video = document.getElementsByTagName('video')[0];

    4. Set the width and height to half those of the video, and set the canvas dimensions too:

            width = video.videoWidth / 2;
            height = video.videoHeight / 2;
            canvas.width = width;
            canvas.height = height;

    5. Use `drawImage()` to draw the video element directly into the canvas:

            ctx.drawImage(video, 0, 0, width, height);


3. Play the video, and hit the ‘Snap’ button as it plays. The current video frame should be drawn into the canvas.
