# 🧠 Fashion Image Recommendation System (NumPy CNN + Flask)

A handcrafted image-based recommendation engine built entirely using **NumPy**, served via a **Flask API**, and integrated into the **Style Studio** fashion app.
Style Studio app Repo-[https://github.com/Ananyasolanki123/StyleStudio]

Upload an image of a dress, sketch, or outfit — and the model finds the most visually similar item from a preloaded dataset.  
No TensorFlow. No PyTorch. Just clean logic and layers.

---

## 🚀 Features

- ✅ Custom Convolutional Neural Network (CNN) built from scratch using NumPy
- ✅ Cosine similarity for image embedding comparison
- ✅ Works with grayscale or converted images (28×28 input)
- ✅ Flask API endpoint for real-time recommendations
- ✅ Integrated with FlutterFlow frontend in Style Studio app
- ✅ Google Colab-compatible training and testing

---

## 🏗️ Architecture Overview

1. **Training Phase (Colab)**  
   - Loads and preprocesses MNIST (or Fashion-MNIST)
   - Initializes CNN layers manually (Conv → ReLU → Pool → Dense)
   - Trains on image-label pairs
   - Precomputes feature vectors for all catalog items

2. **Inference Phase (API)**  
   - Accepts an uploaded image via `/recommend` endpoint
   - Preprocesses and embeds the image using trained CNN
   - Finds the most visually similar image using cosine similarity
   - Returns the best match (as an image or base64)

---

## 🧰 Tech Stack

| Group           | Tools/Libraries                             |
|----------------|---------------------------------------------|
| ML Core         | NumPy, Matplotlib, PIL                      |
| Serving Layer   | Flask (REST API)                            |
| UI Integration  | FlutterFlow (frontend), Colab (debugging)   |
| Dataset         | MNIST (prototyping), Fashion-MNIST (planned)|
| Utilities       | Google Colab, GitHub                        |

---

## ⚙️ How to Run

### 🧪 Training & Testing (Google Colab)

1. Load the notebook
2. Train the CNN model on MNIST/Fashion-MNIST
3. Precompute feature vectors

# Install dependencies
pip install flask pillow numpy

# Run the app
python app.py

http://localhost:5000/recommend

📦 API Endpoint
POST /recommend
Upload an image file as form-data (image)
Returns: JSON with:

match_base64: base64 encoded closest-match image

score: similarity score (0–1)

📌 Future Improvements
Add support for color images and larger input sizes

Upgrade dataset to Fashion-MNIST / DeepFashion

Add Top-3 matches instead of one

Store results in Firebase for persistent UX

WebSocket or async Flask version for batch calls

🤝 Contributing
Pull requests are welcome. For major changes, open an issue first to discuss what you’d like to add.

📄 License
This project is for educational and prototyping purposes. Feel free to fork or build upon it with attribution.

✨ Built With Love for Style Studio
This recommender powers the Style Studio app — matching outfits to your inspiration, sketch, or wardrobe style.
Proudly handcrafted — one matrix multiplication at a time.   
