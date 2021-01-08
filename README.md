# Client Image Loader
Client Image Loader is a DLL that can be injected into a MapleStory client to load from image data files.

## What
 This will make your MapleStory client load from "*.img" files inside a data directory "./Data" instead of "*.wz" compressed files at the index.
 
## Why
There are a couple of advantages especially for WZ editors trying to get new content to work in older versions.

 - Eliminate the GFX glitches and memory leaks making the client more stable.
- Push file updates and patches to your users faster, easier and less bandwidth consuming.
-  Your game installation directory and file structure will look well organized.
- It's cool and interesting?

## How
You need to specify the correct function addresses in "Resman.cpp" for your particular client version. In fact, you should find information in the "functions" directory for the major versions.

 So, after you compile this project resulting in a DLL file you need to inject it. Now, there are many ways to inject a DLL to your MapleStory client but this project is already configured with the APIDummy export method.
 1. Download CFF Explorer.
 2. Go to "File > Open" and select your "ijl15.dll" inside your MapleStory directory.
 3. Proceed to "Import Adder" and click "Add" then select the compiled DLL file.
 4. Import the "APIDummy" export that you just added.
 5. Click "Rebuild Import Table" then save the file.
Now your client should automatically load with the compiled DLL already injected.

## Credits
@[**buttbeam**](http://forum.ragezone.com/members/2000258756.html) ~ Everything? [Released this](https://gist.github.com/y785/3f13026d33b5a7f0edab0bd60f4eed36).

@[**Darter**](http://forum.ragezone.com/members/450249.html) ~ This project is based on his [AuthHook](https://github.com/RajanGrewal/AuthHook/) release.

@[**Eric**](http://forum.ragezone.com/members/801110.html "Eric is online now") ~ I [learnt a lot](http://forum.ragezone.com/f921/src-universal-localhost-enabler-1137639-post8872554/#post8872554) from him.
