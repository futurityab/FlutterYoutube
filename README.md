# flutter_youtube

Flutter plugin to play youtube videos

Supported

- Android
- iOS

Violates YT TOS on iOS, if that is important for you, don't use it.
This is just educational code, forked from https://github.com/PonnamKarthik/FlutterYoutube.

## How to Use

```yaml
dependencies:
  flutter_youtube: "^2.0.0"
```

### Imports

```dart
import 'package:flutter_youtube/flutter_youtube.dart';
```

### Code

```dart

FlutterYoutube.playYoutubeVideoByUrl(
  apiKey: "<API_KEY>",
  videoUrl: "<Youtube Video URL>",
  autoPlay: true, //default falase
  fullScreen: true //default false
);
```

### Video End Listener

> Note Right now only supported in android

```dart
FlutterYoutube.onVideoEnded.listen((onData) {
  //perform your action when video playing is done
});
```

| Key        | Value              | Default |
| ---------- | ------------------ | ------- |
| apiKey     | String (Not Null)  |
| videoUrl   | String (Not Null)  |
| videoId    | String (Not Null)  |
| autoPlay   | Boolean (Optional) | false   |
| fullScreen | Boolean (Optional) | false   |

### API Key
Your API key is what you need to use so your application can submit API requests to youtube.
For that you are gonna need a Google Account to access the Google API Console, request an API key, and register your application.
After that create a project in the Google Developers Console and obtain authorization credentials so your application can submit API requests.
More info here https://developers.google.com/youtube/v3/getting-started
