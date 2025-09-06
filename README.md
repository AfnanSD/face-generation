# Face Generation with GANs 🧑‍🎨✨

## 📌 Overview

This project is part of the **Udacity Deep Learning Nano Degree** program.
The objective is to build a **custom Generative Adversarial Network (GAN)** capable of generating realistic human face images based on the **CelebA dataset**.

The project demonstrates the **end-to-end GAN workflow**:

* Designing a data preprocessing pipeline
* Implementing custom **Generator** and **Discriminator** networks in PyTorch
* Applying adversarial loss functions and optimizers
* Iteratively training and refining models
* Generating new face samples that resemble real human features

---

## 🛠️ Tech Stack

* Python 3.7+
* PyTorch – deep learning framework
* Torchvision – transforms and dataset utilities
* NumPy, Pandas, Matplotlib – data wrangling & visualization
* Jupyter Notebook – interactive development

---

## 📊 Dataset

* **CelebA Dataset (subset)** – collection of celebrity face images
* Preprocessed to **64x64 RGB tensors**
* Pixel values normalized to **\[-1, 1] range** for stable GAN training

---

## 🚀 Project Workflow

1. **Data Pipeline**

   * Implemented a `get_transform` function with resizing, cropping, normalization
   * Created a custom `DatasetDirectory` class with `__len__` and `__getitem__`

2. **Model Architecture**

   * **Generator**: Takes a latent vector (noise) and outputs a 3-channel RGB image
   * **Discriminator**: Takes an image (real/fake) and outputs a single authenticity score

3. **Loss Functions & Optimization**

   * Adversarial loss functions (Generator vs Discriminator)
   * Low learning rates for stability

4. **Training Strategy**

   * Iterative training with separate steps for Generator and Discriminator
   * Loss values monitored and adjusted
   * Training continues until generated faces show meaningful features (eyes, nose, mouth, hair)

---

## 📈 Results

* Initial outputs: random noise with vague structure
* After several epochs: faces with distinguishable features emerge
* Final samples demonstrate **recognizable human-like faces** with variations in expression and attributes

<img width="799" height="219" alt="sample" src="https://github.com/user-attachments/assets/889d2207-336c-46e0-8216-a9dfc62f6d29" />



## 🎓 Acknowledgements

* Project completed as part of the **Udacity Deep Learning Nano Degree**
* Dataset: [CelebA Dataset](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)
