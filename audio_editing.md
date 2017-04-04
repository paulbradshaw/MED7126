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

## Ways to adjust audio

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

## The playback controls

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

Here you can also change how much it is going to reduce that frequency by changing the settings.

Make sure you select all the audio before applying - you can do that within this menu by clicking **Select entire file**

![](https://raw.githubusercontent.com/paulbradshaw/MED7126/master/noisereduction_notes.png)

## Fading in or out

You might have noise at the start that you want to avoid by adding a fade in or a fade out. You can do this by going to:

*Effects > Fade In* 

Or:

*Effects > Fade Out*

You can also click and drag the small box in the upper left area of the audio to change the fade.

![](https://raw.githubusercontent.com/paulbradshaw/MED7126/master/fadein_notes.png)

## Getting rid of clicks

You can get rid of clicks by deleting that section of the audio, or reducing the volume, but there's also the **Automatic click remover**. This works by identifying an unusual noise in the context of other noise in the same selection, so you need to select the section containing both the click and 'normal' noise. Then click:

*Effects > Noise Reduction/Restoration > Automatic Click Remover*

This will bring up a window where you can choose how strict or not the process is. Note that there are presets you can select for 'Heavy' reduction (strict), 'Light' reduction (less strict) or 'Medium'. A strict reduction might be very effective but leave you with audio which sounds too processed, so try a few approaches.

![](https://raw.githubusercontent.com/paulbradshaw/MED7126/master/autoclickremover_notes.png)

[Workshop Tagline.wav](https://github.com/paulbradshaw/MED7126/blob/master/audio/Workshop%20Tagline.wav) is a useful file to work on some of these techniques

## Compression

[TechTeam_intro.mp3](https://github.com/paulbradshaw/MED7126/blob/master/audio/TechTeam_intro.mp3)

Select:

*Effects > Amplitude and Compression > Single-band compressor*

There are lots of presets: chances are one will work for your audio, e.g. Radio leveler, or Voice leveler (even quiet sounds like 's' and 'h' will be made as prominent as louder sounds). You don't always want this levelling, but that's what it does.

Top two faders are most important: 

* Threshold (when do I start changing audio) - look at the graph of the audio to identify where you want to 'cut back' unusually high or low sounds
* Ratio (hwo strongly do you want to reduce)

For example, if the threshold is -10 and the ratio is 12-to-1, for every 12 decibels above -10 you'll get 1 dB of sound out. The more it goes above, the more severe the compression will be, this preserves the dynamic between different levels.

Other faders include:

* Attack (how quickly do you begin compressing - think of a slight fade in of compression)
* Release (how quickly do you stop - think of a fade out, in miliseconds)
* Output gain

## Multitrack editing

Switch from the *Waveform* tab in the upper left area to the *Multitrack* tab. A window will appear asking you to choose settings for your new project.

* **Template**: there are some pre-set options here for different types of projects. For example 'Podcast' is one option, as is a Radio VO (voiceover).
* **Sample Rate** is how often is it going to take a snapshot of the audio
* **Bit Depth** is how detailed that snapshot is going to be

Note that the podcast preset has 44100 sample rate and 16 bit depth.

These all affect the file size that will result - but it is always best to edit at a high quality and then consider exporting as a lower quality to optimise file size.

### Compiling multitrack

Click and drag from files into tracks to make your package. If the file is a different sample rate a warning will appear offering to convert it - say 'yes'.

On the tracks you should see a yellow and a blue line:
* The yellow line is volume control
* The blue line is a panning control (from left to right channel)

Note that if you drag clips over each other, yellow lines will appear to indicate the cross fade. These can also be dragged to change the nature of the cross fade.

### Editing fades or pans in multitrack

To add fades in or out, click on the yellow line once to create a key frame where the fade should start. Click again at another point to create another where it should stop. Then click and drag to move the lines (volume) between key frames, controlling how much it fades and where.

The same process applies to the blue lines, creating key frames at the points where you want to change the pan, and then dragging the lines between keyframes to change the pan from left to right or vice versa.

This doesn't affect the original sound file so you can use it over and over again with different settings in different contexts.

Changes in the **waveform view**, however (if you double-click on an audio element, or switch back to waveform and amend files there), will be reflected in any projects using that.

To avoid this happening, right-click on a multitrack instance and select *Convert to unique copy* if you want to make a change to the waveform itself without affecting others (this basically creates a duplicate file).

### Mute channels or record directly

To the left of each track you should see three buttons:

* M: mute the channel
* S: make this channel the *sole* channel playing (muting all others)
* and R: record directly into that channel.

### Other buttons and controls

The *Magnet* button towards the top of the screen will make clips snap into position parallel with others. This toggles on and off

You can drag start edge or end of clips in or out to trim it.

At the top: the *razor blade* button will chop where you click, to create new clips.

The *History* tab in the bottom left corner shows all the actions you have performed. You can go back through that list to undo particular actions.

*Export to Adobe Premiere Pro* in the multitrack menu will directly export your audio to the video editing package. It is best to edit video first then export audio to Audition to tidy up before exporting back into Premiere. A small thumbnail of video will also appear in the bottom corner so you can see that alongside the audio.

# Saving audio

If you are in multitrack view and select *Save* it will save a **project file**. To save as an audio file that you can publish (such as an mp3 or wav) go to *Export > Multitrack mixdown*.

In waveform view you can *save* to overwrite the existing file(s) or *save as* a new file. You can also choose *Export* to save as a different file type.

Select *Save All* to ensure you save all the changes to all audio files you have made.
