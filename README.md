<div align="center">

# **ARVI**

Meet Arvi, the world’s leading open-source AI wearable that revolutionizes how you capture and manage conversations. Simply connect Friend to your mobile device and enjoy automatic, high-quality transcriptions of meetings, chats, and voice memos wherever you are.


[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)&ensp;&ensp;&ensp;


</div>

## Features

- **Real-Time AI Audio Processing**: Leverage powerful on-device AI capabilities for real-time audio analysis.
- **Low-powered Bluetooth**: Capture audio for 24h+ on a small button battery
- **Open-Source Software**: Access and contribute to the pin's software stack, designed with openness and community collaboration in mind.
- **Wearable Design**: Experience unparalleled convenience with ergonomic and lightweight design, perfect for everyday wear.

## Get Started with our Documentation:


## Contribution:



## How it works

```mermaid
graph TD;
   A[Device] -- Streams Audio --> B[Phone App];
   B -- Transmits --> C[Deepgram];
   C -- Returns Transcript --> D[Phone App];
   D -- Sends Transcript to Plugins Enabled --> G[Community Plugins];
   D -- Saves Original Transcript --> E[Phone Storage];
   G -- Saves Plugin Responses --> E;

classDef lightMode fill:#FFFFFF, stroke:#333333, color:#333333;
classDef darkMode fill:#333333, stroke:#FFFFFF, color:#FFFFFF;

classDef lightModeLinks stroke:#333333;
classDef darkModeLinks stroke:#FFFFFF;

class A,B,C,D,E,G lightMode;
class A,B,C,D,E,G darkMode;

linkStyle 0 stroke:#FF4136, stroke-width:2px;
linkStyle 1 stroke:#1ABC9C, stroke-width:2px;
linkStyle 2 stroke:#0074D9, stroke-width:2px;
linkStyle 3 stroke:#FFCC00, stroke-width:2px;
linkStyle 4 stroke:#2ECC40, stroke-width:2px;
linkStyle 5 stroke:#B10DC9, stroke-width:2px;

```

## Get the software


Or you can build your own app from the sources in `apps/AppWithWearable` and firmware from `firmware` folders.



# Getting Started

Follow these steps to get started with your Friend.

### Install the app

Before starting, make sure you have the following installed:

- Flutter SDK
- Dart SDK
- Xcode (for iOS)
- Android Studio (for Android)
- CocoaPods (for iOS dependencies)

### Setup Instructions

1. **Upgrade Flutter**:
   Before proceeding, make sure your Flutter SDK is up to date:
    ```
    flutter upgrade
    ```

2. **Get Flutter Dependencies**:
   From within `apps/AppWithWearable`, install flutter packages:
    ```
    flutter pub get
    ```

3. **Install iOS Pods**:
   Navigate to the iOS directory and install the CocoaPods dependencies:
    ```
    cd ios
    pod install
    pod repo update
    ```

4. **Environment Configuration**:
   Create `.env` using template `.env.template`
    ```
    cd ..
    cat .env.template > .env
    ```

5. **API Keys**:
   Add your API keys to the `.env` file. (Sentry is not needed)

6. **Run Build Runner**:
   Generate necessary files with Build Runner:
    ```
    dart run build_runner build
    ```

7. **Run the App**:
    - Select your target device in Xcode or Android Studio.
    - Run the app.



## Licensing

Arvi is available under MIT License
