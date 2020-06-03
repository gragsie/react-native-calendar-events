Passing an array of calendar ID's to fetchAllEvents, doesn't appear to have any effect.

### Environment
System:
    OS: macOS 10.15.5
    CPU: (8) x64 Intel(R) Core(TM) i7-6700K CPU @ 4.00GHz
    Memory: 3.22 GB / 32.00 GB
    Shell: 3.2.57 - /bin/bash
  Binaries:
    Node: 13.5.0 - ~/.nvm/versions/node/v13.5.0/bin/node
    Yarn: 1.21.1 - /usr/local/bin/yarn
    npm: 6.13.4 - ~/.nvm/versions/node/v13.5.0/bin/npm
    Watchman: 4.9.0 - /usr/local/bin/watchman
  SDKs:
    iOS SDK:
      Platforms: iOS 13.5, DriverKit 19.0, macOS 10.15, tvOS 13.4, watchOS 6.2
    Android SDK:
      API Levels: 24, 25, 28, 29
      Build Tools: 25.0.2, 28.0.0, 28.0.1, 28.0.2, 28.0.3, 29.0.0, 29.0.1, 29.0.2
      System Images: android-28 | Intel x86 Atom_64, android-28 | Google APIs Intel x86 Atom, android-28 | Google Play Intel x86 Atom, android-29 | Intel x86 Atom_64
  IDEs:
    Android Studio: 4.0 AI-193.6911.18.40.6514223
    Xcode: 11.5/11E608c - /usr/bin/xcodebuild
  npmPackages:
    react: 16.9.0 => 16.9.0 
    react-native: 0.61.5 => 0.61.5 
  npmGlobalPackages:
    react-native-cli: 2.0.1

### Steps to Reproduce
  let calendarsToShow = ["junk"]
  let events = await RNCalendarEvents.fetchAllEvents(
        theDay.toISOString(),
        nextDay.toISOString(),
        calendarsToShow // Returns events for all calendars, even though it should not return anything
   );

### Expected Behavior
Should not return any events

### Actual Behavior
Returns events for all calendars
