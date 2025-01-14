# QLumEdit

### LICENCE

```
QLumEditWasm, an ultimate Eulumdat in Browser file editor
Build with CMake using emscripten and QT WebAssembly
Copyright (C) 2022 Holger Trahe

a fork of

QLumEdit, an ultimate Eulumdat file editor
Copyright (C) 2007-2021 Krzysztof Strugiński

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

Contact e-mail: Krzysztof Strugiński <cagrin@gmail.com>
  Program page: https://github.com/cagrin/qlumedit
      Icon set: https://iconarchive.com/show/gartoon-icons-by-zeusbox.html
```

### TRANSLATIONS

```
English: https://github.com/cagrin
 Polish: https://github.com/cagrin
 German: https://sourceforge.net/users/erni24
```

Online App

https://eulumdat.icu

### CHANGELOG

QLumEditWasm 0.2 (2022-10-10)

- Added URL reading and loading given name and ldc_content bas64 encoded, so a
  Eulumdat can be loaded via URL (see gldf.icu, which creates eulumdat.icu urls
  to view/edit the GLDF contained LDCs)
- fixed emscripten Asyncify configuration

0.1 (2022-10-09):

- Updated to use QT6.5
- created CMakeLists.txt and the CMake ToolChain needed for WebAssebmly using
  emscripten and the configured QT Source for using WebAssembly
- changed header
- initial WIP WASM compatible Browser File Upload for uploading Files instead of
  Open File from FileSystem

1.0.3 (2021-10-06):

- updated to Qt 6.2.0
- macOS universal version

1.0.2 (2021-02-09):

- updated project file to Qt 5.14.2
- added German translation
- x64 version

1.0.1 (2012-09-19):

- new installer and icon set
- file association *.ldt

0.2.1 (2007-06-29):

- becomes version 1.0
