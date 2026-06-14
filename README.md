# IRGPOST - GNSS RTK Post-Processing App

IRGPOST is an Android app for GNSS data processing, RTK post-processing, and RINEX rover/base solution generation. It is built for survey, geodesy, mapping, and tectonic plate study workflows that need mobile RTKLIB-style post-processing from RINEX observation and navigation files.

Use IRGPOST to process standard RINEX data from GNSS receivers, including rover/base RINEX files exported by receivers such as Emlid and other survey-grade GNSS systems. The built-in raw-log converter is limited to IRG09, IRG03, and IRG04 GNSS receiver files.

Search terms: GNSS data processing, RTK GNSS, RTKLIB Android, RINEX post-processing, rover base processing, GNSS survey app, Emlid RINEX processing, GPS GLONASS Galileo BDS post-processing.

## Download / Install

[Download latest APK](https://github.com/Ishra-Nav/IRGPOST/releases/download/v2/IRGPOST.apk)

Steps to install on your phone:

1. Open the download link above in your browser. It downloads `IRGPOST.apk`.
2. Tap the downloaded file from the notification or Downloads app.
3. If prompted with `Install unknown apps`, tap Settings and enable `Allow from this source`.
4. Go back and tap Install.
5. The app appears in your app drawer once installed.

The app checks for updates automatically and prompts you to install new versions as they are released.

## Sample Data

Sample RTK/RINEX data is available here:

[IRGPOST sample data on Google Drive](https://drive.google.com/drive/u/1/folders/108PdpVP9yu8ZTcFeYzjDadPoRZQGJ7e3)

Download the sample rover, base observation, and navigation files, then copy them to:

```text
Documents/IRGPOST/RINEX
```

Create the folder on the phone if it does not already exist.

## Post-Processing Steps

### 1. Copy RINEX Files To The Phone

Place rover and base RINEX observation/navigation files in:

```text
Documents/IRGPOST/RINEX
```

Supported observation file examples:

```text
.obs, .OBS, .26O, .26o
```

Supported navigation file examples:

```text
.nav, .NAV, .26P, .26p
```

### 2. Select Input Files

Open the `Files` menu:

- `ROVER:OBS` selects one or more rover observation files.
- `BASE:OBS` selects the base station observation file.
- `BASE:NAV` selects the base station navigation file.

The file picker opens the RINEX folder and filters files by the selected input type.

### 3. Adjust Settings

Open the `Config` menu to set processing options such as:

- Positioning mode
- Frequencies
- Navigation systems
- Elevation mask
- Solution format
- Reference position
- Output epoch
- Output processed files: `Combined` or `Separate`

Use `Combined` to merge all rover results into one output file, or `Separate` to create one output file per rover file.

### 4. Run Processing

Open:

```text
Process -> Execute
```

The app processes each rover file against the selected base OBS/NAV data.

### 5. View Results

When processing finishes, the app shows a `Process Result` dialog with computed positions, including latitude, longitude, height, quality indicator, and related statistics.

For multi-rover batches, a summary line shows the output file location and number of processed points.

Output `.pos` files are written under:

```text
Documents/IRGPOST
```

or the app output folder if Android storage restrictions require it.

## Convert Raw Logs

Use the `Convert` menu to convert supported raw receiver logs into RINEX observation/navigation files before processing.

The converter supports only IRG09, IRG03, and IRG04 GNSS receiver raw files as input.

## Output And Report Features

The result viewer supports:

- All epochs
- Best epoch
- Average
- Analysis
- STD statistics
- LLH / UTM display
- Position and altitude plots
- PDF report generation

PDF reports include Best, Average, Analysis, STD, and plots.
