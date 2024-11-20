# speed estimation

[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/khulnasoft-ai/notebooks/blob/main/notebooks/how-to-estimate-vehicle-speed-with-computer-vision.ipynb)
[![YouTube](https://badges.aleen42.com/src/youtube.svg)](https://youtu.be/uWP6UjDeZvY)

## 👋 hello

This example performs speed estimation analysis using various object-detection models
and ByteTrack - a simple yet effective online multi-object tracking method. It uses the
metavision package for multiple tasks such as tracking, annotations, etc.

https://github.com/khulnasoft/metavision/assets/26109316/d50118c1-2ae4-458d-915a-5d860fd36f71

> \[!IMPORTANT\]
> Adjust the [`SOURCE`](https://github.com/khulnasoft/metavision/blob/e32b05a636dab2ea1f39299e529c4b22b8baa8da/examples/speed_estimation/ultralytics_example.py#L10)
> and [`TARGET`](https://github.com/khulnasoft/metavision/blob/e32b05a636dab2ea1f39299e529c4b22b8baa8da/examples/speed_estimation/ultralytics_example.py#L15)
> configuration if you plan to run a speed estimation script on your video file. Those must be adjusted separately for each camera view. You can learn more
> from our YouTube [tutorial](https://youtu.be/uWP6UjDeZvY).

## 💻 install

- clone repository and navigate to example directory

  ```bash
  git clone https://github.com/khulnasoft/metavision.git
  cd metavision/examples/speed_estimation
  ```

- setup python environment and activate it \[optional\]

  ```bash
  python3.10 -m venv venv
  source venv/bin/activate
  ```

- install required dependencies

  ```bash
  pip install -r requirements.txt
  ```

- download `vehicles.mp4` file

  ```bash
  python3.10 video_downloader.py
  ```

## 🛠️ script arguments

- `--khulnasoft_api_key` (optional): The API key for Khulnasoft services. If not provided
  directly, the script tries to fetch it from the `KHULNASOFT_API_KEY` environment
  variable. Follow [this guide](https://docs.khulnasoft.com/api-reference/authentication#retrieve-an-api-key)
  to acquire your `API KEY`.

- `--model_id` (optional): Designates the Khulnasoft model ID to be used. The default
  value is `"yolov8x-1280"`.

- `--source_weights_path`: Required. Specifies the path to the YOLO model's weights
  file, which is essential for the object detection process. This file contains the
  data that the model uses to identify objects in the video.

- `--source_video_path`: Required. The path to the source video file that will be
  analyzed. This is the input video on which traffic flow analysis will be performed.

- `--target_video_path`: The path to save the output video with
  annotations. If not specified, the processed video will be displayed in real-time
  without being saved.

- `--confidence_threshold` (optional): Sets the confidence threshold for the YOLO
  model to filter detections. Default is `0.3`. This determines how confident the
  model should be to recognize an object in the video.

- `--iou_threshold` (optional): Specifies the IOU (Intersection Over Union) threshold
  for the model. Default is 0.7. This value is used to manage object detection
  accuracy, particularly in distinguishing between different objects.

## ⚙️ run

- yolo-nas

  ```bash
  python yolo_nas_example.py \
      --source_video_path data/vehicles.mp4 \
      --target_video_path data/vehicles-result.mp4 \
      --confidence_threshold 0.3 \
      --iou_threshold 0.5
  ```

- inference

  ```bash
  python inference_example.py \
      --khulnasoft_api_key <KHULNASOFT API KEY> \
      --source_video_path data/vehicles.mp4 \
      --target_video_path data/vehicles-result.mp4 \
      --confidence_threshold 0.3 \
      --iou_threshold 0.5
  ```

- ultralytics

  ```bash
  python ultralytics_example.py \
      --source_video_path data/vehicles.mp4 \
      --target_video_path data/vehicles-result.mp4 \
      --confidence_threshold 0.3 \
      --iou_threshold 0.5
  ```

## © license

This demo integrates two main components, each with its own licensing:

- ultralytics: The object detection model used in this demo, YOLOv8, is distributed
  under the [AGPL-3.0 license](https://github.com/ultralytics/ultralytics/blob/main/LICENSE).
  You can find more details about this license here.

- metavision: The analytics code that powers the zone-based analysis in this demo is
  based on the Metavision library, which is licensed under the
  [MIT license](https://github.com/khulnasoft/metavision/blob/develop/LICENSE.md). This
  makes the Metavision part of the code fully open source and freely usable in your
  projects.
