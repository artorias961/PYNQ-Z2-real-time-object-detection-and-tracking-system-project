# Project Goal
Develop a real-time object detection and tracking system using the PYNQ-Z2 board, leveraging its FPGA capabilities for high-speed video processing and machine learning acceleration.



## High-Level Objectives
1. Detect objects in a video feed (e.g., people, vehicles)
2. Track objects across video frames with unique IDs
3. Display real-time results on a monitor or a web interface


## Pipeline Block Diagram

```bash
Camera Input --> Preprocessing --> Object Detection (YOLOv3-tiny) --> Tracking (DeepSORT) --> Output (Display/Web Interface)
```

Components:

- **Camera Input**: USB or HDMI camera providing live video feed
- **Preprocessing**: Resizing and formatting frames for the model
- **Object Detection**: FPGA-accelerated object detection using YOLOv3-tiny or MobileNet-SSD
- **Tracking Algorithm**: Assign unique IDs and track objects using SORT or DeepSORT
- **Output**: Visualize results via HDMI display or a web-based interface


## Phase 1: Research and Planning

1. Understand PYNQ-Z2:
   - Review its hardware features (e.g., FPGA, ARM processor, HDMI support)
   - Explore the PYNQ framework and pre-built overlays for machine learning

2. Select Models and Algorithms:
   - Object Detection: Lightweight models like YOLOv3-tiny or MobileNet-SSD
   - Object Tracking: Algorithms like SORT (simple) or DeepSORT (advanced)


3. List Resources:
   - Hardware: PYNQ-Z2 board, camera, monitor, SD card
   - Software: PYNQ framework, Vivado (for custom overlays), Python libraries




## Phase 2: Prototype Design

1. Set up a video pipeline using OpenCV on a PC:
   - Capture frames from a camera
   - Implement basic detection using pre-trained YOLOv3-tiny
 
2. Visualize detections with bounding boxes




## Phase 3: Deploy to PYNQ-Z2
1. Prepare the Model:
   - Convert the model to ONNX or TensorFlow Lite
   - Quantize the model for FPGA deployment

2. Use Pre-Built Overlays:
   - Load pre-built PYNQ overlays for machine learning
   - Test detection on the FPGA with sample frames

3. Integrate the Camera:
   - Connect the camera to PYNQ-Z2
   - Stream live video through the pipeline


## Phase 4: Add Object Tracking
1. Implement a tracking algorithm:
   - SORT: Simple tracking with bounding box overlap
   - DeepSORT: Combines tracking with feature embeddings

2. Assign unique IDs to detected objects


## Phase 5: Optimize and Test
1. Measure system performance:
   - Evaluate FPS, accuracy, and latency
   - Test in various environments and lighting conditions

2. Debug issues:
   - Address misdetections or dropped frames


## Phase 6: Final Integration
1. Add an output interface:
   - Display results on an HDMI-connected monitor
   - Alternatively, build a web-based GUI with Flask, Django, or Node.JS

2. Document the project:
   - Write a report with diagrams, code snippets, and performance metrics




# Libraries and Tools

## Python Libraries
1. **OpenCV**: For camera input and video processing.
2. **PYNQ Framework**: High-level programming on the PYNQ-Z2.
3. **NumPy**: For numerical operations.
4. **TensorFlow or PyTorch**: For model conversion and preprocessing.
5. **Flask/Django**: For a web-based GUI (if required).


## FPGA Tools
1. **Vivado**: For custom overlays (if needed).
2. **Xilinx DPU (Deep Learning Processor Unit)**: For accelerating ML models.


# Models
1. **YOLOv3-tiny**: Pre-trained on the COCO dataset.
2. **MobileNet-SSD**: Lightweight and suitable for embedded systems



# Resources to Review
1. PYNQ Documentation:
   - Official PYNQ documentation for understanding the framework

2. YOLOv3-tiny or MobileNet-SSD:
   - Study their architectures and usage in embedded systems

3. SORT/DeepSORT:
   - Research papers or GitHub repositories for implementation


# Next Steps
1. Set up your hardware (PYNQ-Z2, camera, and monitor)
2. Begin with the software pipeline on your PC (OpenCV + YOLOv3-tiny)
3. Transition the pipeline to PYNQ-Z2 using pre-built overlays
4. Test and integrate object tracking
5. Optimize, finalize, and document
































