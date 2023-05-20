# Document of "Amir Decore -> Admin Panel" project

## Directories descriptions:

1. Public -> All assets File and index.html is in this directory

2. Src -> Main Files are in this directory

## Folders in Src Directory descriptions:

1. Components -> This directory includes all section of project that reapeted to use.

2. Connection -> This directory includes `SignalR` and `Restfull` WebConnection class and method for connect to server.

3. Container -> This directory includes `Layouts` and `Routing` of project.

4. Context -> This directory includes all `Context API` that there is in project.

5. Page -> This directory includes all files that show as a page with a route in project.

6. Styles -> This directory includes all `*.module.css` files that use in project.

7. Utils -> This directory includes all files that help us in project, but aren't very important for develop.

## Rule for File Naming in project:

1. JSX -> files that user can see those at the website like `Header`, `Footer`, `AboutUs` and ect ...

2. JS -> files that user can't see those but use them like `App.js`, `index.js`, `Authenticated.js` and ect ...

## Package Managers in project:

1. NPM

2. YARN

## challenges of the project that we have to solve them:

### 1. Image Cache:



***

### 2. Designer:

***

### 3. Type of Connection:

Alright, we decide to use both of SignalR and RestFull Connection in project

-> use SignalR for `Chat` and `Notification` and component to be realtime

-> use RestFull for `All Connection except component that use SignalR`

***

### 4. SignalR using Structure:

Structure and class of SignalR is in `src/Connection/SignalRConnectionServer.js`
