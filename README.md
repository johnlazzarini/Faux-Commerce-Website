## Simple webpage advertisement
#### https://johnlazzarini.github.io/drone-deploy-webpage-ad/

## Summary
Simple proof of concept which is made up of text over a looping, muted stock video captured by an aerial drone and made available through pixabay.

## Implementation details
#### HTML
The workhorse element is represented by a simple video tag, placed at the bottom of the body.
```
<video id="my-video" class="video" autoplay="autoplay" loop="loop" muted="">
            <source src="lake.mp4" type="video/mp4" />
</video>
```
The included properties are essential to creating a captivating but non-intrusive user experience.
- Video starts immediately on load
- Sound is muted
- Video loops through 12 second cycles

##### Why this video in particular?
It's important for the video to be short enough such that the FPS displays fluidly over different connections.  This video consists of a series of cuts, which creates the illusion that the video is longer than it actually is, and results in a natural looping pattern.  

#### CSS
This webpage is very simple, and there isn't much more than intermediate CSS at play accordingly.

But since a video HTML element is fairly new territory for front-end developers, I'd just like to point out some of the CSS that I used to stylize the looping aerial video:
```
.video {
  position: fixed;
  top: 50%; left: 50%;
  z-index: 1;
  min-width: 100%;
  min-height: 100%;
  width: auto;
  height: auto;
  transform: translate(-50%, -50%);
}
```
It's neccessary for the video to take up the whole screen in terms of percentages, which lends itself to a more responsive design pattern.  The position is fixed so that the text on the webpage can be overlayed on top of the video.

## Possible use cases
Could be displayed as a modal over websites such as Forbes Technology, WIRED, etc.
