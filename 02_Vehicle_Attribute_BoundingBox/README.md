# Vehicle Detection Dataset

## Project Overview

* **Annotation tool:** CVAT
* **Annotation type:** Bounding Box
* **Images:** 30
* **Classes:** 6
* **Export formats:** YOLO 1.1, CVAT 1.1

## Class Mapping

| ID | Class         |
| -- | ------------- |
| 0  | car           |
| 1  | bus           |
| 2  | truck         |
| 3  | motorcycle    |
| 4  | bicycle       |
| 5  | auto_rickshaw |

### Class Definitions

* `car` — passenger cars
* `bus` — passenger buses
* `truck` — cargo trucks and light cargo vehicles
* `motorcycle` — motorized two-wheeled vehicles
* `bicycle` — pedal-powered bicycles
* `auto_rickshaw` — three-wheeled motorized vehicles

## Annotation Rules

* Only the six specified classes were annotated.
* Bounding boxes tightly cover the visible vehicle.
* Unidentifiable or excessively blurry vehicles were not annotated.
* `car`, `bus`, `truck`, and `auto_rickshaw` smaller than approximately **15 × 15 pixels** were not annotated.
* Smaller `motorcycle` and `bicycle` objects were annotated when clearly identifiable.

## Occlusion

CVAT's built-in `Occluded` property was used.

* `ON` — another object blocks part of the vehicle.
* `OFF` — the vehicle is not blocked.
* `Q` — toggle `Occluded`.

## Attributes

### Color

Values:

`black`, `white`, `gray`, `silver`, `red`, `blue`, `yellow`, `green`, `brown`, `other`

Use `other` when the color is uncertain or does not match the available categories.

### Orientation

Values:

`front`, `rear`, `left_side`, `right_side`, `front_left`, `front_right`, `rear_left`, `rear_right`

### Truncated

* `yes` — vehicle is cut by the image boundary.
* `no` — vehicle is completely inside the image.

`Occluded` and `truncated` are separate properties and may both apply to the same vehicle.

## Dataset Structure

```text
02_Vehicle_Attribute_BoundingBox/
│
├── CVAT_1.1/
│   ├── images/
│   │   ├── image_001.jpg
│   │   ├── image_002.jpg
│   │   └── ...
│   └── annotations.xml
│
├── YOLO_1.1/
│   ├── images/
│   │   ├── image_001.jpg
│   │   ├── image_002.jpg
│   │   └── ...
│   └── labels/
│       ├── image_001.txt
│       ├── image_002.txt
│       └── ...
│
├── classes.txt
└── README.md
```

## YOLO Class File

`classes.txt` contains class names in ID order:

```text
car
bus
truck
motorcycle
bicycle
auto_rickshaw
```

Numbers are not written in `classes.txt`. The line order determines the YOLO class ID.

## YOLO Annotation Format

Each image has a corresponding `.txt` label file:

```text
class_id center_x center_y width height
```

Example:

```text
0 0.542716 0.635844 0.326503 0.144781
2 0.756200 0.546625 0.477203 0.225594
```

Coordinates are normalized between `0` and `1`.

## Export Information

**CVAT 1.1** preserves:

* Classes
* Bounding boxes
* Occluded
* Color
* Orientation
* Truncated

**YOLO 1.1** contains:

* Class IDs
* Bounding-box coordinates

## Quality Notes

All annotations were manually created in CVAT using consistent class, bounding-box, occlusion, truncation, color, and orientation rules.
