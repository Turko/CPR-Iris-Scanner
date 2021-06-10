# CPR-Fiebermesser


## Überblick
Mithilfe von **Raspberry PI** und einer **Raspberry PI Infrarotkamera** soll man imstande sein die Temperatur einer Person beim Betreten vom Schulgebäude einzufangen.

## Ziele

- Daten von der Infrarotkamera auslesen und weiterverarbeiten
- Ergbenis mithilfe mit Highcharts oder chartJS auf einer Website anzeigen können
- mit einem Express-Server das ganze laufen lassen

## Themenbeschreibung

Als Hardware benutzen wir ein **Raspberry PI** und eine **[Raspberry PI Infrarotkamera](https://at.rs-online.com/web/p/raspberry-pi-kameras/9132664/)**
Hierbei werden für die Umsetzung die Softwares **OpenCV, Highchart und Docker** verwendet.
Mithilfe von **Raspberry PI** und einer **Raspberry PI Infrarotkamera** soll man imstande sein die Temperatur einer Person beim Betreten vom Schulgebäude einzufangen.


## Verwendete Technologien

1. OpenCV
2. [Highchart](https://www.highcharts.com/) oder [chartJS](https://www.chartjs.org/)
3. [Docker](www.docker.com)

## Teamzusammensetzung
- Muhammad Turko (Teamleiter).
- Pascal Sielicki
- Raphael Scharrer


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Bisher erreichte Ziele

11.03
- Image Installation

25.03
- Kamera erfolgreich mit dem Raspberry PI verbunden: 

![1](https://user-images.githubusercontent.com/74356182/119810306-340db080-bee6-11eb-950d-65854cfb5d8f.jpg)
![2](https://user-images.githubusercontent.com/74356182/119810416-4f78bb80-bee6-11eb-9ea7-5c077ec50269.jpg)

25.03
- Bilder aufnehemen mithilfe von: raspistill -o image.jpg
- Videos aufnehemen mithilfe von raspivid -o video.h264 -t 10000 ===> -t steht hier in dem Fall für eine 10 sekündige Aufnahme


15.04
- Nach dem Einrichten des Kameramoduls wurde anschließend, mithilfe von CMake, OpenCV installiert
- Tutorial Link --> https://robu.in/installing-opencv-using-cmake-in-raspberry-pi/

- Wichtige Arbeitsvorgänge: 
- CMake hilft uns die OpenCV Libary zu kompiliern, somit müssen wir das als erstes snapd installieren um die CMake Packages installieren zu können --> sudo apt install snapd

![1](https://user-images.githubusercontent.com/74356182/121461503-4b9d6c80-c9af-11eb-87d6-20fbdfeb0324.png)
 

27.05
- Arbeiten am "Protokoll"
- Informieren über die noch zu erreichenden Ziele










