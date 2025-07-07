# Facial Recognition Glasses for Visually Challenged Persons

This project enables real-time facial recognition using the **ESP32-CAM module**, with face data stored on **Firebase**. It is designed to assist visually challenged individuals by identifying known faces and conveying their identities through audio notifications on a connected mobile app.

---

## 💡 Features

- 📸 Face detection using ESP32-CAM
- ☁️ Face image storage and retrieval using Firebase
- 🔊 Audio output via mobile app ("Keerthi is coming")
- 🖥️ Real-time processing and output on a laptop screen
- 🔌 ESP32-CAM powered through external supply and connected via WiFi

---

## 🧠 How It Works

1. **Connect ESP32-CAM and Laptop to the Same WiFi Network**  
   Ensure both devices are on the same network for communication.

2. **Run `face_detection.py`**  
   - This Python script opens a command prompt window.
   - It will ask for the ESP32-CAM streaming URL.
   - Once entered, it starts capturing face images.

3. **Image Processing**  
   - Captured faces are matched with images stored in Firebase.
   - You must create an `images` folder in the project directory to store local images temporarily.

4. **Audio Output**  
   - If a face matches, the name is displayed on the screen.
   - The mobile app plays an audio message like:  
     _"Keerthi is coming"_, based on the name stored with the face.

---

## 🔧 Requirements

- ESP32-CAM module (powered externally)
- Firebase project (Firestore + Storage)
- Python 3.x
- OpenCV
- Firebase Admin SDK
- Mobile app (for audio output – preconfigured to receive events)

---

## 📁 Project Structure

```

Facial-Recognition-Glasses/
│
├── face\_detection.py         # Main script to detect and match faces
├── firebase\_config.py        # Firebase connection & setup
├── images/                   # Folder to store reference face images
└── mobile\_app/               # (Optional) Folder containing mobile app source

````

> ⚠️ **Important:** Make sure to create the `images` folder before running the script.

---

## 🚀 Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/Keerthi-gatla/Facial-Recognition-Glasses-for-Visually-Challenged-Persons.git
   cd Facial-Recognition-Glasses-for-Visually-Challenged-Persons
````

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Set up Firebase credentials in `firebase_config.py`.

4. Create an `images/` folder inside the project directory.

5. Run the application:

   ```bash
   python face_detection.py
   ```

---

## 📷 ESP32-CAM URL

* Format: `http://<ESP32-CAM-IP-ADDRESS>`
* You will be prompted to enter this when you run the script.

---

## 📱 Mobile App Integration

* The mobile app is built to:

  * Listen for identified faces
  * Play audio notifications like: *"Keerthi is coming"*
* Firebase is used as the bridge between Python and the mobile app.

---

## ✅ To Do

* [ ] Add support for multiple user profiles
* [ ] Improve recognition accuracy using embeddings
* [ ] Push real-time notifications
* [ ] Upload mobile app code to this repo

---

## 🤝 Contributors

* **Keerthi Gatla** – Developer
  (Project done as part of academic work)

---

## 📜 License

This project is licensed under the MIT License.

