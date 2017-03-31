# Audio editing

You wouldn't leave a camera and walk away - treat audio recording the same. Think about where you're positioning it, listen to background sound etc.

# Adobe Audition and audio editing

Two modes in top left corner: 

* Waveform: for editing a single audio sample
* Multitrack: for piecing together all of your audio into a show or packages

Easiest way to click and drag into the Files area in the upper left corner. This shows files you are working on at the moment.

You can bring a video file in and it will take the audio track from that. It will also work together with Adobe Premiere.

Don't confuse this with the *Media Browser* area underneath which shows files on your computer more generally.

Double-click on a file to see it in the main window:

* Across the top is time
* Up the side is decibels (volume)
* Note L and R - you can click on either to turn that channel on or off - quite common if you're recording on a video or camera, where audio might only be recorded on one channel: you can copy audio from one channel into the empty one to get stereo.

Number 1.wav is a mono file - you can also convert it to mono by selecting *Edit > Convert sample type* then in the *Channels* section change from Mono to Stereo.

![](https://raw.githubusercontent.com/paulbradshaw/MED7126/master/mono.PNG)

Press space bar to play the audio: below the waveform you will see the **Levels** box which shows whether the levels are 'peaking' (too high, denoted by the red area at the far right), creating clipping or distortion, or too low (in the green).

Ho Ho Ho.wav is an example of a file which peaks in the red.

If you record your audio in a distorted form, you cannot get rid of that distortion.

# Ways to adjust audio

When you hover over the audio waves (or a selection) you should see a small icon menu appear, called the HUD (Heads Up Display). The icons are:

* A series of bars
* A dial
* +0 dB
* a pin (click this to pin the HUD in position)

You can click and drag on the dial to adjust the volume; likewise you can click on the dB number to change the decibels.

Better to use the **Effects** menu at the top of the screen:

*Effects > Amplitude and Compression > Normalize*

![](https://raw.githubusercontent.com/paulbradshaw/MED7126/master/normalize.PNG)

Normalize at 99%

Some software (like Adobe Premiere) treats hitting 0 as peaking; others (like Adobe Audition) sees it as not peaking, so avoid 100%.

# The playback controls

The playback buttons (play, go back, go to end, record) are straightforward, but the loop option (toggle on or off) is useful as it will continue to loop what is selected while you make the changes

The zoom options include both horizontal and vertical zooms. Avoid the vertical zoom as it will look like the audio is too loud but you've just zoomed in. To the far right are also options to automatically zoom to selection, to the out point of the selection, or the in point of the selection (where it begins).

Click and drag to select a section; double-click to select everything.

# EQ (equalisation) and treble

Each audio includes sounds that resonate at different frequencies. You can isolate a particular frequency and increase or decrease the volume of that frequency (leaving other frequencies unaffected). In music this might be turning up the bass, but in journalism you might use this to reduce background noise. Select:

*Effects > Filter and EQ*

You can choose how many bands you're controlling: 10 bands for example will give you 10 controllers to affect different frequencies. Note that loop is here too so you can have sound looping while you change the EQ.

Low frequencies have much bigger sound waves which travel more easily through solid objects - this is why when you stand outside a club or pub you hear the bass sounds of the music inside, but not the high ones.

High frequencies have smaller sound waves. Small speakers do not have enough power to generate the larger sound waves, which is why phones and laptops sound 'tinny'.

## Noise reduction

Capture the frequency of a selection by clicking on:

*Effects > Noise Reduction/Restoration > Noise Print*

![](https://raw.githubusercontent.com/paulbradshaw/MED7126/master/noiseprint.PNG)

To see what you have just captured, click:

*Effects > Noise Reduction/Restoration > Noise Reduction (process)*

Here you can also change how much it is going to reduce that frequency by.

Make sure you select all the audio before applying - you can do that within this menu by clicking **Select entire file**

![](https://raw.githubusercontent.com/paulbradshaw/MED7126/master/noisereduction_notes.png)

You can add a fade in or a fade out by going to:

*Effects > Fade In* 

Or:

*Effects > Fade Out*

You can also click and drag the small box in the upper left area of the audio to change the fade.
