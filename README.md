# Fashion-MNIST-GAN
Fashion image generation using a Generative Adversarial Network (GAN) with TensorFlow.

## 📌 Project Overview
This project demonstrates how a Generative Adversarial Network (GAN) can learn to generate new fashion-like images using the Fashion-MNIST dataset.
The GAN consists of two neural networks:

- **Generator** – creates fake fashion images from random noise.
- **Discriminator** – determines whether an image is real or generated.
  
Both networks are trained together in a competitive process. As training progresses, the Generator learns to create more realistic images while the Discriminator learns to distinguish real images from generated ones.

## 📊 Dataset
The project uses the **Fashion-MNIST** dataset.
- 60,000 training images
- 10,000 test images
- Image size: 28 × 28 pixels
- Grayscale images
- 10 fashion categories
The dataset is loaded directly using TensorFlow/Keras.

## 🧠 GAN Architecture
### Generator
The Generator takes a random noise vector of 100 values as input and gradually increases the image size:

100-dimensional Noise → Dense Layer  → 7 × 7 × 128  →  Reshape  → 7 × 7  →  14 × 14  → 28 × 28 × 1 → Generated Fashion Image

### Discriminator
The Discriminator takes a 28 × 28 grayscale image and gradually reduces it to a single real/fake score:

28 × 28 × 1 Image →  Convolution → 14 × 14  → Convolution  →  7 × 7   →  Flatten  →  Real/Fake Score

⚙️ Technologies Used

-Python
-TensorFlow
-Keras
-NumPy
-Matplotlib
-Fashion-MNIST

🔄 Training Process

-The Generator creates fake images from random noise.
-The Discriminator receives both real and fake images.
-The Discriminator learns to identify real and fake images.
-The Generator learns to create images that can fool the Discriminator.
-This process continues for multiple epochs.
The model is trained for 20 epochs.

📈 Results

The project visualizes:

-Real Fashion-MNIST images
-Untrained Generator output
-Generator progress during training
-Discriminator confidence
-Real vs. generated fashion images
The same random noise is used for selected epochs to observe how the Generator's output improves during training.

🚀 How to Run

-Clone or download this repository.
-Open Fashion_MNIST_GAN.ipynb in Jupyter Notebook, JupyterLab, Google Colab, or Kaggle.
-Run the notebook cells in order.
-The Fashion-MNIST dataset will be loaded automatically through TensorFlow/Keras.

🎯 Learning Objective

The main objective of this project is to understand:

-How Generative Adversarial Networks work.
-How a Generator creates new images.
-How a Discriminator identifies real and fake images.
-How both networks learn through adversarial training.

🔮 Future Improvements

Possible improvements include:

-Training for more epochs.
-Using a deeper DCGAN architecture.
-Improving image quality.
-Experimenting with different hyperparameters.
Using other image datasets.

👩‍💻 Author

-Palak
MSc Artificial Intelligence
