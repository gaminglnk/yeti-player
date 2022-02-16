## Modified [Yeti Player]
This is a modified version of Plyr with a yellow theme.

[Checkout the demo](https://codepen.io/gaminglnk/full/BamRLrW). This is specially for ```HTML5 Video Player```.

# Installation
In order to use this player you'll have to add the CSS, Js, Loader Js and HTML from below, in your HTML page.
## HTML5 Video
```html
<video style="object-fit: cover;"
            class="yeti-player"
            crossorigin
            controls
            playsinline
            preload="none"
            poster="sample.jpg">
       
            <!-- HD Source -->
            <source size="720"
                    type="video/mp4" 
                    src="sample.mp4" />
       
            <!-- SD Source -->
            <source size="480"
                    type="video/mp4"
                    src="sample.mp4" />
       
            <!-- Captions  -->
            <track default=""
                   label="English"
                   kind="captions"
                   srclang="en"
                   src="sample.vtt" />
       
            Your browser does not support the HTML5 video tag.
     </video>
```
- Replace `sample.mp4` in source with your video file url or name.
- Replace `sample.jpg` in poster with your thumbnail url or name.
- Replace `sample.vtt` in captions with your captions url or name.

## CSS
You can install the stylesheet using this code :
```html
<style>@import url(https://cdn.jsdelivr.net/gh/gaminglnk/static/plyr/player.css);</style>
```
...or use this if above doesn't work :
```html
<style>@import url(https://www.speedynet.eu.org/assets/css/player.css);</style>
```
## JavaScript
You can install the javascript using this code before closing ```</body>```
```html
<script src="https://cdn.jsdelivr.net/gh/gaminglnk/static/plyr/player.js"></script>
```
...or use this if above doesn't work :
```html
<script src="https://www.speedynet.eu.org/assets/js/player.js"></script>
```
## Load the Player
At last you will have to add this code just below the JavaScript to load the player (Recommended to no to change the code, incase you don't know what you are doing).
```html
<script>
var controls = [
    'play-large',
    'rewind', // 10 sec back.
    'play', // Play/pause playback.
    'fast-forward', // 10 sec forward.
    'progress', // The progress bar.
    'current-time', // The current time of playback
    'duration', // The full duration of the media
    'mute',
    'settings', // Settings menu.
    'airplay', // Airplay (For safari only)
    'fullscreen' // Toggle fullscreen.
    // 'download', // Download button for media
    // 'restart',
    // 'pip', // Picture-in-picture
];
const player = new Plyr('.yeti-player', {
    controls });
</script>
```
After adding the above code. It is necessary to add ```class="yeti-player"``` in your ```<video>``` or ```<iframe>``` tag in order to load the player.

*View code on **[codepen.io](https://codepen.io/gaminglnk/pen/BamRLrW)** online.*
