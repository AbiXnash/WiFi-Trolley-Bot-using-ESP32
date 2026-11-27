# WiFi Trolley Bot

A WiFi-controlled trolley bot, built as a III B.Tech CSE IIoT project by Abinash S, Srivatsan N and Hari Prasad S
(see [Project Members.txt](<Project Members.txt>) and the slides in [Wifi Trolley Bot.pptx](<Wifi Trolley Bot.pptx>)).

The board runs its own WiFi access point and a small web server. A phone app sends driving commands over HTTP, and
the board drives two DC motors through an L298N motor driver.

> The repository name says ESP32, but the sketch is written for an **ESP8266 (NodeMCU)** board: it uses
> `ESP8266WiFi` and `ESP8266WebServer`.

## Hardware

- NodeMCU (ESP8266) board
- L298N motor driver
- Two (or four, paired) DC motors, wheels and chassis
- Battery pack for the motors and board

| L298N pin | NodeMCU pin |
|-----------|-------------|
| ENA (right speed) | GPIO14 (D5) |
| IN1 / IN2 (right) | GPIO15 (D8) / GPIO13 (D7) |
| ENB (left speed) | GPIO12 (D6) |
| IN3 / IN4 (left) | GPIO2 (D4) / GPIO0 (D3) |

## Flash the sketch

1. Install the [Arduino IDE](https://www.arduino.cc/en/software) and the **ESP8266** board package (Boards Manager
   URL `http://arduino.esp8266.com/stable/package_esp8266com_index.json`).
2. Open [`IIoT_WiFi Trolley Bot Code/sketch_feb2b.ino`](<IIoT_WiFi Trolley Bot Code/sketch_feb2b.ino>).
3. Select **NodeMCU 1.0 (ESP-12E Module)** and the right port, then upload.

## Drive it

1. Power the bot. It starts an open access point called **NodeMCU Car** (serial at 115200 prints its IP, normally
   `192.168.4.1`).
2. Install [`NodeMCU_Car.apk`](NodeMCU_Car.apk) on an Android phone and join the **NodeMCU Car** network.
3. Drive with the app. The screenshots in the code folder (`setup.png`, `go ahead.png`, ...) show each screen.

The app calls `http://<ip>/?State=<command>`. You can also send commands from a browser:

| Command | Action |
|---------|--------|
| `F` / `B` | Forward / back |
| `L` / `R` | Left / right |
| `I` / `G` | Forward-right / forward-left |
| `J` / `H` | Back-right / back-left |
| `S` | Stop |
| `0`–`9` | Speed, from 400 up to 1023 (PWM) |

## Licence

MIT, see [LICENSE](LICENSE).
