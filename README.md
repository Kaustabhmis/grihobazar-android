# Grihobazar Android App

An Android application for **Grihobazar** - a real estate platform for buying, renting, and selling properties in Kolkata and West Bengal, India.

## Features

- 🏠 **Browse Properties** - Search and filter properties for buying, renting, or selling
- 🔍 **Advanced Search** - Filter by location, price, property type, and more
- ❤️ **Favorites** - Save your favorite properties
- 📞 **Contact Owners** - Direct communication with property owners
- ✅ **Verified Properties** - 100% legally verified listings
- 📱 **User-Friendly UI** - Modern Jetpack Compose interface
- 🌙 **Dark Mode Support** - Full dark theme support

## Tech Stack

- **Language**: Kotlin
- **UI Framework**: Jetpack Compose
- **Networking**: Retrofit2 + OkHttp
- **Dependency Injection**: Koin
- **Asynchronous Programming**: Kotlin Coroutines
- **Image Loading**: Coil
- **Local Database**: Room
- **Navigation**: Jetpack Navigation Compose

## Project Structure

```
app/
├── src/main/
│   ├── java/com/grihobazar/android/
│   │   ├── data/
│   │   │   ├── api/           # API service interfaces
│   │   │   ├── models/        # Data models
│   │   │   └── repository/    # Data repositories
│   │   ├── ui/
│   │   │   ├── screens/       # Screen composables
│   │   │   ├── components/    # Reusable UI components
│   │   │   └── theme/         # Theme configuration
│   │   ├── viewmodel/         # ViewModels for state management
│   │   └── MainActivity.kt
│   └── AndroidManifest.xml
└── build.gradle.kts
```

## Getting Started

### Prerequisites
- Android Studio (latest version)
- JDK 8 or higher
- Android SDK 24+

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Kaustabhmis/grihobazar-android.git
cd grihobazar-android
```

2. Open the project in Android Studio

3. Build and run:
```bash
./gradlew build
./gradlew installDebug
```

## Configuration

### API Configuration
Create a `local.properties` file in the project root:
```properties
BASE_URL=https://api.grihobazar.in/
```

### Environment Variables
- `BASE_URL`: Backend API base URL
- `API_KEY`: API authentication key (if required)

## Development Guidelines

### Naming Conventions
- **Composables**: PascalCase (e.g., `PropertyCard.kt`)
- **Functions**: camelCase (e.g., `getProperties()`)
- **Constants**: UPPER_SNAKE_CASE (e.g., `BASE_URL`)

### Code Style
- Follow Kotlin style guide
- Use coroutines for async operations
- Implement proper error handling
- Write unit tests for business logic

## API Integration

The app communicates with the Grihobazar backend API. Key endpoints:

- `GET /api/properties` - Get properties list
- `GET /api/properties/{id}` - Get property details
- `POST /api/properties` - Create new listing
- `PUT /api/properties/{id}` - Update property
- `DELETE /api/properties/{id}` - Delete property

## Future Enhancements

- [ ] User authentication & profiles
- [ ] Property listing creation
- [ ] Payment integration
- [ ] Real-time notifications
- [ ] Map integration
- [ ] Video tours
- [ ] Social sharing
- [ ] Chatbot support

## Contributing

Contributions are welcome! Please follow these steps:

1. Create a feature branch (`git checkout -b feature/amazing-feature`)
2. Commit your changes (`git commit -m 'Add amazing feature'`)
3. Push to the branch (`git push origin feature/amazing-feature`)
4. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For issues and feature requests, please create an issue on the [GitHub repository](https://github.com/Kaustabhmis/grihobazar-android/issues).

## Contact

- Website: https://www.grihobazar.in
- Email: support@grihobazar.in

---

Made with ❤️ by Kaustabhmis
