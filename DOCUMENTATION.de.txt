IPCONFIG.R4X
============

IPCONFIG.R4X zeigt Netzwerkstatus, Adapterdaten und Servicezustand im
Terminal an.

Projektstruktur seit 0.51.19:
- `build.zig` baut die App als eigenes SDK-Projekt.
- `build.zig.zon` bindet `r4os_sdk` als Paket.
- `module.R4MF` beschreibt Artefakt, Zielpfad, Imports und Contract.

Build:

    cd Code\System\Software\IpConfig
    ..\..\..\DevTools\Zig\zig.exe build

Ergebnis:

    Code\System\Software\IpConfig\zig-out\IPCONFIG.R4X

Contract:
- R4XStart-Entry: `ipconfig_main`
- App-Klasse: `console`
- R4L-Imports: `R4SYS`, `R4NET`
- Zielpfad im Image: `C:\R4OS\SOFTWARE\TERMINAL\IPCONFIG.R4X`

