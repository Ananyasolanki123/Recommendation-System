# 🧠 Fashion Image Recommendation System (NumPy CNN)

A handcrafted image-based recommendation engine built entirely using **NumPy**, served via a **Flask API**, and integrated into the **Style Studio** fashion app.

Upload an image of a dress, sketch, or outfit — and the model finds the most visually similar item from a preloaded dataset.  
No TensorFlow. No PyTorch. Just clean logic and layers.
---

### 📥 Download Datasets (Google Drive)

| Dataset         | Description                   | Drive Link                                                                     |
|-----------------|-------------------------------|--------------------------------------------------------------------------------|
| Train_images.zip| Fashion-MNIST training images | [Link](https://drive.google.com/file/d/11UFr3YwO5XH0h6na7NigjNwg9PyaabIQ/view) |
| t10k_images.zip | Fashion-MNIST training images | [Link](https://drive.google.com/file/d/119Y3tZlfwXlZnynO5_lkWRIs6DpALhfm/view) |
|Train_labels.zip | Fashion-MNIST train labels    | [Link](https://drive.google.com/file/d/117sAuayr51xIphdtRy2QgC2T7zu0ztRN/view) |
| t10k_labels.zip | Fashion-MNIST test labels     | [Link](https://drive.google.com/file/d/117YGlvjB2IGsz4sWBO3RTDKy7ASWBaUR/view) |

---

## 🚀 Features

- ✅ Custom Convolutional Neural Network (CNN) built from scratch using NumPy
- ✅ Cosine similarity for image embedding comparison
- ✅ Works with grayscale or converted images (28×28 input)
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
   - Accepts an uploaded image 
   - Preprocesses and embeds the image using trained CNN
   - Finds the most visually similar image using cosine similarity
   - Returns the best match (as an image or base64)

---

## 🧰 Tech Stack

| Group           | Tools/Libraries                             |
|----------------|---------------------------------------------|
| ML Core         | NumPy, Matplotlib, PIL                      |
| UI Integration  | FlutterFlow (frontend), Colab (debugging)   |
| Dataset         | MNIST (prototyping), Fashion-MNIST (planned)|
| Utilities       | Google Colab, GitHub                        |

---

## ⚙️ How to Run

### 🧪 Training & Testing (Google Colab)

1. Load the notebook
2. Train the CNN model on MNIST/Fashion-MNIST dataset provided in readme.
3. Precompute feature vectors
4.Returns with:
match_base64: base64 encoded closest-match image
score: similarity score (0–1)

📌 Future Improvements
Add support for color images 

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
