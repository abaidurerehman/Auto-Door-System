# 🚪 Facial Recognition Smart Door System with Admin Email Approval

This project is a smart door security system that uses real-time facial recognition to identify known individuals and automatically open the door. If an unknown person is detected, it sends an email to the admin for manual approval. Admins can approve access by clicking the "ALLOW" button in the email.

---

## 📸 Features

- ✅ Real-time face detection and recognition using webcam
- ✅ Automatically opens door for recognized persons
- ✅ Sends email alert to admin for unrecognized persons
- ✅ Admin can approve access via email within 60 seconds
- ✅ Displays name labels and highlights known/unknown faces
- ✅ Uses CSV to store known face encodings and names

---

## 📂 Project Structure

```
face-recognition-door-system/
│
├── face_data.csv           # Stores known face names and encodings
├── face_recognition_main.py  # Main face recognition script
├── README.md               # Project documentation
└── requirements.txt        # Required Python packages
```

---

## ⚙️ Technologies Used

- Python 3.7+
- OpenCV
- face_recognition (dlib)
- smtplib, imaplib (Email handling)
- NumPy, Pandas
- EmailMessage (HTML emails with buttons)

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/abaidurerehman/Auto-Door-System.git
cd face-recognition-door-system
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

> **Note**: You may need to install `dlib` separately based on your OS.

### 3. Add Your Known Faces

Create or update `face_data.csv` file:
- Columns: `Name`, `Encoding`
- Store NumPy arrays of 128-d encodings as strings (comma-separated)

Or modify the script to encode and save faces directly.

### 4. Set Your Admin Email Credentials

In `face_recognition_main.py`, update:

```python
EMAIL_ADDRESS = "your-email@gmail.com"
EMAIL_PASSWORD = "your-app-password"  # Use Gmail App Password
```

> Use Gmail's [App Passwords](https://support.google.com/accounts/answer/185833) if 2FA is enabled.

### 5. Run the Program

```bash
python face_recognition_main.py
```

---

## ✉️ Email Alert Sample

When an unknown person is detected, the admin will receive an email like this:

> Subject: ❌ Unknown Person Detected! Approval Required  
> Message:  
> 📩 An unknown person is detected at the door.  
> ✅ Click the "ALLOW" button to grant access.

---

## 📊 Future Enhancements

- Add GUI for managing known faces
- Integrate with IoT for actual door unlocking
- Use cloud database for storing face data
- Voice assistant for interaction
- Add multi-user role support (e.g., Admin, Security Officer)

---

## 🛡️ License

This project is licensed under the MIT License.  
See the [LICENSE](LICENSE) file for more details.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the project
2. Create a feature branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m 'Add new feature'`
4. Push to the branch: `git push origin feature/my-feature`
5. Submit a pull request

---

## 👨‍💻 Author

**Abaidur-E-Rehman**  


---

## ✅ Optional: `requirements.txt`

```txt
opencv-python
face_recognition
numpy
pandas
```
