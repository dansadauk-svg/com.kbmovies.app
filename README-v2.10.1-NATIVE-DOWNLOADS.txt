KB Movies Android v2.10.1

- Correct package: com.kbmovies.app
- Correct website: https://kbmovies.ng
- versionCode 22 / versionName 2.10.1
- Minimum Android SDK 24 (Android 7.0), compatible with Google Play automatic protection
- Native Android download progress notification
- Visible and audible "download started" foreground notification using a new
  high-importance Android channel (required to replace the previous silent channel)
- Pause, Resume and Cancel notification actions
- Resumable R2 downloads using HTTP Range
- Movie files saved under Downloads/KB Movies
- Existing KB_* GitHub signing secrets are used
- KB upload certificate SHA-1: 3A:D7:15:3B:F6:30:CB:D3:DE:E3:17:19:D7:7B:37:8C:A0:36:15:77
- CI removes the exact stale ng/com/mkmovies source directory left by older
  mixed repository uploads and verifies com/kbmovies/app before compiling.
