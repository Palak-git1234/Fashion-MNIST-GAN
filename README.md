# Fashion-MNIST GAN

Fashion image generation using a Generative Adversarial Network (GAN) with TensorFlow.

## 📌 Project Overview

This project demonstrates how a Generative Adversarial Network (GAN) can generate new fashion-like images using the Fashion-MNIST dataset.

A GAN consists of two neural networks:

- **Generator:** Creates fake images from random noise.
- **Discriminator:** Determines whether an image is real or fake.

The Generator and Discriminator are trained together. The Generator tries to create realistic images, while the Discriminator tries to distinguish real images from fake ones.

## 📊 Dataset

This project uses the **Fashion-MNIST** dataset.

- 60,000 training images
- 10,000 test images
- Image size: 28 × 28 pixels
- Grayscale images
- 10 fashion categories

The dataset is loaded automatically using TensorFlow/Keras.

## 🧠 GAN Architecture

### Generator

The Generator takes a 100-dimensional random noise vector and gradually transforms it into a 28 × 28 grayscale image.

```text
Random Noise (100 values)
        ↓
    Dense Layer
        ↓
    7 × 7 × 128
        ↓
      Reshape
        ↓
    7 × 7 Feature Map
        ↓
  Conv2DTranspose
        ↓
      14 × 14
        ↓
  Conv2DTranspose
        ↓
     28 × 28 × 1
        ↓
   Generated Image
```
Discriminator

The Discriminator takes a 28 × 28 grayscale image and produces a score indicating whether the image is real or fake.
```text
28 × 28 × 1 Image
        ↓
      Conv2D
        ↓
      14 × 14
        ↓
      Conv2D
        ↓
       7 × 7
        ↓
     Flatten
        ↓
     Dense(1)
        ↓
   Real/Fake Score
```

⚙️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Fashion-MNIST

🔄 Training Process

- The Generator creates fake images from random noise.
- The Discriminator receives real and fake images.
- The Discriminator learns to distinguish real images from fake images.
- The Generator learns to create images that can fool the Discriminator.
- Both networks are updated using backpropagation and Adam optimization.
- The model is trained for 20 epochs.

📈 Results

The project visualizes:
- Real Fashion-MNIST images
- Untrained Generator output
- Generator progress during training
- Discriminator confidence
- Real vs. generated fashion images

The same random noise is used for selected epochs to observe how the Generator's output changes during training.

🚀 How to Run

- Download or clone this repository.
- Open Fashion_MNIST_GAN.ipynb.
- Run the notebook using Jupyter Notebook, Google Colab, or Kaggle.
- Run the cells in order.
- The Fashion-MNIST dataset will be loaded automatically through TensorFlow/Keras.

🎯 Learning Objective

The main objectives of this project are:
- Understand how Generative Adversarial Networks work.
- Understand how a Generator creates new images.
- Understand how a Discriminator identifies real and fake images.
- Understand how both networks learn through adversarial training.

🔮 Future Improvements
- Train the GAN for more epochs.
- Use a deeper DCGAN architecture.
- Improve generated image quality.
- Experiment with different hyperparameters.
- Test the model on other image datasets.

Author

Palak
MSc Artificial Intelligence
