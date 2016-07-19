# Try a JNI Demo on Dragonboard410c


Assume you are working on a dragonboard410c with Debian, you’ve attached sensors mezzanine to the baseboard, powered it up, attached it to an HDMI monitor with a keyboard and mouse, you have connected to WiFi, or installed a USB-Ethernet dongle and have that hooked up, and you have installed libsoc, jre, jdk.


## Run the jni demo and check the result

---

#### Download led_touch.jar

    $ git clone https://github.com/LiveWang/jni_Demo.git<Enter>

#### Setup the Hardware

    Attach the touch sensor to G2 (reading from GPIO-E)
    Attach the led to G3 (driving GPIO-G)

#### Run the Demo

    $ cd jni_Demo
    $ sudo java -Djava.library.path=. -jar jni_Demo.jar

Tap the touch sensor with your finger. Tap the touch sensor several times in different speed (you can try tap very fast, or keep your finger on the touch sensor for several seconds and move away or any other speed).

Check the result on your screen, number after highs should equal to number after lows every time you move your finger away from the touch sensor. If not, some interrupts were missed by the board.



