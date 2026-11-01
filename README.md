# KB Movies Android App

Native Android WebView app for KB Movies.

## App configuration

- App name: KB Movies
- Package: `com.kbmovies.app`
- Version: `2.7.0` (`versionCode 17`)
- Website: `https://kbmovies.ng/`
- Minimum Android: 6.0, API 23
- Target Android: API 36
- Push service: Firebase Cloud Messaging

## Included features

- Website and Flutterwave checkout open inside the app
- Payment redirects return inside the app
- Android Download Manager support for movie downloads
- Native Firebase push notifications
- Notification clicks open the supplied website page
- Pull to refresh and Android back navigation
- Fullscreen video playback
- File upload chooser
- KB Movies splash screen with progress bar and percentage
- GitHub Actions release APK and AAB build

## GitHub repository secrets

Add these under Settings, Secrets and variables, Actions:

- `KB_KEYSTORE_BASE64`
- `KB_KEYSTORE_PASSWORD`
- `KB_KEY_PASSWORD`

The workflow uses alias `kb_movies`.

Create the Base64 value in Windows PowerShell:

```powershell
[Convert]::ToBase64String([IO.File]::ReadAllBytes("kb-movies-release-key.jks")) | Set-Clipboard
```

Paste the copied value into `KB_KEYSTORE_BASE64`.

## Build with GitHub

1. Upload the contents of this folder to the root of a private GitHub repository.
2. Add the three repository secrets.
3. Open Actions.
4. Select `Build KB Movies APK and AAB`.
5. Select Run workflow.
6. Download the APK and AAB from the completed workflow artifacts.

Never upload the signing key or its passwords to the repository.

## WordPress push notifications

The app registers Firebase tokens at:

`https://kbmovies.ng/wp-json/mkpush/v2/register-token`

Your WordPress push plugin must use the Firebase service-account credentials from the `kbmovies-9efc4` Firebase project.
