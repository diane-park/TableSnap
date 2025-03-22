# TableSnap
By: Ashley Brea, Ashley Kim, Diane Park
Deep Learning Project Spring-2025

### Abstract:
Our project focuses on converting tables from images into CSV format, with the long-term goal of digitizing handwritten data tables. To achieve this, we begin by detecting table structures through object detection (Milestone 1). Then, we hope to identifying rows and columns map their relationships before applying OCR for text extraction.

We build on previous research, such as CascadeTabNet (Prasad et al.) and DeCNT (Siddiqui et al.), which utilize deep learning for table detection and structure recognition. Using a filtered subset of the General Table Detection dataset (1,308 samples with a single table per page), we preprocess the data by extracting bounding box values and normalizing them relative to image dimensions. The dataset is split into training (70%), validation (20%), and testing (10%).

Key challenges include identifying tables without visible borders, training with a limited dataset, handling mixed file formats (.jpg and .png), and addressing the dataset’s lack of handwritten text samples. Future work will focus on expanding the dataset and improving OCR performance for handwritten table data.