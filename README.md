# IRGPOST

Android app for RTK GNSS post-processing.

## Download / Install

[Download latest APK](https://github.com/Ishra-Nav/IRGPOST/releases/download/v2/app-debug.apk)

**Steps to install on your phone:**
1. Open the download link above in your browser — it downloads `app-debug.apk`.
2. Tap the downloaded file (from the notification or Downloads app).
3. If prompted "Install unknown apps", tap **Settings** and enable **"Allow from this source"**, then go back and tap **Install**.
4. The app will appear in your app drawer once installed.

The app checks for updates automatically and will prompt you to install new versions as they're released.

## Post-Processing Steps

1. **Copy RINEX files to the phone**
   Place your rover and base RINEX observation/navigation files (e.g. `.obs`/`.26O`, `.nav`/`.26P`) into the
   `Documents/IRGPOST/RINEX` folder on the phone (create the folder if it doesn't exist).

2. **Link the RINEX folder (first run only)**
   The first time you select a file, the system folder picker opens — navigate to and select
   `Documents/IRGPOST/RINEX` and confirm. This is a one-time setup; the app remembers the folder afterwards.

3. **Select input files — Files menu**
   - **ROVER:OBS** — select one or more rover observation files (multi-select: long-press the first
     file, tap to select additional files, then tap "Select").
   - **BASE:OBS** — select the base station observation file.
   - **BASE:NAV** — select the base station navigation file.

4. **(Optional) Adjust settings — Config menu**
   Set processing options such as **O/p Processed Files**: `Combined` (merge all rover results into one
   output file) or `Separate` (one output file per rover file), along with other RTK processing parameters.

5. **Run processing — Process menu → Execute**
   The app processes each rover file against the base OBS/NAV data. A progress bar shows which file is
   currently being processed and the overall percentage complete.

6. **View results**
   - When processing finishes, a **Process Result** dialog summarizes the computed positions
     (latitude, longitude, height, quality indicator, etc.).
   - For multi-rover batches, a summary line (e.g. "Batch complete: 1 combined file, N point(s)") shows
     the output file location.
   - Output `.pos` files are written under `Documents/IRGPOST` (or the app's output folder) and can be
     opened from the **Files** menu or any file manager.

7. **Convert raw logs (optional)**
   Use the **Convert** menu to convert raw receiver logs (e.g. Unicore logs) into RINEX OBS/NAV files
   before processing.
