# MotoMicTester

Android Studio project for testing audio input routing on Moto G Stylus 2023 / XT2315-5.

## What it does

- Lists Android-exposed audio input devices.
- Lets you select an input device.
- Calls AudioRecord.setPreferredDevice() with the selected device.
- Records PCM audio.
- Shows a basic input level meter.
- Plays the last recording.

## Important limitation

Android does not guarantee that a device listed as an input corresponds to a specific physical microphone. The Motorola audio HAL may ignore an app's preferred input device. This project therefore tests what Android exposes; it does not modify WhatsApp's microphone routing.

## Build

Open the project in Android Studio, let Gradle sync, then:

Build > Build APK(s)

The debug APK will normally be under:

app/build/outputs/apk/debug/app-debug.apk
