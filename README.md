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

We Solve this Challeng with a way that on it, we get a list from server that includes `( for example: 100 )` images url

at the next step we show `( for example: 15 )` images at the website and download other images to cache them at the memory
like stack that it's capacity is `100` images

it's mean that if you scroll up at the site, you just have last serie of images that got from server,
if your scroll is long, you have to download again image and cache them

```javaScript

    const [data, setData] = useState([]);
    const [index, setIndex] = useState(30);

    // =================================================================

    const image_list = [
        "http://movista.ir/image/x0bsgEeWqpvH8Lgwgmzi2tujlrV.jpg",
        "http://movista.ir/image/nS3nhUZUSY8dWEsRmKILfiOC3F0.jpg",
        "http://movista.ir/image/urb5Wf4yffJQ2KwAuSPxCbOM8HA.jpg",
        "http://movista.ir/image/1YtsND7vSNymylnOSzgg3DdVFMB.jpg",
        "http://movista.ir/image/iB64vpL3dIObOtMZgX3RqdVdQDc.jpg",
        "http://movista.ir/image/8fUEFPUTF7kBMuKPiSQHxPvd8EZ.jpg",
        "http://movista.ir/image/39wmItIWsg5sZMyRUHLkWBcuVCM.jpg",
    ];


    useEffect(() => {
        const temp = [];
        image_list.map((item) =>
            temp.push(
                <div className={styles.thingCard}>
                    <img alt="" src={item} width={"100%"} height={"100%"} />
                </div>
            )
        );
        setData(temp);
    }, []);

```

---

### 2. Designer:

---

### 3. Type of Connection:

Alright, we decide to use both of SignalR and RestFull Connection in project

-> use SignalR for `Chat` and `Notification` and component to be realtime

-> use RestFull for `All Connection except component that use SignalR`

---

### 4. SignalR using Structure:

Structure and class of SignalR is in `src/Connection/SignalRConnectionServer.js`
