# TableSnap: Table Detection
Team Name: Algorithm Architects 

Team Members: Ashley Brea, Ashley Kim, Diane Park

Deep Learning Project Spring-2025

### Abstract:
Our project focuses on converting tables from images into CSV format, with the long-term goal of digitizing handwritten data tables. To achieve this, we begin by detecting table structures through object detection (Milestone 1). Then, we hope to identifying rows and columns map their relationships before applying OCR for text extraction.

We build on previous research, such as CascadeTabNet (Prasad et al.) and DeCNT (Siddiqui et al.), which utilize deep learning for table detection and structure recognition. Using a filtered subset of the General Table Detection dataset (1,308 samples with a single table per page), we preprocess the data by extracting bounding box values and normalizing them relative to image dimensions. The dataset is split into training (70%), validation (20%), and testing (10%).

We then use YOLOv5 as our baseline model for obejct detection. This was motivated by YOLO's capacity to pad and resize images, allowing us to use images of different sizes. We continue to use YOLOv5 as our deep learning model, where we trander learning and fine tune our date by increasing the number of epochs and decrerasing the learning rate. Both the baseline model and the deep learning model are evaluated, and we do see an improvemnt in its metrics after the finetuning. 

Our next steps are to implement visualizations, and move onto row and column detection and mapping.

### Setup & How to Run:
Simply copy the CoLab Notebook and run all cells.

Key challenges include identifying tables without visible borders, training with a limited dataset, handling mixed file formats (.jpg and .png), and addressing the dataset’s lack of handwritten text samples. Future work will focus on expanding the dataset and improving OCR performance for handwritten table data.
