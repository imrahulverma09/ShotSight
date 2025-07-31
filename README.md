# ShotSight is a computer vision project that detects the precise moment a golf ball enters the hole — the perfect putt. 

### 1. Dataset Preparation (Roboflow)
- Create a project on [Roboflow]
- Define two classes:
  - `Golf_ball`
  - `Golf_hole`
- Upload this [golf video] at 30 FPS
- Annotate all frames and label every Golf_ball and Golf_hole

### 2. Export the Dataset
- Download the dataset as a ZIP file in **YOLO format**

### 3. Model Training
- Train using YOLOv11s (Ultralytics)
- Try parameters like:
- `batch=4`
- `imgsz=640`
- `epochs=30`
- Evaluate performance and fine-tune if needed

### 4. Run Inference on the Video
- Load your trained model (`best.pt`)
- Detect Golf_ball and Golf_hole in each frame
- Check if ball center lies inside the hole's bounding box
- If it does, overlay:
