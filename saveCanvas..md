##DOWNLOAD BUTTON
Taken from http://weworkweplay.com/play/saving-html5-canvas-as-image/

Start off with creating a basic <a>.
  <a href="#" class="button" id="btn-download">Download</a>

All you need to do is listen to the click:

  var button = document.getElementById('btn-download');
  button.addEventListener('click', function (e) {
      var dataURL = canvas.toDataURL('image/png');
      button.href = dataURL;
  });

Running this results in a button that opens the canvas image in the browser window. 
Forcing download on the front-end side using the download attribute is a relatively 
young feature, supported only by Chrome and Firefox. It's better than nothing. You 
could try a cross-browser solution using a server-side file processor and AJAX, but 
I won't cover that in this post.

  <a href="#" class="button" id="btn-download" download="my-file-name.png">Download</a>

That's it! Remember that if you don't explicitly draw a background, it'll be a 
transparent PNG. Have fun drawing!
