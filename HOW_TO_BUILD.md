# How to get your Far Cry 2 APK (about 15 minutes, no programming)

GitHub builds the APK for you in the cloud. You only click buttons.

## A. Make the build (once)
1. Go to github.com and create a free account (or sign in).
2. Click **+** (top right) > **New repository**. Name it `fc2-android`, leave it Public, click **Create repository**.
3. On the empty repo page click **uploading an existing file**.
4. Unzip `fc2-apk-build.zip` on your computer and drag the contents in (the `.github` folder, `fc2_profile` folder, README.md). Click **Commit changes**.
   - If the `.github` folder does not upload (hidden folder), use **Add file > Create new file**, type the name `.github/workflows/build-apk.yml`, paste the contents of `build-apk.yml` (sent as a separate file), and commit.
5. Open the **Actions** tab. If asked, click **I understand my workflows, enable them**.
6. Click **Build Far Cry 2 APK** on the left, then **Run workflow** > **Run workflow**.
7. Wait 10 to 25 minutes. A green check means success. A red X means it failed: open it, copy the red error text and send it to me.
8. Open the finished run and download **FarCry2-apk** at the bottom (Artifacts). Unzip it to get the `.apk`.

## B. Install on the phone
1. Copy the `.apk` to the phone and tap it. Allow "install unknown apps" when asked.
2. Open the app once and wait for its first-time setup to finish (a minute or two).

## C. First-time game setup (once, then it is one tap)
1. Put the game folder in `Download/FarCry2/` on the phone (with `bin\FarCry2.exe` inside).
2. In the app: **+** to create a container. Settings by phone model:
   - Snapdragon (SM-S908U): 1280x720, driver Turnip, DXVK, Box64 preset Compatibility.
   - Exynos (SM-S908B): 960x540, driver VirGL, DXVK (try WineD3D if black screen), Compatibility.
3. Open the container > **Shortcuts** tab > add `D:\FarCry2\bin\FarCry2.exe`. In the shortcut settings pick the **Far Cry 2** controls profile. Tick **Force Fullscreen**.
4. Launch it from the app home screen shortcut (the app can also pin the shortcut to the phone's home screen).

## Notes
- The touch profile has: movement pad, FIRE, AIM, JUMP, RELOAD, USE, RUN, DUCK, MAP, HEAL, MENU, weapon switch. Keys follow the usual PC defaults. If one does nothing, check the key in the game's Options > Controls, then edit the button in the app.
- No keyboard or mouse needed. A Bluetooth gamepad also works.
- I could not test this build myself (my workspace cannot reach Android's build servers). If the build fails, send me the error and I will fix the workflow.
- The package name stays `com.winlator` because the bundled system image depends on it, so this is a re-labeled Winlator build, not a separate engine.
- The disc copy may still ask for activation or the disc at launch; that is a limit of the game, not of the app.
