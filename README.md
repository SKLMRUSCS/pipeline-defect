# Pipeline Crack and Leakage Detection Dataset

This dataset is specifically designed for the detection of pipeline defects, such as cracks and leakages, using object detection models. The data is formatted in both Pascal VOC and YOLO formats, allowing for compatibility with a wide range of machine learning frameworks.

## Dataset Overview

- **Image Format**: JPEG (.jpg)
- **Annotation Formats**:
  - Pascal VOC (.xml)
  - YOLO (.txt)
- **Number of Images**: 2069
- **Number of Annotations**:
  - VOC (.xml): 2069
  - YOLO (.txt): 2069
- **Number of Categories**: 2
- **Category Names**:
  1. `kebocoran` (Leakage)
  2. `keretakan` (Crack)
- **Bounding Box Statistics**:
  - `kebocoran`: 1406 bounding boxes
  - `keretakan`: 1192 bounding boxes
  - **Total Bounding Boxes**: 2598

## Annotation Rules

- **Annotation Tool**: [labelImg](https://github.com/tzutalin/labelImg)
- **Methodology**: Bounding boxes were manually drawn around the defects, with strict adherence to the following guidelines:
  - Clearly identify the boundaries of each defect.
  - Assign the appropriate label (`kebocoran` or `keretakan`) to each bounding box.
  
## Dataset Structure

The dataset is organized as follows:

```
Pipeline-Defect-Detection-Dataset/
|-- images/
|   |-- 0001.jpg
|   |-- 0002.jpg
|   |-- ...
|
|-- annotations/
|   |-- PascalVOC/
|   |   |-- 0001.xml
|   |   |-- 0002.xml
|   |   |-- ...
|   |
|   |-- YOLO/
|       |-- 0001.txt
|       |-- 0002.txt
|       |-- ...
```

- **`images/`**: Contains all the JPEG images.
- **`annotations/PascalVOC/`**: Contains the Pascal VOC annotations in XML format.
- **`annotations/YOLO/`**: Contains the YOLO annotations in TXT format.

## Dataset Usage

### Pascal VOC Format

The Pascal VOC XML files contain detailed annotation information for each image, including:
- Bounding box coordinates (`xmin`, `ymin`, `xmax`, `ymax`)
- Object class (`kebocoran` or `keretakan`)

### YOLO Format

The YOLO TXT files contain annotations in the following format:
```
<class_id> <x_center> <y_center> <width> <height>
```
- `<class_id>`: 0 for `kebocoran`, 1 for `keretakan`
- `<x_center>`, `<y_center>`: Center of the bounding box (normalized to image width and height).
- `<width>`, `<height>`: Width and height of the bounding box (normalized to image width and height).

## Label Distribution

| Category    | Number of Bounding Boxes |
|-------------|---------------------------|
| kebocoran   | 1406                      |
| keretakan   | 1192                      |
| **Total**   | **2598**                  |

## Applications

This dataset is ideal for training and evaluating object detection models, particularly for:
- Defect detection in industrial pipelines.
- Automated quality assurance in manufacturing.

## Citation

If you use this dataset in your research or projects, please cite this work appropriately.

## License

This dataset is licensed under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You are free to use, share, and adapt the dataset, provided proper attribution is given.

---

For any questions or support, please feel free to reach out via the repository's issue tracker.

