<h1 align="center">
Darktop
</h1>
<p align="center">
Convert Website to Desktop application
</p>

## System requirements
To get started, you must first install `nodejs` on your system. A package manager like `npm` is also required.
- [nodejs](https://nodejs.org)
- [npm](https://www.npmjs.com)
- [git](https://git-scm.com)

To output the rpm file you need to install its module in the system, otherwise delete its value. Below is the command to install rpm in Ubuntu:
```bash
sudo apt install rpm
```


## Installation

To install and run this project, follow these steps:

1. Clone the repository:

```bash
git clone https://github.com/ReactMVC/Darktop.git
```

2. Navigate into the project directory:

```bash
cd Darktop
```

3. Install the dependencies:

```bash
npm install
```

4. Start app

```bash
npm start
```

## Build the Application for platforms

To build the Windows platform:
```bash
npm run build-w
```
To build the Linux platform:
```bash
npm run build-l
```

Built output applications are located in the newly created directory called “dist” which is inside your application directory.

## Documentation
Now is the time to look at the change guide and make your job easier. Please follow us and give this project a star.

### Change application URL
On your project folder, open config.js file and change `websiteUrl` value:
```javascript
// Main Application URL
'websiteUrl' : 'https://github.com',
```

### Change application Name
First, you need to change the name attribute of the package.json file in the application root directory.
```javascript
"name": "Darktop",
```
Next, modify config.js file appName value.
```javascript
'appName' : 'Darktop',
```

### Change application description
First you need to change the application root directory package.json description attribute.
```javascript
"description": "Convert Website to a Desktop application",
```

### Application Icon change
All application Icons are located in the build folder. Replace images using the same name.
- Windows - Optional icon.ico (Windows app icon) or icon.png. Icon size should be at least 256x256.
- Linux - Linux icon sets will be generated automatically based on the macOS icons file or common icon.png.

### Customize the main/right menu
There are two menu types
- Main application menu – menu-config.js
- Right menu – right-menu-config.js


### Hide website elements
Give a native look to your application. You can hide your website elements as you prefer. To do this, open config.js file.
Next, you can add your class or id value separated by comma.

#### Hide elements by ID
```javascript
'hideElementsId' : ['id_1', 'id_2', 'id_3'],
```

#### Hide elements by Class
```javascript
'hideElementsClass' : ['class_1', 'class_2', 'class_3'],
```

### Edit Application Website Info
you need to change the repository attribute of the package.json file in the application root directory.
```json
"repository": {
    "type": "git",
    "url": "git+https://github.com/ReactMVC/Darktop.git"
}
```

### Build Info
you need to change the build info of the package.json file in the application root directory.
```json
"build": {
    "appId": "com.darktop.app",
    "productName": "Darktop",
    "artifactName": "darktop-${version}-${arch}.${ext}",
    "asar": true,
    "copyright": "Copyright © 2023 Hossein Pira",
    "generateUpdatesFilesForAllChannels": true,
    "detectUpdateChannel": true,
    "npmRebuild": true,
    "buildDependenciesFromSource": false,
    "afterSign": "electron-builder-notarize",
    "win": {
      "target": [
        "zip",
        "nsis"
      ],
      "icon": "build/icon.ico"
    },
    "linux": {
      "category": "Utility",
      "target": [
        {
          "target": "deb",
          "arch": [
            "x64"
          ]
        },
        {
          "target": "tar.gz",
          "arch": [
            "x64"
          ]
        },
        {
          "target": "AppImage",
          "arch": [
            "x64"
          ]
        },
        {
          "target": "rpm",
          "arch": [
            "x64"
          ]
        }
      ],
      "vendor": "Hossein Pira",
      "synopsis": "Convert Website to Desktop application",
      "artifactName": "darktop-linux-${version}-${arch}.${ext}",
      "icon": "build/icon.png"
    },
    "nsis": {
      "oneClick": false,
      "perMachine": true,
      "installerIcon": "build/icon.ico",
      "uninstallerIcon": "build/icon.ico",
      "artifactName": "darktop-setup.${ext}",
      "shortcutName": "TCI"
    }
}
```
### Linux Apps Categories
| Main Category | Description                                         | Notes                                                 |
| ------------- | --------------------------------------------------- | ----------------------------------------------------- |
| AudioVideo    | Application for presenting, creating, or processing multimedia (audio/video) |                                                       |
| Audio         | An audio application                                 | Desktop entry must include AudioVideo as well         |
| Video         | A video application                                 | Desktop entry must include AudioVideo as well         |
| Development   | An application for development                      |                                                       |
| Education     | Educational software                                |                                                       |
| Game          | A game                                              |                                                       |
| Graphics      | Application for viewing, creating, or processing graphics |                                                       |
| Network       | Network application such as a web browser            |                                                       |
| Office        | An office type application                           |                                                       |
| Science       | Scientific software                                 |                                                       |
| Settings      | Settings applications                               | Entries may appear in a separate menu or as part of a "Control Center" |
| System        | System application, "System Tools" such as say a log viewer or network monitor |                                                       |
| Utility       | Small utility application, "Accessories"              |                                                       |

## Developer Contact

For any queries or suggestions, you can reach out to the developer:

- Name: Hossein Pira
- Email: h3dev.pira@gmail.com
- Telegram: [@h3dev](https://t.me/h3dev)

## License

This project is licensed under the MIT License.
