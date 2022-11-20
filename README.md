# WinRar Password: kol2233

# Fortnite External
Fortnite external cheat by Vaseliinikives & Joona70

fuck all the skids who still calls this oracle, we made this somewhere near september-october 2019.
uses socket driver. (detected now.)

you must update offsets and change driver to make this working & undetected.

original thread of this cheat: https://www.unknowncheats.me/forum/fortnite/355924-fortnite-free-esp.html

updated version with fixed w2s & new driver: https://www.unknowncheats.me/forum/fortnite/369607-fortnite-free-esp-aimbot.html

source of the updated version with fixed w2s & new driver: https://github.com/Joona70/fortnite-cheat-source-public

# memenite AIO - Please leave a star ⭐
## Fortnite Anti-cheat Bruteforcer, HWID Spoofer, Cleaner, Hardware Serials checker, Cheat x2, FOV Changer
### ElitePVP - https://www.elitepvpers.com/forum/fortnite-hacks-bots-cheats-exploits/4713716-release-free-ac-forcer-spoofer-serial-checker-cleaner.html#post37952599
### VirusTotal (False Positives) - https://www.virustotal.com/gui/file/e7cf7ff9ea09f7c3113727198af276a57e5ff44fbf68c4af593e266e6aeab8bd/detection
#### Changelog
> Fixed driver not mapping due to wrong location set. Credits: @HighGamer.

> Fixed BattlEye forcing

> Added another cheat

> Added FOV Changer

> [ 2/3/2020 ]

> Bug fixes

