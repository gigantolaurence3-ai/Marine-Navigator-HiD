# Marine Navigator HD — first Android build

This is the first working prototype source project. It is not yet a compiled APK.

## Included in version 1.0
- OpenStreetMap general-purpose background centered on Cebu City
- GPS location marker (requires location permission and a GPS fix)
- Tap the map to save waypoints; waypoints persist on the phone
- Add point button to save the map center
- Straight-line preview connecting saved waypoints
- Clear button

## Important limitations
- This version does NOT contain nautical charts, depth soundings, bathymetry, tide/current data, hazard overlays, or automatic marine routing.
- The background map is a general map and may be incomplete or unsuitable for navigation.
- The route is only a straight-line visual preview. It does not avoid land, reefs, shallow water, restricted areas, or hazards.
- Do not use this prototype to plan or conduct a boat trip or as a substitute for official current nautical charts and qualified guidance.

## Build using only an Android phone
1. Create/sign in to a GitHub account and create a new **private** repository named `MarineNavigatorHD`.
2. Upload the contents of this folder to the repository root (not the ZIP file itself). Ensure `.github/workflows/build-apk.yml` is included.
3. Open the repository's **Actions** tab. If prompted, enable workflows.
4. Run **Build Marine Navigator HD APK** (or push to the `main` branch).
5. When the run succeeds, open the run and download the `Marine-Navigator-HD-debug` artifact.
6. Extract the downloaded artifact ZIP. It contains `app-debug.apk`. Install it only on your own device after reviewing Android's install warning.

## Developer details
- Android Gradle Plugin 8.7.3, Gradle 8.9, JDK 17
- compileSdk/targetSdk 35, minSdk 26
- Kotlin 2.0.21, osmdroid 6.1.20
