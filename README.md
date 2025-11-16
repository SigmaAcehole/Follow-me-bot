# Follow-me bot
This repository demonstrates the concept of a "Follow-me" robot that can locate a person of interest (or the user) and keep following them from a safe distance. The person of interest is located with a bounding box and tracked even when obstructed with obstacles or other humans. The distance of the person from the camera is computed and displayed below the bounding box.

![Model output visualization](demo.gif)  

**Deep learning models utilized**
- **[YOLOv8](https://docs.ultralytics.com/models/yolov8/)**: A single-stage object detection network that was pre-trained to detect multiple objects including humans.
- **[MiDAS](https://github.com/isl-org/MiDaS)**: A monocular depth estimation network that was pre-trained to compute relative depth of image pixels.
- **[DeepSORT](https://github.com/nwojke/deep_sort)**: An object tracking algorithm that uses deep learning based appearance descriptors and Kalman Filter to track an object accurately even when obstructed by obstacles.


**Quick Start**
- **Prerequisites**: Python 3.8+, PyTorch and jupyterlab.

**Running the notebook**
- Start Jupyter and run the `follow_me_robot.ipynb` notebook.


**Notes & Tips**
- MiDaS model weights are downloaded automatically by the notebook during the first run. If running offline, download the weights in advance and point the notebook to the local path.
- For best performance on larger images use a machine with a GPU and install a CUDA-enabled build of PyTorch.
