# esp32-data-logger

[PlatformIO](https://platformio.org/platformio-ide)


    ├── src                     # source files
    │   ├── credentials.h       # user secrets
    │   ├── main.cpp            # main methods (main sketch file analogous to arduino IDE)
    ├── test                    # unit tests


## Set up project

### `pio boards ttgo` to find board in list

### `pio project init --board ttgo-t7-v13-mini32` to initialize project with your board

### `pio run --target upload` to compile and upload to board

### `pio device monitor` for serial monitor

## User secrets

### `touch src/credentials.h`

```C++
// credentials.h
#define SECRET_EMAIL <your email>
#define SECRET_PASSWORD <your password>
#define SECRET_API_KEY <api key>
#define SECRET_DATABASE_URL <your password>
#define SECRET_WIFI_SSID <wifi network name>
#define SECRET_WIFI_PASSWORD <wifi password>
```
```C++
// main.cpp
#include "credentials.h"

// Firebase
#define DATABASE_URL SECRET_DATABASE_URL
#define API_KEY SECRET_API_KEY
#define USER_EMAIL SECRET_EMAIL
#define USER_PASSWORD SECRET_PASSWORD

// WiFi
#define WIFI_SSID SECRET_WIFI_SSID
#define WIFI_PASSWORD SECRET_WIFI_PASSWORD
```
> remember to add credentials.h to .gitignore file