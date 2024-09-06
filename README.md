# Object Detection using YOLOv8 and Tensorflow.js

---

Object Detection application right in your browser. Serving YOLOv8 in browser using tensorflow.js
with `webgl` backend.

**Setup**

```bash
git clone https://github.com/JoaoGabrielSC/yolotfjs.git
cd yolov10-tfjs
npm install #Install dependencies
```

**Scripts**

```bash
npm start
```

## Model

YOLOv10m model converted to tensorflow.js.

```
used model : yolov10m
size       : 30 Mb
```

**Use another model**

Use another YOLOv8 model.

1. Export YOLOv8 model to tfjs format. Read more on the [official documentation](https://docs.ultralytics.com/tasks/detection/#export)

   ```python
   from ultralytics import YOLO

   # Load a model
   model = YOLO("yolov10m.pt")  # load an official model

   # Export the model
   model.export(format="tfjs")
   ```

2. Copy `yolovX*_web_model` to `./public`
3. Update `modelName` in `App.jsx` to new model name
   ```jsx
   ...
   // model configs
   const modelName = "yolov10*"; // change to new model name
   ...
   ```
4. Done! 😊

**Note: Custom Trained YOLOvx Models**

Please update `src/utils/labels.json` with your new classes.

# References
 - https://github.com/Hyuto/yolov8-tfjs.git
