# Electronic Component Segmentation Dataset

## Project Overview

**Annotation Tool:** CVAT
**Annotation Type:** Polygon / Instance Segmentation
**Dataset Type:** Electronic Components
**Export Formats:** CVAT for Images 1.1, Ultralytics YOLO Segmentation

## Classes

1. Arduino Uno
2. 7-Segment Display
3. DC Motor
4. Buzzer
5. LED Light
6. Resistor
7. Taper Potentiometer
8. Push Switch

## Annotation Work

I created polygon annotations around the visible boundaries of electronic components. The polygons were carefully fitted to the object contours, including curved and irregular shapes.

The dataset was reviewed to maintain:

* Accurate object boundaries
* Consistent class labeling
* Proper separation between individual components
* Detailed polygon contours for irregular and curved objects
* Consistent annotation quality across images

## Dataset Exports

**CVAT for Images 1.1**

* Preserves the original CVAT polygon annotations.
* Used as the detailed/master annotation format.

**Ultralytics YOLO Segmentation**

* Converts the polygon annotations into YOLO segmentation format.
* Suitable for computer-vision segmentation training workflows.

## Skills Demonstrated

* Polygon annotation
* Instance segmentation
* Electronic-component identification
* Object boundary tracing
* Dataset organization
* CVAT annotation workflow
* YOLO segmentation dataset preparation


Electronic_Component_Segmentation/
│
├── CVAT_1.1/
│   ├── images/
│   │   ├── image_001.jpg
│   │   ├── image_002.jpg
│   │   └── ...
│   │
│   └── annotations.xml
│
├── YOLO_Segmentation/
│   ├── images/
│   │   ├── image_001.jpg
│   │   ├── image_002.jpg
│   │   └── ...
│   │
│   └── labels/
│       ├── image_001.txt
│       ├── image_002.txt
│       └── ...
│
├── classes.txt
└── README.md