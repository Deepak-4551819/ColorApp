# Drive Link :- https://drive.google.com/file/d/1fEJ0POOuJM9SRKvgfzcf5SrXaBreaU1a/view?usp=sharing
Download and try
# ColorApp

This is a Kotlin-based Android application that helps you manage a collection of colors by storing them in a local database and synchronizing them with Firebase Realtime Database. The app follows the MVVM (Model-View-ViewModel) architecture and leverages Jetpack Compose for a modern UI experience.


# Features
- Add Colors: Generate random colors with metadata and save them locally.
- View Colors: Display saved colors in a grid layout with attractive cards.
- Sync Colors: Synchronize unsynced colors with Firebase Realtime Database.
- Track Pending Syncs: Keep track of unsynced colors with a count displayed in the app's top bar.

# Project Structure
com.colorapp
├── data/
│   ├── firebase/
│   │   └── FirebaseService.kt
│   ├── local/
│   │   ├── AppDatabase.kt
│   │   └── ColorDao.kt
│   └── repository/
│       └── ColorRepositoryImpl.kt
├── domain/
│   ├── model/
│   │   └── ColorEntity.kt
│   ├── repository/
│       └── ColorRepository.kt
├── presentation/
│   ├── components/
│   │   ├── ColorCard.kt
│   │   └── IconCard.kt
│   ├── pages/
│   │   ├── ColorGrid.kt
│   │   └── ColorApp.kt
│   └── viewmodel/
│       ├── ColorViewModel.kt
│       └── ColorViewModelFactory.kt
└── MainActivity.kt

## Key Layers

1. # Data Layer (data/)
firebase/FirebaseService.kt: Manages interactions with Firebase Realtime Database.
local/: Contains the Room database (AppDatabase) and DAO (ColorDao) for local data storage.
repository/ColorRepositoryImpl.kt: Implements the repository interface for data operations, including syncing with Firebase.

2. # Domain Layer (domain/)
model/ColorEntity.kt: Defines the data model for a color entity.
repository/ColorRepository.kt: Declares an interface for the repository to abstract data operations.

3. # Presentation Layer (presentation/)
components/: Reusable UI components, such as ColorCard and IconCard.
pages/: Composable screens, including the main app layout and the grid of colors.
viewmodel/: Manages UI state and business logic, including ColorViewModel and its factory (ColorViewModelFactory).

## How to Use
1.Add Colors: Use the "Add Color" button to generate a random color and save it locally.
2.View Colors: Colors appear as cards in a grid view.
3.Sync Colors: Click the sync icon to synchronize pending colors with Firebase.
4.Monitor Pending Syncs: The sync button displays the number of unsynced colors.

