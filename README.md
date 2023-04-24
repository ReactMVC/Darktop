<h1 align="center">
Darktop
</h1>
<p align="center">
Convert Website to Desktop application
</p>
<hr>
<div align="center">
<h3>Developer <a href="https://t.me/h3dev">Hossein Pira</a></h3>
</div>
<br>
<h2>Installation</h2>

You must install Node.js and clone the project:  

```
git clone https://github.com/ReactMVC/Darktop.git
```

Then install the requirements by running:
```bash
npm install
```
And for running it, you can enter this command:
 ```bash
npm start
```

# Build the Application for platforms
First you need to install electron-builder package globally :
```bash
$ npm i electron-builder -g
```
To build all platform :
```bash
$ electron-builder -mwl
```
To build the macOS platform:
```bash
$ electron-builder --mac
```
To build the Windows platform:
```bash
$ electron-builder --win
```
To build the Linux platform:
```bash
$ electron-builder --linux
```

Built output applications are located in the newly created directory called “dist” which is inside your application directory.

# Documentation
Now is the time to look at the change guide and make your job easier. Please follow us and give this project a star.

# Change application URL
On your project folder, open config.js file and change `websiteUrl` value:
```javascript
// Main Application URL
'websiteUrl' : 'https://github.com',
```

# Change application Name
First, you need to change the name attribute of the package.json file in the application root directory.
```javascript
"name": "Darktop",
```
Next, modify config.js file appName value.
```javascript
'appName' : 'Darktop',
```

# Change application description
First you need to change the application root directory package.json description attribute.
```javascript
"description": "Convert Website to a Desktop application",
```

# Application Icon change
All application Icons are located in the build folder. Replace images using the same name.
```bash
macOS
Optional icon.icns (macOS app icon) or icon.png. Icon size should be at least 512x512.
```
```bash
Windows
Optional icon.ico (Windows app icon) or icon.png. Icon size should be at least 256x256.
```
```bash
Linux
Linux icon sets will be generated automatically based on the macOS icons file or common icon.png.
```

# Customize the main/right menu
There are two menu types
```bash
Main application menu – menu-config.js
```
```bash
Right menu – right-menu-config.js
```


# Hide website elements
Give a native look to your application. You can hide your website elements as you prefer. To do this, open config.js file.
Next, you can add your class or id value separated by comma.

# Hide elements by ID
```javascript
'hideElementsId' : ['id_1', 'id_2', 'id_3'],
```

# Hide elements by Class
```javascript
'hideElementsClass' : ['class_1', 'class_2', 'class_3'],
```
