# Devops03 - Cum incepem dezvoltarea cu Flutter

## Ce este flutter
Fluttter este un platforma de dezvoltare a interfeței cu utilizatorul gratuit și open source creat de Google. Pană atunci, a fost folosit pentru a dezvolta aplicații pentru Android și iOS și este, de asemenea, principala metodă de creare a aplicațiilor pentru Google Fuchsia.

Cu toate acestea, datorită posibilităților oferite de limbajul de programare Dart și noilor instrumente de dezvoltare, s-a reușit să se extindă suportul inițial atat la web cat si la Desktop.

## Un pic de istoric

Totul a început în 2011: Xamarin, acum o companie deținută de Microsoft, a venit cu o soluție pentru aplicații mobile hibride prin produsul său de semnătură, Xamarin SDK cu C #. Și astfel a început revoluția aplicațiilor mobile hibride, ușurința în scrierea unei baze de cod pentru multe platforme.

Ionic a apărut în 2013 cu prima sa versiune de Drifty Co. Ionic a ajutat dezvoltatorii web să își folosească abilitățile existente în industria de aplicații mobile în creștere. În 2015, Facebook a folosit React.js pentru a-l reinventa pentru dezvoltatorii de aplicații mobile. Ne-au oferit React Native, o bază de cod complet JavaScript bazată pe SDK-uri native.

## De ce vom avea nevoie

### Utilitare

| Utility | Image | Description |
| :--- | :---: | --- |
| [Android Studio](https://developer.android.com/studio) | ![Android Studio](https://raw.githubusercontent.com/c4xp/Devops03/master/assets/astudio.png) | Android Studio will supply the SDK needed for simulating the mobile phone |
| Visual Studio Code | ![VS Code](https://raw.githubusercontent.com/c4xp/Devops03/master/assets/vscode.png)  | Visual Studio Code is the Integrated editor used for Development |
| [Docker desktop](https://www.docker.com/products/docker-desktop) | ![Docker desktop](https://raw.githubusercontent.com/c4xp/Devops03/master/assets/docker.png)  | Otional* We will need docker for seting up the local backend for testing |
| [Chocolatey](https://chocolatey.org/) | ![Chocolatey](https://raw.githubusercontent.com/c4xp/Devops03/master/assets/chocolatey.png) | With Chocolatey package manager we will stay up to date with flutter, git, dart and other needed packages |

### Android Studio

Dupa ce am instalat Android Studio impreuna cu Android Virtual Device, vom instala SDK cu versiunea de Android dorita si Command-line Tools care va permite interactiunea cu flutter.

[Android Sdk](https://raw.githubusercontent.com/c4xp/Devops03/master/assets/sdk.png)

Urmatorul pas e sa construim un mediu virtual Android

[Android Avd](https://raw.githubusercontent.com/c4xp/Devops03/master/assets/avd.png)

### Chocolatey

- Deschideți o fereastră Powershell: `❖ + X`, select `Windows PowerShell (Admin)`
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
Enable-WindowsOptionalFeature -Online -FeatureName containers –All
```

Ce avem ca setare de sistem ?
```
Get-ExecutionPolicy
```

Atunci vrem sa putem instala pachete verificate
```
Set-ExecutionPolicy AllSigned
```

Asta inseamna si Chocolatey
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

### Altele

| Utility | Setup |
| :--- | --- |
| Git | `choco install git` |
| VS Code | `choco install vscode` |
| Flutter | `choco install flutter` |

### Mediul Flutter

Trebuie sa fim de acord cu cateva lucruri:

```
flutter doctor --android-licenses
```

si sa vedem ca totul este in regula:

```
flutter doctor -v
```

