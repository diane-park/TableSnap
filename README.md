# TableSnap: Table Detection
Team Name: Algorithm Architects 

Team Members: Ashley Brea, Ashley Kim, Diane Park

Deep Learning Project Spring-2025

### Abstract:

Table detection in document images is a critical task in document analysis, facilitating the extraction of structured data from unstructured sources. In this project, we focus on detecting tables from images, with the long-term goal of digitizing handwritten data tables from images into CSV format. To achieve this, our current focus is on detecting table structures through object detection techniques.

Building on prior work such as CascadeTabNet (Prasad et al.) and DeCNT (Siddiqui et al.), we leverage deep learning approaches for table detection. We use the General Table Detection dataset, initially training on a filtered subset of 1,308 images containing a single table per page. After validating our approach, we retrained on the full dataset of 2,835 images, including pages with multiple tables. We preprocessed the data by extracting bounding box values and normalizing them relative to image dimensions. Also, the dataset is split into training (70%), validation (20%), and testing (10%).

We then use YOLOv5 as our baseline model for object detection. This was motivated by YOLO's capacity to pad, resize, and normalize images, as well as its pre-trained features. We continue to use YOLOv5 as our deep learning model, where we transfer learning and fine tune our model by increasing the number of epochs and decreasing the learning rate. We decided to fine-tune our model since we can build on our baseline that has already learned general features from the large dataset of YOLOv5. Additionally, our dataset for table detection is relatively limited in size, making fine-tuning a more suitable approach. Both the baseline model and the deep learning model are evaluated, and we do see a 13.7% improvement in mean Average Precision (mAP@05) after the finetuning. 

As next steps, we aim to extend our model to perform row and column detection and structure recognition, ultimately enabling full table digitization.

### Setup & How to Run:
Simply copy the Colab Notebook ([here](TableSnap_Final_Submission.ipynb)) and run all cells from the beginning. If you do not want to retrain the baseline/fine-tuning model, you can download our pretrained model best weights for both models ([baseline model weights](baseline_all_tables_best.pt), [deep learning model weights](fine_tuned_all_tables_best.pt)), and instructions on how to modify filepaths within evaluation cells to use these files are provided within the Notebook. 
