#Introduction to open source chip design and Tiny TapeOut
##Workshoppens forventede indhold
•	Introduktion til Chip design
•	Open source Værktøjer
•	Verilog kode eksempel 
•	Funktionel simulering med CocoTB
•	GitHub og Tiny Tapeout Verilog template
•	RTL – GDS, med Tiny tapeout Verilog template
•	Resultater, GDS inspektion

##Forberedelser
Operativsystemer
Open source værktøjer er primært Linux baseret, ingen eller ganske få kører windows, og generelt virker det bare lettere med Linux. Flere værktøjer er også kræsne med linux versionen. Jeg bruger Ubuntu 22.04. Indtil for nylig frarådede man 24.04, så for en sikkerheds skyld, brug gerne Ubuntu 22.04. 
Virtuel maskine
Har man allerede en virtuel maskine fra et kursus på AU kan man godt bruge den. Eller lave en ny.
Windows subsystem for linux, WSL2
Et alternativ til en Virtuel maskine er WSL2 der også integrerer med Windows og windows foldere. Man kan også bruge VSCode og extensions i en WSL installation, og man bestemmer selv hvilken linux distribution man vil bruge, f.eks Ubuntu 22.04.

•	Se er for  information om Windows Subsystem for Linux Documentation | Microsoft Learn
1.	Se under dokumentationen for installation af Ubuntu 22.04. Default version er 24.04 og installeres blot med ”wsl -- install” i windows powershell
2.	Efter succesfuld installation af Ubuntu 22.04 kan Visual Studio Code installeres ved i en linux kommando linje at skrive ”code .” Se under ”Getting started with code” under ”tutorials”
3.	Git kan installeres ved at følge ”Getting started with Git” under ”Tutorials”
•	Grundlæggende Linux kommandoer kan findes under ”Getting started with Linux and Bash” under ”Tutorials”

Værktøjer
Quartus/Modelsim, kommercielt værktøj -alternativ til open source
Da open source værktøjer kører under linux kan det være en omvæltning at skulle skifte til Linux. Quartus bruges kun til implementering på FPGA, Modelsim (evt. med VScode som editor) kan bruges som værktøj til kodning og simulering
Github konto
Man skal lave sig en Github konto på GitHub hvis man ikke allerede har en konto. 
VSCode og extensions
Workshoppen anbefaler brug af VScode som editor, og f.eks denne extension så VScode kan håndtere Verilog filer:
Verilog-HDL/SystemVerilog/Bluespec SystemVerilog - Visual Studio Marketplace

En af mange verilog guides på internettet er denne her : Verilog Tutorial
Open source HDL værktøjer
Vi kan i workshoppen godt undvære brugen af linux hvis vi alene bruger Github og denne TinyTapeout/tt10-verilog-template: Submission template for Tiny Tapeout 10 - Verilog HDL Projects template. Men vi vil nok gerne prøve at kompilere/simulere lokalt. 
Denne side, Working with HDLs :: Quicker, easier and cheaper to make your own chip! Beskriver hvordan vi kan bruge HDL og hvordan vi arbejde lokalt ved installere værktøjer lokalt: Testing your design :: Quicker, easier and cheaper to make your own chip!

Denne side beskriver hvordan vi bruger Github og ”Github actions”
3 - Create the GDS :: Quicker, easier and cheaper to make your own chip!

Vores værktøjer er:
Verilator
IVerilog/icarus
CocoTB og Pytest

Til workshoppen forberedes der en CocoTB testbench sammen med et Verilog eksempel, f.eks dette her: Gurusatwik/PWM-Generator: This repository focuses on how to design a PWM Generator with variable Duty cycle
Ekssemplet kan naturligvis også bruges med Quartus/Modelsim, og koden kan testes på et FPGA board.
Workflow
”Frontend”: Design og funktionel simulering
”Backend”: RTL-to-GDS, et automatiseret flow med Github actions via en Verilog TT template
GDS inspektion/3D viewer
Optionelt: Fra GDS til Chip via Tiny Tapeout


