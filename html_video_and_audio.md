# HTML Video & Audio
-Video can have a self closing tag `<video..../>` also have to add a type, `type="video/mp4"`.
-Controls attribute does not need a classification. just `controls`. Can also remove `controls` and use `autoplay`, which does what it says it does.

## Video Sourcing
-Create `<source> element`(does not need closing tag) to add multiple video formats for multiple browser support.

-[Video Documentation on MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video)

## Audio Element
*Syntax*
```
<audio controls(or other play options)>
  <source src="url" type="audio/mp3(or other audio type)">
</audio>
```

-[Audio Documentation on MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio)

## Creating Media (File Sizes)
-Programs to help with Media conversion to h.264
  * [VLC](http://www.videolan.org/vlc/index.html)
  * Adobe Media Encoder

-Also want to create .OGG files.

-Want to create the smaller file size, change bit rate to 5000 or 10000.

## Captioning A Video
-2 types of caption file formats, '.srt' or *'webvtt'*
-Create a new file name, "file-name.vtt"

*Syntax*
```
WEBVIT file

0
00:00:00.500 --> 00:00:05.000(length of caption)
[This is our caption.]

1(this number goes up with each caption)
00:00:06.000 --> 00:00:010.000(length of caption)
[This is another caption.]
```
-[Live WebVTT Validator](https://quuz.org/webvtt/), use to make sure captions work.

## The Track Element
-Within the video element add the `<track>` element(self closing)...
*Syntax*
```
<track label="English(not language, just explination) kind="subtitles" srclang="en(for english) src="file.vtt" default(shows captions no matter what)>
```
-Adds CC button to player controls.
