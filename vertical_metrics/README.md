# research vertical metrics used by apps and operating systems

The idea of this project is to figure out which application uses which vertical metrics information.
To figure this out, I have created some demo fonts with broken vertical metrics in specifc areas.

Fonts for testing: ./fonts

| OS  | App                          | which vertical metrics | useTypeMetrics  | reference | notes                                                                                          | 
| ------------- |------------------------------|-----------------|-----------------| ------------- |------------------------------------------------------------------------------------------------|
| MacOS Monterey (Version 12.1) | Folder Preview               | hhea            | no              | Olli Meier | [1]                                                                                            |
| MacOS Monterey (Version 12.1) | Folder Preview               | hhea            | yes             | Olli Meier | [1]                                                                                            |
| MacOS Monterey (Version 12.1) | Adobe InDesign 2022 (17.0.1) | does not matter | does not matter | Olli Meier | Adobe seems to do it's own things. All fonts have the same vertical metrics [2]. Seems to follow the 120%-rule. |
| Windows 10 | Fonts Preview                | usWin           | no              | Olli Meier | It uses usWin if useTypoMetrics is not set. [3]                                                |
| Windows 10 | Fonts Preview                | sTypo           | yes             | Olli Meier | If useTypoMetrics is set it uses sTypo values. [3][4][5]                                       |
| Windows 10 | MS Word (2108)               | usWin           | no              | Olli Meier | It uses usWin if useTypoMetrics is not set. [6]                                                |
| Windows 10 | MS Word (2108)               | sTypo           | yes              | Olli Meier | If useTypoMetrics is set it uses sTypo values. [6]                                             |
| Windows 10 | MS PowerPoint (2108)         | not clear       | not clear              | Olli Meier | It's not clear which vertical metrics is used by PowerPoint. [7]                               |

# Proofs
[1] Mac 12.1 Folder Preview:
![Mac 12.1 InDesign 17.0.1](./proofs/olli_meier/MacPreview.png?raw=true "Mac 12.1 Folder Preview")


[2] Mac 12.1 InDesign 2022:
![Mac 12.1 InDesign 2022](./proofs/olli_meier/MacInDesign2022.png?raw=true "Mac 12.1 InDesign 17.0.1")

[3] Windows 10 Fonts Preview usWin:
![Windows 10 Fonts Preview usWin](./proofs/olli_meier/win10/Win10FontsPreview_usWin.png?raw=true "Windows 10 Fonts Preview usWin")

[4] Windows 10 Fonts Preview sTypo:
![Windows 10 Fonts Preview sTypo](./proofs/olli_meier/win10/Win10FontsPreview_sTypo.png?raw=true "Windows 10 Fonts Preview sTypo")

[5] Windows 10 Fonts Preview hhea:
![Windows 10 Fonts Preview hhea](./proofs/olli_meier/win10/Win10FontsPreview_hhea.png?raw=true "Windows 10 Fonts Preview hhea")

[6] Windows 10 MS Word 2108:
![Windows 10 MS Word 2108](./proofs/olli_meier/win10/Win10Word.png?raw=true "Windows 10 MS Word 2108")

[7] Windows 10 MS PowerPoint 2108:
![Windows 10 MS PowerPoint 2108](./proofs/olli_meier/win10/Win10PowerPoint.png?raw=true "Windows 10 MS PowerPoint 2108")

