# Vehicle Detection Dataset


Annotation tool: CVAT

Annotation type: Bounding Box

Number of images: 50

Number of classes: 5

Export format: YOLO 1.1





# Class Mapping


0 = car

1 = bus

2 = truck

3 = motorcycle

4 = bicycle





# Annotation Rules


* Only the five specified vehicle classes were annotated.
* Vehicles or objects that did not match these five specified classes were not annotated.





# Dataset Structure


Vehicle\_Detection\_CVAT\_Portfolio/

│

├── images/

│   ├── image\_001.jpg

│   ├── image\_002.jpg

│   └── ...

│

├── labels/

│   ├── image\_001.txt

│   ├── imgae\_002.txt

│   └── ...

│

│

├── classes.txt

└── README.md





# Annotation Format


* Each image has a corresponding .txt annotation file.
* Each line in the .txt file represents one annotated object: class\_id center\_x center\_y width height
* An image can contain multiple annotated objects, so the .txt file can contain multiple lines.


Example:

0 0.542716 0.635844 0.326503 0.144781
2 0.756200 0.546625 0.477203 0.225594
2 0.177459 0.516953 0.063543 0.043281


* The first value is the class ID, followed by the normalized bounding-box coordinates.
* Coordinates are normalized between 0 and 1.


**Notes** *All bounding boxes were manually annotated in CVAT.*

