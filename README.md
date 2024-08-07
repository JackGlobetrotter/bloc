# BLOC - Line bisection pc task

1. [Downloads](#downloads)
2. [Instructions](#instructions)
3. [Changelog](#changelog)
4. [Building and Contributing](#build)
5. [Validation Study](#validation)
6. [Other Documents](#docs)

<a id="downloads"></a>

## Download

All downloads are hosted on the [release page](https://github.com/JackGlobetrotter/bloc/releases/latest).

### Windows

#### Portable Version (No installation required)

- [BLOC.exe](https://github.com/JackGlobetrotter/bloc/releases/latest/download/BLOC.exe)
- Only x64 OS versions are supported
- A waring may pop up during download, as the software has not been signed with a Windows authorized certificat due to cost reasons.
- When first opening the application you will see a message popup due to this software not beeing verified: \
  <img src="https://github.com/JackGlobetrotter/bloc/blob/main/docs/windowsUnverifiedMessage.png?raw=true" alt="drawing" style="width:300px;"/>
- Click `More info` and `Run anyway`

#### Installer

- [BLOC-SETUP.exe](https://github.com/JackGlobetrotter/bloc/releases/latest/download/BLOC-SETUP.exe)

### MacOS

- Intel : [BLOC-x64.dmg](https://github.com/JackGlobetrotter/bloc/releases/latest/download/BLOC-x64.dmg)
- Apple silicon (M1, M2, ...): [BLOC-arm64.dmg](https://github.com/JackGlobetrotter/bloc/releases/latest/download/BLOC-arm64.dmg)

### Linux

- Instructions to come

<a id="instructions"></a>

## How to use

- Open the application
- Line generation modes:
  - Random : lines will be generated randomly (as for their position and letters)
  - Pseudo Random - Fixed Order: Use the pseudo random letters and order defined in the research protocol
  - Pseudo Random - Random Order: Use the pseudo random letters and positions defined in the research protocol but randomize the order of the lines
- Run Mode:
  - Loop: run indefinitely
  - Enter a number of repetitions for the task (default is 60)
- Display
  - Select the Screen to show the task on, should be facing the patient
  - Defaults to any external display if connected
  - Built-in or primary screen is written in bold
- Custom screen settings (optional)
  - Cahnge resolution and size in inches used by the screen used to display the task
- Click on run
- Go forward lines with any key
- Go back (if needed) with the left arrow key (`←`)
- Quit the task with `Escape` or `Abort` on the control screen, will automatically exit if a number of repetitions has been defined and reached
- If lines are not showing, try to click on the grey screen once and retry the keys

<a id="changelog"></a>

## Changelog

Full changelog is available [here](https://github.com/JackGlobetrotter/bloc/blob/main/Changelog.md).

v1.0.2 - Update handeling
v1.0.1 - Icon update
v1.0.0 - Inital release version

<a id="build"></a>

## Building and testing locally

### Testing

`npm run test`

### Building

`npm run build`

### Packaging

`npm run package`

For macOS signing and notarization:

- there are two possiblities:
  - Using an app specific password, your dev id and team id
  - using the keychain
    - add your Apple Developper credentials to the keychain: `xcrun notarytool store-credentials --apple-id "XXXX" --team-id "XXXXX"`
    - enter a name when asked, this will be your KEYCHAIN_PROFILE variable
- create a .env file, examples are given below

Password example

```
APPLE_ID=<APPLEID>
APPLE_APP_SPECIFIC_PASSWORD=<APP SPECIFIC PASSWORD>
TEAM_ID=<APPLLE DEV TEAM ID>
CI=true
```

Keychain example

```
CI=true
KEYCHAIN_PROFILE=<KEYCHAIN NAME GIVEN IN THE PREVIOUS STEP>
```

## Contributing

To come.

<a id="validation"></a>
## Validation
Coline Bouyer, Manuel Gimenes, Jakob Dickert, Siobhan Vicente, Véronique Stal, Michel Wager & Vanessa Baudiffier (2023) Validation of the BLOC test: A computerized oral line bisection task in French healthy participants, Applied Neuropsychology: Adult, DOI: 10.1080/23279095.2023.2290190] (https://www.tandfonline.com/doi/full/10.1080/23279095.2023.2290190)


<a id="docs"></a>
## Other documents

### [Assessment for paper line bissection](https://github.com/JackGlobetrotter/bloc/blob/main/docs/FeuilleDePassation.pdf) ([Download](https://raw.githubusercontent.com/JackGlobetrotter/bloc/main/docs/FeuilleDePassation.pdf))

- Document used to score paper line bisection and defining pseudo-random letter and line position order
