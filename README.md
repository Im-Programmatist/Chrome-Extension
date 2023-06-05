## 5 Major Components to Building a Chrome Extension

### 1. The manifest file 
**It is registry for chrome extension and it has extension details like name description, permission needed etc**
**we define where our background, popup, and options components are located in our file directory.**
**We can defined foreground location file in manifest as well as programmatically add it in extension code**
**APIs that let us do things like store data locally and host permissions which tell the browser which urls your Chrome extension is allowed to interact with.**

### 2. TheThe background script.
**This is a JavaScript file like the mainframe or hub of a Chrome extension. It is like a back-end environment**

### 3. The popup page.
**This is an HTML page users see when they click on the extension icon in the menu bar. with this users can interact with your extension--like a front-end.**

### 4. The options page.
**ANother HTML page that user sees this page when they right click on your extension icon and choose for the options like a front-end.**

### 5. The foreground/content script.
**This file is a JavaScript script.It is special case js file attach to website/extension to work on concept.**

## Service Worker In Javascript
1. A service worker is a script that runs independently in the browser background. 
2. It can intercept its network requests and can manage/manipulate request and response and respond to frontend.
3. Service workers mainly serve features like background sync, push notifications and they are commonly used to set offline data at first time so that user can focus on UI/UX in applications
4. AppCache helps to serve offline experience feature. 
5. Service worker mostly uses Promises in js
6. These services are programmable network proxy, it can call and fetch data from server and respond to frontend. Also can change request & it's response made by user from frontend.
7. Life cycle of services are different from normal webpage, We only terminated when it’s not used and restarted when it’s next needed.
8. Service worker get installed and cache some website pages, if pages are getting cached then worker installed successfully.
9. Service worker typically deleted old cache and replace new cache during it's installation/reinstallation.
10. Prerequisites :
    - 10.1 HTTPS unless on localhost:
        - Service workers require the use of HTTPS connection.
        - The workers does work under the localhost server.
    - 10.2 Browser support: 
        - Service Workers are highly supported over the internet by Chrome, Firefox, Opera, Safari and Edge, which makes them worthy for deployment.
11. Before installation of service worker we need to register this worker with windows navigator(with 'load' event listener), once it get register then browser will install it in background.
12. After registration service worker file install sw(with 'install' addEventListener) where it fetch your(browsers) cache assets, it opens cache and cache the assets of website then confirm it. 
13. Once installation and cache open with caching assets happens, we have to activate it.(with Activate Event addEventListener('activate'))
14. Once the service worker is set up, it should start to interact and use the cached responses. when user navigates through the web pages, the service worker begins to receive fetch events.
15. Service Worker can NOT access the parent object, windows object, Document object & DOM
16. Service worker can access cache assets & API calls(can intercepts request/response), COntrol network traffic & store application cache
17. Service worker Commonly used for offline-optimized experience, send push notification, and background sync.

