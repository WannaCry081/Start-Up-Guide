# Flutter Environment Setup

## Flutter Configuration

### 📦 Flutter Packages Used

| Development Tools Used | | |
|------------------------|-|-|
| flutter | google_fonts | flutter_svg | 
| flutter_spinkit | provider | shared_preferences |
| flutter_staggered_animations | shimmer_animations | flutter_hive |

### 🛠 Flutter Environment Setup

Follow the steps below to get your Flutter environment up and running with some of the best packages I've come to rely on over the years:

1. `Initialize Your Flutter Project` - Kickstart your Flutter project using the commands below:

```powershell
$ flutter create project_name
cd project_name

# Launch your Flutter app to ensure everything is set up correctly
$ flutter run
```

2. `Install Essential Packages` -
Incorporate a curated set of packages that have proven indispensable in my development journey:

```powershell
$ flutter pub add google_fonts flutter_svg flutter_spinkit provider shared_preferences flutter_staggered_animations shimmer_animations
```

3. `Adopt the MVVM Folder Structure` - 
Ensure to organize your files and folders in line with the Model-View-ViewModel (MVVM) architectural pattern. Adhering to this structure not only aids in readability but also enhances maintainability. 

### 📂 Flutter Folder and File Structure

I've meticulously organized my directories and files in line with the Model-View-ViewModel (MVVM) architecture, a prominent design pattern embraced by the mobile development fraternity. This organization ensures a separation of concerns, enhancing readability and scalability while aligning with best practices in modern mobile development.

```powershell
📁 project_name
│
├── 📁 android
├── 📁 assets
├── 📁 build
├── 📁 lib
│   │
│   ├── 📁 core
│   │   ├── 📁 constants
│   │   └── 📁 services
│   │
│   ├── 📁 models
│   ├── 📁 providers
│   ├── 📁 utils
│   ├── 📁 viewmodels
│   ├── 📁 views
│   │   ├── 📁 home
│   │   ├── 📁 login
│   │   └── 📁 signup
│   │
│   ├── 📁 widgets
│   ├── 📄 main.dart
│   └── 📄 routes.dart
│
├── 📁 test
├── 📄 pubspec.yaml
└── 📄 README.md
```

---