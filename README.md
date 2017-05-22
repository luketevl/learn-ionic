# learn-ionic1
Learn about Ionic 1

# LINK
- https://ionicframework.com
- https://apps.ionic.io/login


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

# PUBLISH APP
- Upload to apps ionic | to see is required use **ionic view**
```shell
ionic upload 
```
- Send to email link
```shell
ionic share email@email.com
```

# IONIC COMMANDS
- **Add** _plataform_ 
```shell
ionic plataforms add android|ios
```
- **BUILD** app
```shell
ionic build android|ios
```
- **Run** build
```shell
ionic run android --device
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

# PLUGINS 
- **Camera**




# COMPONENTS
- **List**
```html
<ion-list>
  <ion-item>Content</ion-item>
</ion-list>
```
- **Menu**
```html
<ion-side-menus>
  <ion-side-menu-content>
    <ion-nav-bar>
      <ion-nav-buttons>
      </ion-nav-buttons>
    </ion-nav-bar>
    <ion-nav-view name="menuContent">
    </ion-nav-view>
  </ion-side-menu-content>
  <ion-side-menu>
    <ion-content>
    </ion-content>
  </ion-side-menu>
</ion-side-menus>
```

# Route 
- **Abstract** route
  - set **abstract** _true_
```javascript
$stateProvider.state('app', {
  url: '/app',
  templateUrl: 'templates/menu.html',
  abstract: true
})

.state('app.list', {
  url: '/list',
  views: {
    'menuContent': {
      templateUrl,
      controller
  }
  }
})
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
- Publish your app for test in https://apps.ionic.io/login | to see is required use **ionic view**
- In **abstract** _routes_ you hae change other routes
-  **BUILD** in **ios** only works in **MAC**, use xcode
  - open xcode and _assign_ app
  - Open the preferences in your iphone and added developer

