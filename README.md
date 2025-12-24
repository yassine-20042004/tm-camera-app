Road Cleanliness Classification
CNN Image Classifier (Teachable Machine + TensorFlow.js)
📌 Project Overview

This project uses a Convolutional Neural Network (CNN) trained with Google Teachable Machine to classify road images into two categories:

🟢 Clean Road

🔴 Dirty Road

The trained model is exported in TensorFlow.js format and can be easily integrated into any HTML web page using the provided API.

🎯 Objectives

Detect road cleanliness using image classification

Provide a ready-to-use AI model accessible via web

Enable developers to integrate the model into their own applications

Demonstrate the use of Teachable Machine + TensorFlow.js

🧠 Model Information

Model type: Image Classification (CNN)

Training tool: Google Teachable Machine

Framework: TensorFlow.js

Output classes:

Clean

Dirty

The model learns visual features such as:

Trash presence

Road texture

Irregular patterns and objects

📂 Project Structure
road-cleanliness-model/
│
├── model/
│   ├── model.json
│   ├── weights.bin
│
├── index.html
├── script.js
├── tm-image.min.js
└── README.md

🖼️ Dataset

Images of roads captured in real environments

Two classes:

Clean roads

Dirty roads

Images were uploaded and labeled directly in Teachable Machine

⚠️ Dataset quality directly impacts model performance.

🌐 How to Use the Model (HTML Integration)
1️⃣ Include TensorFlow.js & Teachable Machine
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@latest"></script>
<script src="https://cdn.jsdelivr.net/npm/@teachablemachine/image@latest"></script>

2️⃣ Load the Model
const URL = "model/";

const modelURL = URL + "model.json";
const metadataURL = URL + "metadata.json";

const model = await tmImage.load(modelURL, metadataURL);

3️⃣ Make Predictions
const prediction = await model.predict(imageElement);
console.log(prediction);


Output example:

[
  { "className": "Dirty", "probability": 0.92 },
  { "className": "Clean", "probability": 0.08 }
]

📷 Supported Inputs

Webcam

Uploaded images

Mobile camera

Static image files

🚀 Deployment

The model can be deployed using:

GitHub Pages

Any static web server

Local browser execution

No backend is required.

🌍 Use Cases

Smart city road monitoring

Environmental cleanliness analysis

AI-assisted urban maintenance

Educational AI demonstrations

⚖️ Ethical Considerations

Model predictions depend on training data quality

Potential bias due to lighting or weather conditions

Should not be used as a sole decision-maker in public safety

Transparency and human supervision are recommended

📌 Limitations

Binary classification only (clean vs dirty)

No object localization (no bounding boxes)

Performance may vary with image quality

🔮 Future Improvements

Upgrade to object detection (trash localization)

Improve dataset diversity

Add confidence threshold handling

Mobile-first optimization

👤 Author

Developed for educational and experimental purposes.

📄 License

Open-source project for learning and demonstration use.
