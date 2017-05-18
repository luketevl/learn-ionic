# learn-ionic1
Learn about Ionic 1

# LINK
- https://ionicframework.com

# ABOUT
- Hybrid Mobile Framework
- Use **angular**

# INSTALL
- Run the command to INSTALL
```shell
  npm install -g cordova ionic
```

# CREATE APP
- Create **app**
  - modelName
    - **blank**
    - **tabs**
    - **sidemenu**
```shell
ionic start appName modelName
```

# INIT SERVER
- Start the **web server**
```shell
ionic serve
```
- Start **lab mode** | Show ios and android views
```shell
ionic serve --lab
```

# STRUCTURE
- Folders
  - **www** | Have all files to create


# VIEWS
- Create view
  - **>ion-view** is **required**, if you don't use this the elements on elements
```html
<ion-view>
</ion-view>
```

- Create **back button** for transitions
```html
<ion-nav-back-button></ion-nav-back-button>
```

# CLASSES

# COMPONENTS
- **List**
```html
<ion-list>
  <ion-item>Content</ion-item>
</ion-list>
```

# OBSERVATIONS
- To **show** HTML is **required** **CONTENT TAG**
```html
<ion-header-bar></icon-header-bar>
<ion-content></ion-content>
<ion-footer-bar></icon-footer-bar>
```
- When create **ANGULAR CONTROLLER** view **module** _name_ in **index.html(ng-app)** or **js/app.js**
- Use **ion-nav-view** and **routes** to create transitions views
```html
<ion-nav-view>
  <ion-nav-bar>
    <ion-nav-back-button></ion-nav-back-button>
  </ion-nav-bar>
</ion-nav-view>
```
