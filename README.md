# Random Joke Generator App

A fun Flutter application that generates random jokes using the JokeAPI.

## ✨ Features

😂 **Random Jokes** - Get random jokes with a single tap  
🔄 **Refresh Button** - Load new jokes instantly  
📱 **Material Design 3** - Modern and beautiful UI  
⚡ **Fast Loading** - Quick API responses  
🎯 **Two Types** - Single-line and setup-delivery jokes  
❌ **Error Handling** - Graceful error messages with retry option  
⏱️ **Timeout Handling** - 10-second request timeout  

## Getting Started

### Prerequisites
- Flutter SDK (3.0.0 or higher)
- Dart SDK

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Ayushraj999-tech/joke-generator-app.git
cd joke-generator-app
```

2. Get dependencies:
```bash
flutter pub get
```

3. Run the app:
```bash
flutter run
```

## How It Works

### API Integration
- Uses **Official Joke API** (https://official-joke-api.appspot.com)
- Fetches random jokes with HTTP requests
- Handles two joke types:
  - **Single-part**: Direct joke text
  - **Two-part**: Setup and delivery

### Joke Model
```dart
Joke {
  String type,        // "single" or "twopart"
  String setup,       // Setup for two-part jokes
  String delivery,    // Punchline for two-part jokes
  String joke,        // Full joke for single-part
}
```

## Dependencies

- **flutter**: Core Flutter framework
- **http**: ^1.1.0 - For API requests

## Usage

1. **Launch the app** - You'll see a random joke on startup
2. **Get New Joke** - Press the "Get Another Joke" button
3. **View Different Types**:
   - Single jokes appear all in one section
   - Two-part jokes show setup first, then punchline
4. **Error Handling** - If request fails, tap "Try Again"

## API Details

### Endpoint
```
GET https://official-joke-api.appspot.com/random_joke
```

### Response
```json
{
  "type": "twopart",
  "setup": "Why don't scientists trust atoms?",
  "delivery": "Because they make up everything!",
  "id": 13
}
```

## Code Structure

```
lib/
├── main.dart
├── JokeGeneratorApp          # Root widget
├── Joke                       # Model class
└── JokeHomePage              # UI and API integration
```

## Building APK

### Release APK:
```bash
flutter build apk --release
```

APK location: `build/app/outputs/flutter-apk/app-release.apk`

### Install on Device:
```bash
flutter install
```

## Features Explained

### FutureBuilder
- Handles async API calls elegantly
- Shows loading state while fetching
- Displays error with retry option
- Shows joke once loaded

### Error Handling
- Network timeout (10 seconds)
- API errors with user-friendly messages
- Retry button for failed requests

### UI/UX
- Beautiful Material Design 3 card
- Large emoji for visual appeal
- Clear separation between setup and delivery
- Disabled button during loading

## Future Enhancements

- [ ] Share jokes on social media
- [ ] Favorite jokes storage
- [ ] Filter jokes by category
- [ ] Dark mode support
- [ ] Offline joke cache
- [ ] Custom joke categories
- [ ] Joke history
- [ ] Search jokes

## License

This project is open source and available under the MIT License.

## Author

**Ayushraj999-tech**

---

**Repository:** https://github.com/Ayushraj999-tech/joke-generator-app

**API:** https://official-joke-api.appspot.com