![memenite](https://i.imgur.com/7oxYjUA.png)

This tool is completely free and opensource.
Why batch? It works. It's user friendly, convenient, easy for anyone to learn, edit and make improvements. 

### Using:

- Drag main folder to Desktop
- Run 'Run me.bat'
- Select choice

### Menu:
![memenite](https://i.snipboard.io/kn9Plm.jpg)

### Features:
- Fortnite Anti-cheat Bruteforcer ✔️
- HWID Spoofer ✔️
- Cleaner ✔️
- Hardware Serials checker ✔️
- Fortnite Cheat ✔️
- Fortnite FOV Changer ✔️

### Credits: OverHax, KDMapper.


# Fortnite API

A simple to use package for interacting with Fortnite API.

## Install

```
$ go get github.com/jryd/fortnite
```

## API

### FIRST THINGS FIRST

To access the Fortnite API, you need to have an account on Epic Games. After that you need to get 2 headers that your client uses to access Fortnite.

You can get these headers by using a tool to capture incoming and outgoing HTTP traffic. The steps below are for the Fiddler tool that I used.

*   Install & Open Fiddler
*   In Tools -> Options -> HTTPS, Select Capture HTTPS Connects
*   After that start the Epic Games launcher
*   You will see a request with _/account/api/oauth/token_. Click on it -> Click Inspectors to view the headers (you want to grab the long string in the Authorization header, without the basic part - i.e header is basic abcd... you only need the abcd... bit) => **This header is your Client Launcher Token**
*   Launch Fortnite
*   You will see again a request with _/account/api/oauth/token_. Click on it -> Click Inspectors to view the headers (you want to grab the long string in the Authorization header, without the basic part - i.e header is basic abcd... you only need the abcd... bit) => **This header is your Fortnite Client Token**

---

### USAGE

```go
fortniteClient := fortnite.NewClient("email address", "password", "client launcher token", "fortnite client token")
```

---

### METHODS

```go
fortniteClient.Login()

fortniteClient.Lookup("jryd")
fortniteClient.CheckPlayer("jryd")
fortniteClient.GetStatsBR("jryd", "pc")
fortniteClient.GetStatsBRFromID("12345", "pc")
fortniteClient.GetFortniteNews()
fortniteClient.CheckFortniteStatus()
fortniteClient.GetFortnitePVEInfo("en")
fortniteClient.GetStore("en")

fortniteClient.KillSession()
```

More information on the mentods can be found in the [GoDoc](https://godoc.org/github.com/jryd/fortnite).
[![LICENCE](https://img.shields.io/github/license/Ileriayo/markdown-badges?style=for-the-badge)](./LICENSE)
[![TYPESCRIPT](https://img.shields.io/badge/typescript-%23007ACC.svg?&style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![JAVASCRIPT](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![NODEJS](https://img.shields.io/badge/node.js-%2343853D.svg?&style=for-the-badge&logo=node.js&logoColor=white)](https://www.nodejs.org)
[![DISCORD0](https://img.shields.io/badge/Discord%20Server-%237289DA.svg?&style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/b2H6EGAmdQ)\
[![NPM](https://nodei.co/npm/unreal.js.png)](https://npmjs.com/package/unreal.js)

![LOGO_0](https://media.discordapp.net/attachments/833965731279929365/853716847203844106/image0.png)

# unreal.js

## A pak reader for games like [VALORANT](https://playvalorant.com) & [Fortnite](https://fortnite.com) written in Node.JS

### Notice

This library is in VERY early development so it might be unstable. **Please also keep in mind that JavaScript is not
really made for this kind of stuff so the usage of this library is experimental**. We still try fixing most issues
though so report if you experience any!\

### Features

- Easy2use file provider for fast interaction with pak/asset files
- Supports loading of UE4 pak files
- Supports loading of UE4 asset files (.uasset, .umap, .uexp, .ubulk)
- Supports loading of .locres files
- Supports loading of AssetRegistry.bin
- Supports exporting of UE4 textures as image
- Supports exporting of UE4 sounds files

### Prerequisites

- Node.JS/NPM installed
- **Experience with JavaScript or TypeScript**
- Python, Visual C++ Build Tools (node-gyp dependencies)

### Installation

`npm i unreal.js`\
This library has optional dependencies like `canvas` and `dxt-js` which are used in ue4 texture conversion. If you don't
want to install these dependencies, use: `npm i unreal.js --no-optional`.

### Documentation

[Here](https://unreal.js.org)

### Usage

#### Basics: FileProvider

The file provider is basically the heart of the library and from there you control basically all features.

**IMPORTANT**: When using the library with **Fortnite V14.40 and above**, you need `oo9core_8_win64.dll` present in your
working directory (you can download it using `Oodle.downloadDLL()`). You will also need
a [.usmap mappings](https://benbot.app/api/v1/mappings) file corresponding to your fortnite version.\
You will also experience longer mounting times than e.g VALORANT.

- **Usage with Fortnite**
    ```js
    // Create new instance
    const usmap = new UsmapTypeMappingsProvider(readFileSync("USMAPPATH"))
    const provider = new FileProvider("GAMEPATH", VERSION, usmap)
    provider.mappingsProvider.reload() // Loads .usmap
    // Setting this to '0' will skip reading directory index
    // Means it will not populate .utoc file entries, so <FIoStoreReader>.getFiles() will be empty
    // Leaving it to default value will slightly increase pak mounting time
    provider.ioStoreTocReadOptions = 0
    // 'start' the provider
    await provider.initialize()
    // submit aes key to decrypt paks
    await provider.submitKey(FGuid.mainGuid, "KEY")
    ```
  Replace:
    - `USMAPPATH`: Path to your .usmap file (doesn't need to be in working dir)
    - `VERSION`: Version you want to use (e.g `Ue4Version.GAME_UE4_26`, pass `null` for latest)
    - `GAMEPATH`: Path to fortnite's paks
    - `KEY`: An [aes key](https://benbot.app/api/v1/aes) corresponding to your version


- **Usage with VALORANT**
   ```js
    // Create new instance 
    const provider = new FileProvider("GAMEPATH", Ue4Version.GAME_VALORANT)
    // 'start' the provider
    await provider.initialize()
    // submit aes key to decrypt paks
    await provider.submitKey(FGuid.mainGuid, "0x4BE71AF2459CF83899EC9DC2CB60E22AC4B3047E0211034BBABE9D174C069DD6")
   ```
  Replace:
    - `GAMEPATH`: Path to valorant's paks

#### Basics: Loading an asset

- **Loading whole file**
  ```js
   const pkg = provider.loadGameFile("PATH") // loads the file
   console.log(pkg.toJson()) // turns file into json format
  ```
  Replace:
    - `PATH`: Path to the file you want to load


- **Loading specific object from file**
  ```js
  const obj = provider.loadObject("PATH", "OBJECTNAME") // loads the object
  console.log(pkg.toJson()) // turns object into json format
  ```
  Replace:
    - `PATH`: Path to the file you want to load
    - `OBJECTNAME`: Name of the object to load\
      You can leave this parameter out if you provide the object name as file extension

#### Basics: Exporting sounds

- **Exporting a sound wave**
  ```js
  // this will find an export which matches the class 'USoundWave'
  const sound = pkg.getExportOfType(USoundWave)
  // use 'pkg.getExportOfTypeOrNull(USoundWave)' if you check for undefined/null manually
  const wave = SoundWave.convert(sound) // converts USoundWave to a usable file
  // write it to a file
  writeFileSync(`MySoundFile.${wave.format}`, wave.data)
  ```


- **Exporting wwise audio (VALORANT)**
  ```js
  // this will find an export which matches the class 'UAkMediaAssetData'
  const mediaData = pkg.getExportOfType(UAkMediaAssetData)
  const wwise = WwiseAudio.convert(mediaData) // Converts it to a .wem file
  // write it to a file
  writeFileSync(`MySoundFile.${wwise.format}`, wwise.data)
  ```
  **IMPORTANT**: `.wem` are not playable by windows, you have to convert it to a `.wav` file first!\
  Unreal.JS is able to do that with [vgmstream](https://github.com/vgmstream/vgmstream). Download the zip file
  from [here](https://drive.google.com/file/d/1Fed4ba_FvegUgeIXCgnlcoUzoABC-ZxX/view?usp=sharing), create a folder
  called 'vgm' in your working directory and extract all files into it. Then do:
  ```js
  // this will find an export which matches the class 'UAkMediaAssetData'
  const mediaData = pkg.getExportOfType(UAkMediaAssetData)
  const wwise = WwiseAudio.convert(mediaData) // Converts it to a .wem file
  // converts and exports it as playable .wav file
  wwise.export() // you can pass an output path (must include whole path with filename and extension)
  ```

#### Basics: Exporting textures

```js
  // this will find an export which matches the class 'UTexture2D'
  const tex = pkg.getExportOfType(UTexture2D)
  // use 'pkg.getExportOfTypeOrNull(UTexture2D)' if you check for undefined/null manually
  const image = Image.convert(tex) // converts texture to image (import Image class from unreal.js)
  // writes it it a file
  writeFileSync("image.png", image)
  ```

#### Basics: Loading locres

- **Loading by file path**
   ```js
   const locres = provider.loadLocres("PATH") // loads the locres file
   console.log(locres.toJson()) // turns locres into json format 
   ```
  Replace:
    - `PATH`: Path to the .locres file


- **Loading by enum**
  ```js
  const locres = provider.loadLocres(FnLanguage.DE) // loads using enum
  console.log(locres.toJson()) // turns locres into json format 
  ```  

#### Advanced: Loading a pak file manually

```js
const reader = new PakFileReader("PATH", GAME) // Create a new instance
reader.aesKey = "KEY" // Set an aes key (can be left out if pak is not encrypted)
reader.readIndex() // Read the index
reader.extract(reader.files.first()) // Gets the first file and extracts it as Buffer
```

Replace:

- `PATH`: Path to the pak file
- `GAME`: Game version you are using (e.g `Ue4Version.GAME_UE4_26`)\
  You can leave it out if you want to use the latest version
- `KEY`: Aes key used for decrypting the pak\
  **WARNING** Using a wrong aes key will throw an exception! You can use `reader.testAesKey("KEY")` to test if it
  works (returns a boolean)

#### Advanced: Loading a package manually

```js
// load a pak package (e.g valorant)
const pkg = new PakPackage(UASSETBUFFER, UEXPBUFFER, UBULKBUFFER, NAME, PROVIDER, GAME)
// load an io package (mostly used in fortnite)
const pkg2 = new IoPackage(UASSETBUFFER, PACKAGEID, STOREENTRY, GLOBALPACKAGESTORE, PROVIDER, GAME)
```

Replace:

- `UASSETBUFFER`: Buffer of the .uasset file
- `UEXPBUFFER`: Buffer of the .uexp file
- `UBULKBUFFER`: Buffer of the .ubulk file (pass `null` if it doesn't exist)
- `NAME`: Name of the package
- `PROVIDER`: Instance of a fileprovider (optional in `PakPackage`)
- `GAME`: Version of the game you are using (e.g `Ue4Version.GAME_VALORANT`, optional in both)
- `PACKAGEID`: The id of the io package
- `STOREENTRY`: Instance of the io package's `FPackageStoreEntry`
- `GLOBALPACKAGESTORE`: The file provider's `FPackageStore` object

## Support, Feedback, Contact

- Discord: **MarcelWRLD#4682**
- Twitter: **Sprayxe_**

## Inspiration

- [JFortniteParse](https://github.com/FabianFG/JFortniteParse)
- [CUE4Parse](https://github.com/FabianFG/CUE4Parse)

![LOGO_1](https://media.discordapp.net/attachments/833965731279929365/853716847430074368/image1.png)

# pynite
An async python wrapper for the Fortnite API.

#### Installation
Type this into your console:
```
pip install pynite
```
If you come across an unknown error or bug, please [open an issue](https://github.com/cree-py/pynite/issues/new).

#### Documentation
Documentation is in progress! If you would like to contribute, let us know by joining our [discord server](https://discord.gg/RzsYQ9f). Current docs are in the [docs folder](https://github.com/cree-py/pynite/tree/master/docs) of this repository. Start out with [intro.md](https://github.com/cree-py/pynite/blob/master/docs/intro.md)

#### Misc
This is an async python wrapper for the Fortnite API. If you would like to help, just let us know in our [discord server](https://discord.gg/RzsYQ9f)!

# FortniteAdvESPupdate
FortniteAdvESP

without aimbot http://www72.zippyshare.com/v/jHQX8nH8/file.html 

FortHook + BattleEyeFix 13.10.17
http://www20.zippyshare.com/v/tY2UDlrf/file.html

exclude NOEYE.exe fromn antivirus! (fucks drivers AV dont like that)
Start NOEyE.exe
Start Fortnite
Start fav injector (extreme / xenos)
Inject fav hack.dll
win


Features:
- Aimbot
- Chams
- Item and enemy ESP
- Teleport

Press *V* to Telepick up weapons
Press *B* to Telepick up ammo
Press *F7* to toggle the aimbot.
Press *F8* to toggle the chams.
Press *F9* to toggle ESP.
Press *XBUTTON1* to aimbot aim
Press *XBUTTON2* to toggle advanced ESP.
CHANGE IN CONGIG.h
https://msdn.microsoft.com/de-de/library/windows/desktop/dd375731(v=vs.85).aspx

Compile in release x64 if you just want to use it.





Original code by zoomy500
Credits to NSeven, TJ888, and UMO

Additional contributions from: NewbieH4x, Randshot, xzyxzy

updated by Snoopy

# Winrar password: fiji009

# FORTNITE RAGE CHEAT 
 
### LATEST UPDATE 01-23-2022 🗓

# offsets & Sigs Outdated!

# Info 📝
<ul><li>This original source was made by @Android1337 edited and updated to the latest fortnite patch by me </li><li>
 
 Open/Close Menu key = Insert

 
# Features 💿
<ul><li>Aimbot</li><li>ESP</li><li>Exploits</li><li>Misc</li><li>Aimbot Fov Circle</li><li>Aimbot Smooth</li><li>Aimbot Bone</li><li>Aimbot Prediction</li>
<li>Box ESP</li></ul><ul><li>Skeleton</li><li>Lines</li></ul></ul></li><li>Player Names</li></ul></li><li>Stream Sniper Player</li></ul></li><li>Aim While Jumping</li></ul></li><li>No Weapon Switch Delay</li></ul></li><li>No Spread</li></ul></li><li>Rapid Fire</li></ul></li><li>Trigger Bot</li></ul></li><li>AirStuck</li></ul></li><li>360 Fov</li></ul></li><li>Instant Revive</li></ul></li><li>Fov Circle off/on</li></ul></li><li>Crosshair</li></ul>

# Download Cheat Ready to use here! 🔥

>>> https://github.com/SantaaVibez/FortniteRageCheatSource/releases/tag/V2


[![Watch the video](https://i.imgur.com/vKb2F1B.png)](https://streamable.com/xmx49y)


![](https://komarev.com/ghpvc/?username=SantaaVibez&color=yellow)
# Fortnite-Emotes-System
This is Fortnite emotes System running in the Unity Engine
To build it you will need the Unity Plus or Unity Pro license to order to this to work and you need to install Visual Studio 2017 or better.



Windows

Microsoft Visual Studio 2019 and Unity 2019.1 or higher.
To Get Custom Faces put it in the Faces folder


![](Screenshot_220.png)

# Fortnite-Emotes-System
This is Fortnite emotes System running in the Unity Engine
To build it you will need the Unity Plus or Unity Pro license to order to this to work and you need to install Visual Studio 2017 or better.



Windows

Microsoft Visual Studio 2019 and Unity 2019.1 or higher.
To Get Custom Faces put it in the Faces folder


![](Screenshot_220.png)

# Dll-Encryptor
-------

(I'm not responsible of any bad usages of this, this as been made for educational purposes only)

People who make pay hacks typically have down syndrome and are incapable of using their brains in any fashion, and yet these bath salt smoking morons are making pay hacks...Sooner or later when they get close to actually releasing their cheat, they realize "omg I pasted this entire thing, what if someone leaks my DLL, they'll know I'm a retard!"

That is when they then come and ask "how to stream a DLL without hitting disk!?"

Well look what we have here, our old friend Senor Paster McGee is back and needs help doing actual development, something he can't paste. Well don't worry folks, Lord Rake has granted you a glimpe into his omniscience with this fresh AF proof of concept that will show you how to stream a DLL, without touching disk, and we'll even slap some juicy encryption on it as well.

This source code shows you how to split the DLL into 4 different files and encrypt each of them using blowfish encryption with seperate keys. Your loader would download these 4 files using InternetReadFile, decrypt them and then combine them into the original DLL bytes as a string, and then manually map it. I have left manual mapping out of this project, you have to figure that part out.

People making payhacks ask how to stream a DLL in C++ all the time, maybe they shouldn't be making pay hacks if they can't solve simple problems like this, smh. So how do you stream a DLL from your web server without downloading it to disk?

Disclaimer: I whipped this up as fast as I could, nothing too special, this is just something I came up with to reduce the chance your DLL gets dumped.

<div align="center">
    <img src="https://cdn.discordapp.com/attachments/901211756075044874/903060398318690334/unknown.png"/>
</div>

This is how you stream a DLL into a string, without ever touching disk, simply using InternetReadFile
(obviously it would be best to use something different that isn't a simple WinAPI call, but this is just a PoC)

```cpp
std::string StreamFileToMemString(std::wstring URL)
{
    const wchar_t* header = L"Accept: *" "/" "*\r\n\r\n";
    HANDLE hInterWebz = InternetOpen(L"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/58.0.3029.110 Safari/537.36", INTERNET_OPEN_TYPE_DIRECT, NULL, NULL, NULL);
    HANDLE hURL = InternetOpenUrl(hInterWebz, URL.c_str(), header, lstrlen(header), INTERNET_FLAG_DONT_CACHE, 0);

    char* Buffer = new char[100000000]; //100mb
    memset(Buffer, 0, 100000000);
    DWORD BytesRead = 1;

    std::string data;

    if (InternetReadFile(hURL, Buffer, 100000000, &BytesRead))
    {
        data = std::string(Buffer);
    }

    delete[] Buffer;
    InternetCloseHandle(hInterWebz);
    InternetCloseHandle(hURL);

    return data;
}
```

**This is how we download the 4 encrypted file & decrypt it into a string which represents our streamed DLL**
```cpp
std::string GetDecryptedDLL()
{
    std::string data1 = StreamFileToMemString(LR"(https://guidedhacking.com/gh/dl/dlltest/1)");
    std::string data2 = StreamFileToMemString(LR"(https://guidedhacking.com/gh/dl/dlltest/2)");
    std::string data3 = StreamFileToMemString(LR"(https://guidedhacking.com/gh/dl/dlltest/3)");
    std::string data4 = StreamFileToMemString(LR"(https://guidedhacking.com/gh/dl/dlltest/4)");

    std::string decryptedDLL = Decrypt({ data1, data2, data3, data4 });

    return decryptedDLL;
}
```

**This function shows the blowfish decryption of the streamed DLL:**
```cpp
std::string Decrypt(EncryptedData_t encryptedData)
{
    //decrypt each part
    std::string BufferDecrypted = blowfish1.Decrypt_CBC(encryptedData.a);
    BufferDecrypted += blowfish2.Decrypt_CBC(encryptedData.b);
    BufferDecrypted += blowfish3.Decrypt_CBC(encryptedData.c);
    BufferDecrypted += blowfish4.Decrypt_CBC(encryptedData.d);

    //rebuild the DLL from decrypted data
    std::ofstream ofs;
    ofs.open(L"original-rebuilt.dll", std::ios::binary);
    std::copy(BufferDecrypted.begin(), BufferDecrypted.end(), std::ostream_iterator<char>(ofs));
    ofs.close();

    return BufferDecrypted;
}
```

**This is showing a test case of downloading, decrypting and saving the file to disk, for testing that it works correctly:**
```cpp
int TestDownloadAndDecryption(fs::path currDir)
{
    std::string decryptedDLL = GetDecryptedDLL();

    //Test output to disk
    std::ofstream ofs;
    ofs.open(currDir / L"original-rebuilt.dll", std::ios::binary);
    std::copy(decryptedDLL.begin(), decryptedDLL.end(), std::ostream_iterator<char>(ofs));
    ofs.close();

    std::getwchar();
    return 0;
}
```
**Now what? How to inject the DLL stream**


```cpp
std::string decryptedDLL = GetDecryptedDLL();
ManualMap(decryptedDll.c_str());
//Ensure the DLL bytes are destroyed at this point
```

This encrypted DLL streaming project is a great starting point for any amateur pay cheat.

Obviously if you were reversing this, you would just dump the argument to the manual mapping function, but if you slapped VMProtect on this and used a few other tricks, it would be annoying enough where most people would give up. Also the flow of execution is very obvious, if you were to do this in stages, sprinkled through the entire execution of your loader, it would be a lot less obvious.

Pro Tip: if you're gonna use this or any other type of encryption, randomize the S boxes and the P array, if you don't SignSearch will detect them and the person analyzing it will instantly know the encryption routine. Most encryption like blowfish will give you this default seed data, and every single implementation you find online will all use the same default seed data, making it trivial to identify with something like SignSearch. (some even use the same key, smh). When you use signsearch and it identifies the encryption, it takes about 15 seconds to find the decryption function. I have already randomized them in my download above.

Also be wary of using cryptopp or other common libraries, they are super easy to identify, some expose RTTI and others have pdbs, then you have TypeLibraries and Lumina servers, making it too easy to identify and reverse them with limited effort.

Credits: Rake (All)