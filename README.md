This is an unofficial Dockerized i2pd within a Debian Jessie image.

Run with the following:

````
docker run --name i2pd -p 7070:7070 -p 4446:4446 -p 6668:6668 derand/i2pd
````

Publish how many (or how few) ports as you want. Ports exposed by default include

* 2827 — BOB
* 4446 — eepSite proxy
* 6668 — Irc2P proxy
* 7650 — I2PControl
* 7655 — SAM (UDP)
* 7656 — SAM (TCP)
