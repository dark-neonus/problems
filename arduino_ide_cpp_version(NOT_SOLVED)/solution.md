NOT SOLVED!

After updates of libraries or just random shit version of c++ can be changed. For bobot project you interested specifically in esp32s2 platform.

To change build configurations(c++ version) go to `/home/dark-neonus/.arduino15/packages/arduino/hardware/esp32/2.0.18-arduino.5` and open `platform.txt`
As DeapSeak recommended find there `compiler.cpp.flags.esp32s2=...` and look at that line and change version of `-std` from any fuck there(like gnu++11) to `-std=gnu++23`.
After that save changes(for gods sake, or not, save backup of that file) and CLOSE ArduinoIDE in order of changes to apply and OPEN IT AGAIN.

Okay. that didnt worked, fuck. I think something wrong with location where I found `platform.txt` but as I remember, it is right location.
Okay I will try to look to other locations and change other files.

Fuck yeah, I finally looked at the error message in ArduinIDE and I found(as i thing right now) right location in my home directory `/home/dark-neonus/.arduino15/packages/esp32/hardware/esp32/3.2.0-RC2`.
So now i will try to do the same with `platform.txt` here.(I will just copy-paste instructions)

It didnt worked.
Th(a/e)n I tried to look in other suspicios directory `/home/dark-neonus/.arduino15/packages/arduino/hardware/esp32/2.0.18-arduino.5` and I dounf `platform.txt` there too.
And you know what? Yeah, fuck, in that file already was esp32s2=...-std=gnu++23.
So FUCK, error somewhere else.

Okay, fuck fuck fuck this is the fucking 1.5 hours I am trying to just fucking COMPILE READY CODE!!! I am giving up, I didnt find problem cause.
I have tried to change different `platform.txt` in different folders and it didnt work. I have tried to reinstall esp32 core in ArduinoIde(not the one from Arduino, but that which provide more boards), and SUPRISE: IT DIDNT WORK!

I give up and just change code(using AI) to not use format, but sme other stupid shit.

FUCK IT!
