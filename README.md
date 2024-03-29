PixelPuzzle
===========

Algorithms Meetup Pixel Puzzle Challenge!

There is a famous image hidden beneath the pixel-noise. Can you figure out what it is? 

Getting Started
===========
1. Install Node.js: 
http://nodejs.org/
2. use the terminal to make a directory and move into it:
```mkdir pixelPuzzle && cd pixelPuzzle ```
3. clone repository in this directory:
```git clone https://github.com/bgando/PixelPuzzle.git```
4. install dependencies:
```npm install```
5. run server:
```node app.js```
6. open page: http://localhost:3000/

Playing with the Code
===========
All the code you need to worry about is located inside the script tags in views/index.ejs 

Here is what it looks like:
```
    <script type="text/javascript">
      function imageLoaded(ev) {
        element = document.getElementById("canvas");
        c = element.getContext("2d");

        im = ev.target; // the image, assumed to be 200x200

        // read the width and height of the canvas
        width = element.width;
        height = element.height;

        // stamp the image on the left of the canvas:
        c.drawImage(im, 0, 0);

        // get all canvas pixel data
        imageData = c.getImageData(0, 0, width, height);

        // put pixel data on canvas
        c.putImageData(imageData, 0, 0);
      }

      im = new Image();
      im.onload = imageLoaded;
      im.src = "images/ironPuzzle.png"; // code assumes this image is 200x200
      //finished? try copperPuzzle.png!

    </script>
```
Resource
===========
If you have never played with pixels in canvas before, here is a good tutorial that walks you through how it works:
http://net.tutsplus.com/tutorials/javascript-ajax/canvas-from-scratch-pixel-manipulation/
http://falcon80.com/HTMLCanvas/PixelManipulation/getImageData.html

For beginners & those who want a HUGE hint on how this works, see this repo:

(SPOILER ALERT!) 
https://github.com/bgando/hint

