# ysay-hotkey
<b>ysay (2023) - Output (read aloud) selected text with speech synthesis (piper) (in German) as an audio stream using a key combination.</b>

*<b>Inspired by:*</b>
*   the use of xsel from the script xsay by Alex (https://www.youtube.com/watch?v=UjBtKRd7c34)
*   the procedure for voice output with piper from Thorsten-Voice (https://www.thorsten-voice.de/kostenloses-deutsches-text-to-speech-tts)

<b>Requirements:</b>

* piper: https://github.com/rhasspy/piper/releases
* espeak,xsel:  <code>sudo apt-get install espeak-ng xsel</code>
* speech files: https://huggingface.co/rhasspy/piper-voices/tree/main/de/de_DE (.onnx und onnx.json of the corresponding voice)

<b>Installation:</b>

* copy the directory of the unpacked piper package to \~bin/ and place the language files in the piper directory (~/bin/piper/)
* copy ysay and ysaykill to ~bin/ 
* now assign the key combinations in the system settings, i have decided on Win+S
  *   Super/Meta+S  output marked text  (~/bin/ysay)
  *   Super/Meta+Shift+S cancel current audio output  (~/bin/ysaykill)

The scripts, language files and piper can of course also be copied to any other path, e.g. under /usr/local/, in which case the path details in the scripts must be adapted.

Tested with Kubuntu 22.04LTS and 23.10 (should work with any distro) with four German (many more available) language models.
Should work on all other dislay managers (though ot tested) other than KDE.

<b>History:</b>
<br> Over the last few years, i've tried to set up a reasonable voice output under Linux from time to time and have tried practically everything with combinations of espeak/mbrola/speechd/flite/ivona/festival/festvox/jovie/gespeaker/ktts/orca/etc...
<br> None of these had really worked (well) in terms of usability and output quality, especially not in German.
<br> Especially in comparison to Android, where there has been very good speech output for years even without Google/Cloud, I find the situation on the Linux desktop pathetic, even under KDE the languages sound bad via speechd. 
<br> I used xsay for a short time, but rarely because of the poor sound quality of the Pico voice. 

<b>Why another script then?</b>
<br> This one works ;-), has a better audio quality and omits the need for temporary wav- or mp3-files
<br> During my latest spontaneous attempt, I came across piper (rather by chance) and was amazed at how quick and easy it was.
<br> The voice quality with all the voices (that I tested) is much better than with Pico and is good enough for me to have longer texts read aloud.

<b>Errors/improvements</b>
<br> I tested it on two computers, it was a successful quick fix for me and I have no plans to turn it into a larger development project.
<br>If you have any errors or suggestions for improvement, please feel free to contact me.
