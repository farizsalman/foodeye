# 🍛 FoodEye – Indian Food Detection using YOLO

FoodEye is a computer vision project that detects and classifies Indian food items from images using the YOLO object detection framework.

The model is trained on a custom food dataset and can identify multiple food categories in a single image with bounding box localization and class prediction.

## 🚀 Features

* Real-time food detection
* Multiple food classes
* YOLO-based object detection
* Custom dataset training
* Bounding box visualization
* Supports image inference and model evaluation

## 📂 Project Structure

```text
food_detection/
│
├── YOLO_OBJ.ipynb          # Training and inference notebook
├── data.yaml              # Dataset configuration
├── README.dataset.txt     # Dataset information
├── README.roboflow.txt    # Roboflow export details
├── .gitignore
│
├── data/                  # Dataset (excluded from GitHub)
├── runs/                  # Training outputs (excluded)
├── venv/                  # Virtual environment (excluded)
│
└── *.pt                   # Model weights (excluded)
```

## 🛠️ Technologies Used

* Python
* Ultralytics YOLO
* OpenCV
* Roboflow
* Jupyter Notebook

## 📊 Dataset

The model was trained using a custom food image dataset exported from Roboflow.

Dataset contains:

* Training images
* Validation images
* YOLO formatted annotations

Dataset files are excluded from this repository due to size limitations.

## 🏋️ Training

Example training command:

```bash
yolo detect train data=data.yaml model=yolov8n.pt epochs=50 imgsz=640
```

For YOLO11:

```bash
yolo detect train data=data.yaml model=yolo11n.pt epochs=50 imgsz=640
```

## 🔍 Inference

```bash
yolo detect predict model=best.pt source=image.jpg
```

Predictions are saved inside the `runs/` directory.

## 📈 Future Improvements

* Streamlit deployment
* Real-time webcam detection
* Nutritional information integration
* Mobile application support
* Food calorie estimation

## 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

## 📜 License

This project is intended for educational and research purposes.
