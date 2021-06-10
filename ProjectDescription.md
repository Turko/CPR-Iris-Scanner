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

## 11.03
- Image Installation

## 25.03
- Kamera erfolgreich mit dem Raspberry PI verbunden: 

![1](https://user-images.githubusercontent.com/74356182/119810306-340db080-bee6-11eb-950d-65854cfb5d8f.jpg)
![2](https://user-images.githubusercontent.com/74356182/119810416-4f78bb80-bee6-11eb-9ea7-5c077ec50269.jpg)

## 25.03
- Bilder aufnehemen mithilfe von: raspistill -o image.jpg
- Videos aufnehemen mithilfe von raspivid -o video.h264 -t 10000 ===> -t steht hier in dem Fall für eine 10 sekündige Aufnahme


## 15.04
- Nach dem Einrichten des Kameramoduls wurde anschließend, mithilfe von CMake, OpenCV installiert

- Wichtige Arbeitsvorgänge: 
- CMake hilft uns die OpenCV Libary zu kompilieren, somit müssen wir das als erstes snapd installieren um die CMake Packages installieren zu können --> sudo apt install snapd

![1](https://user-images.githubusercontent.com/74356182/121461503-4b9d6c80-c9af-11eb-87d6-20fbdfeb0324.png)
 
 - Jetzt können wir die CMake  Packages isntallieren mit folgendem Command --> sudo snap install cmake --classic
 
 ![2](https://user-images.githubusercontent.com/74356182/121461755-bcdd1f80-c9af-11eb-8300-f63afc3b7e50.png)
 
 - Python 3 Installation --> sudo apt-get install python3-dev
 
 ![3](https://user-images.githubusercontent.com/74356182/121461865-f4e46280-c9af-11eb-83cf-aed508343065.png)
 
 - Downloaden der Source Code Packages von OpenCV und kompilieren es auf dem Raspberry Pi mithilfe von CMake --> wget -O opencv.zip       https://github.com/opencv/opencv/archive/4.0.0.zip

![4](https://user-images.githubusercontent.com/74356182/121462467-eba7c580-c9b0-11eb-8610-931a4fad7c67.png)

- und jetzt die Packages entpacken/installieren --> unzip opencv.zip

![5](https://user-images.githubusercontent.com/74356182/121462653-375a6f00-c9b1-11eb-84f9-794234c30f7e.png)

- NumPy Instalation, damit OpenCV auch ordentlich funktionieren kann --> pip install numpy

![6](https://user-images.githubusercontent.com/74356182/121462863-8b655380-c9b1-11eb-8866-82fa376c979c.png)

- Kompilierbefehele --> jetzt müssen wir CMake zum laufen bringen. In den Pfad “~/opencv-4.0.0/build” wechseln und folgende Zeilen hineien kopieren:

cmake -D CMAKE_BUILD_TYPE=RELEASE \
    -D CMAKE_INSTALL_PREFIX=/usr/local \
    -D OPENCV_EXTRA_MODULES_PATH=~/opencv_contrib-4.0.0/modules \
    -D ENABLE_NEON=ON \
    -D ENABLE_VFPV3=ON \
    -D BUILD_TESTS=OFF \
    -D WITH_TBB=OFF \
    -D INSTALL_PYTHON_EXAMPLES=OFF \
    -D BUILD_EXAMPLES=OFF ..

![8](https://user-images.githubusercontent.com/74356182/121463395-40980b80-c9b2-11eb-9c21-4b90f7aa6f0d.png)

![9](https://user-images.githubusercontent.com/74356182/121463506-7b9a3f00-c9b2-11eb-9e33-4aedc77c1148.png)

- OpenCV kompilieren --> Make –j4

![10](https://user-images.githubusercontent.com/74356182/121463738-dcc21280-c9b2-11eb-9da7-b20191c8a6b2.png)

- libopencv Installation --> sudo apt-get install libopencv-devpython-opencv

![11](https://user-images.githubusercontent.com/74356182/121463821-0aa75700-c9b3-11eb-9c33-3fcde3f4dc2a.png)




## 27.05
- Arbeiten am "Protokoll"
- Informieren über die noch zu erreichenden Ziele










