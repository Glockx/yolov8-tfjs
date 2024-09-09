# Object Detection using YOLOv8 and Tensorflow.js

<p align="center">
  <img src="./sample.png" />
</p>

![tensorflow.js](https://img.shields.io/badge/tensorflow.js-white?logo=tensorflow)

---

Object Detection application right in your browser. Serving YOLOv8 in browser using tensorflow.js
with `webgl` backend.

**Setup**

```bash
#Install dependencies
yarn install
```

**Scripts**

```bash
# Start dev server
yarn start
```

# Use another model

Use another YOLOv8 model.

1. Export YOLOv8 model to tfjs format. Read more on the [official documentation](https://docs.ultralytics.com/tasks/detection/#export)

   ```python
   from ultralytics import YOLO

   # Load a model
   model = YOLO("yolov8n.pt")  # load an official model

   # Export the model
   model.export(format="tfjs")
   ```

2. Delete previous model files in `./public/yolov8n_web_model`
3. Copy new model's TF.js files to `./public/yolov8n_web_model`
4. Done! 😊

**Note: Custom Trained YOLOv8 Models**

Please update `src/utils/labels.json` with your new classes.
