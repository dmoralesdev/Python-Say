# Python-Say
 Python script to leverage Pico2Wave or Google TTS (from Google Translate) to convert text to speech.
 
 ## Pico2Wave:
 
 The Pico Text-to-Speech (TTS) service uses the TTS binary from SVOX for producing spoken text.

 You manually need to install the pico2wave binary in order for this service to work correctly. You can, e.g., install it with apt-get:

 sudo apt-get install libttspico-utils
 
 ## Google TTS (from Google Translate):
 
 Sends a request to Google Translate and plays the returned audio using the mpg123 package, install it with apt-get:
 
 sudo apt-get install mpg123
 
 ## Usage:
 
    Args:
        text: The text you want to speak.
        lang: The language to use. Supported languages are:
            en-US, en-GB, de-DE, es-ES, fr-FR, it-IT.
        engine: Options are:
            gtts, pico
        Only for Pico2Wave from here onwards
        volume: Volume level for the converted audio. The normal volume level is
            100. Valid volume levels are between 0 (no audible output) and 500 (increasing the
            volume by a factor of 5). Values higher than 100 might result in degraded signal
            quality due to saturation effects (clipping) and is not recommended. To instead adjust
            the volume output of your device, enter ``alsamixer`` at the command line.
        pitch: The pitch level for the voice. The normal pitch level is 100, the allowed values lie
            between 50 (one octave lower) and 200 (one octave higher).
        speed: The speed of the voice. The normal speed level is 100, the allowed values lie
            between 20 (slowing down by a factor of 5) and 500 (speeding up by a factor of 5).
        device: The PCM device name. Leave as ``default`` to use the default ALSA soundcard.

