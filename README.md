# Expo Camera API: Erratic Behavior When Rapidly Changing Camera Properties via useEffect

This repository demonstrates a bug in the Expo Camera API related to repeatedly setting camera properties within a useEffect hook.  When rapidly changing camera configurations, attempting to modify properties like `flashMode` or `focusMode` multiple times can lead to unexpected behavior or app crashes.

## Bug Description

The issue stems from setting camera properties repeatedly within a `useEffect` hook that re-renders frequently.  This might result in conflicting property settings, causing the camera to malfunction or the application to crash.

## Reproduction

1. Clone this repository.
2. Run `npm install`.
3. Run `expo start`.
4. Observe the erratic behavior when interacting with the camera controls.

## Solution

The provided solution incorporates a check to prevent unnecessary property settings.  This ensures that camera properties are only set when there's an actual change in configuration.

## Contributing

Contributions are welcome! Please feel free to open issues and pull requests.