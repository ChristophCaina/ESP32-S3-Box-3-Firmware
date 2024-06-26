# ESP32-S3-Box-3-Firmware
ESP32 S3 Box 3 Firmware which combines continuous conversation, dock sensors and media player

I combined [jaymunro](https://github.com/jaymunro/esphome_firmware)'s firmware for continuous conversation and sensors support with [gnumpi](https://github.com/gnumpi/esphome_audio/tree/dev-next)'s implementation of media player. It mostly works, although in continuous conversation, after it finishes responding, it goes back to the idle screen for 1-2 seconds before listening again (which is not the case in jaymunro's implementation). In addition, sometimes it doesn't continue the conversation and stays on the idle screen (I couldn't figure why and this is not consistent). Using the media player seems to solve the low volume problem. The firmware implements the "assist query" and "assist reply" sensors which are not used in gnumpi's implementation. The firmware uses "Hey Jarvis" but you can change it to your needs. I didn't use gnumpi's images as I wanted to maintain the original feel. You will need to adjust the firmware to your own environment (wifi, ap, etc.). I did not test it extensively.

I made a few other changes:
 - I removed the frames around the text (I just like it better like that)
 - I clear the query and reply texts so that the old text doesn't display in a new query before the new one displays
 - The time is taken for Home Assistant

Thank you [jaymunro](https://github.com/jaymunro) and [gnumpi](https://github.com/gnumpi) for your good work. 
