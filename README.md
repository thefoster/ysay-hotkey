# ysay-hotkey
<b>ysay (2023) - Markierten Text mit Sprachsynthese (piper) auf deutsch per Tastenkombination als Audiostream ausgeben (vorlesen).</b>

*Inspiriert von:*</b>
*   der Verwendung von xsel aus dem Script xsay von Alex (https://www.youtube.com/watch?v=UjBtKRd7c34)
*   dem Vorgehen zur Sprachausgabe mit piper von Thorsten-Voice (https://www.thorsten-voice.de/kostenloses-deutsches-text-to-speech-tts

<b>Benötigt:</b>

* piper: https://github.com/rhasspy/piper/releases
* espeak,xsel:  <code>sudo apt-get install espeak-ng xsel</code>
* Sprachdateien: https://huggingface.co/rhasspy/piper-voices/tree/main/de/de_DE (.onnx und onnx.json der jeweiligen Stimme)

<b>Installation:</b>

* Das Verzeichnis des entpackten piper-Pakets nach \~bin/ kopieren und die Sprachdateien in das piper-Verzeichnis (~/bin/piper/) legen
* ysay und ysaykill nach ~bin/ kopieren
* In den Systemeinstellungen nun noch die Tastenkombinationen zuweisen, ich habe mich für Win+S entschieden
  *   Super/Meta+S  markierten Text ausgeben  (~/bin/ysay)
  *   Super/Meta+Shift+S  Audioausgabe abbrechen  (~/bin/ysaykill)

Die Skripte, Sprachdateien und piper können natürlich auch in beliebige andere Pfade kopiert werden, z.B. unter /usr/local/, dann müssen die Pfadangaben in den Skripten angepasst werden.

Getestet mit Kubuntu 22.04 und 23.10 (sollte mit jeder Distro funktionieren) mit vier deutschen Sprachmodellen (viele weitere verfügbar).

<b>Geschichte:</b>
<br> In den letzten Jahren hatte ich immer mal wieder versucht, unter Linux eine passable Sprachausgabe einzurichten und habe praktisch alles durch an Kombinationen von espeak/mbrola/speechd/flite/ivona/festival/festvox/jovie/gespeaker/ktts/orca/etc.
<br> Nichts davon hatte bisher hinsichtlich Benutzbarkeit und Ausgabequalität wirklich (gut) funktioniert, insbesondere nicht auf deutsch.
<br> Gerade im Vergleich zu Android, wo es seit Jahren sehr gute Sprachausgabe auch ohne Google/Cloud gibt, finde ich die Situation auf dem Linux-Desktop armselig, auch unter KDE klingen die Sprachen über speechd schlecht. 
<br> Kurze Zeit hatte ich xsay verwendet, aber wegen der mageren Klangqualität der Pico-Sprache eher selten. 

<b>Warum dann ein weiteres Skript?</b>
<br> Dieses funktioniert ;-), hat eine bessere Audioqualität und kommt ohne temporäre wav-oder mp3-Datei aus.
<br> Beim aktuellen spontanen Versuch bin ich dann (eher zufällig) auf piper gestoßen und war erstaunt, wie schnell und unkompliziert das ging.
<br> Die Sprachqualität ist mit allen (von mir getesteten) Stimmen viel besser als bei Pico und für mich ausreichend gut, um auch längere Texte vorlesen zu lassen.

<b>Fehler/Verbesserungen</b>
<br> Ich habe es auf zwei Rechnern getestet, es war für mich ein erfolgreicher Schnellschuss und ich habe nicht vor, daraus ein größeres Entwicklungsprojekt zu machen.
<br>Bei Fehlern oder Verbesserungsvorschlägen könnt ihr mich aber gerne kontaktieren.
