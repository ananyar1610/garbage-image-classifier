# Garbage Image Classification using Computer Vision  

## Overview  
This project applies computer vision and deep learning to classify images of waste into predefined categories such as **plastics, paper, glass, metals, and organic matter**.  

The goal is to support efficient waste management by automating the sorting process, reducing human error, and promoting sustainability.  

The model is built using **TensorFlow/Keras** and fine-tuned on a garbage dataset. Architectures like **MobileNetV2** and **EfficientNetB0** are employed for lightweight yet accurate classification. A **Streamlit dashboard** is included to allow users to upload waste images and receive real-time predictions.  

---

## Features  
- Automated classification of garbage images into multiple categories  
- Pre-processing pipeline with resizing, normalisation, and augmentation  
- Transfer learning with MobileNetV2 and EfficientNetB0  
- Streamlit dashboard for interactive image upload and prediction  
- EDA visualisations including class distribution and sample images  

---

## Project Structure  

data/                # Dataset (not included, add your own or link)  
notebooks/           # Jupyter notebooks for EDA and prototyping  
src/                 # Source code (data_loader.py, model.py, utils.py)  
app/                 # Streamlit dashboard (streamlit_app.py)  
saved_models/        # Trained model weights  
requirements.txt     # Dependencies  
README.md            # Project documentation  

---

## Dataset  
The dataset consists of labelled images of waste divided into categories such as **plastics, paper, glass, metals, organic waste, and residual waste**.  
Images are collected under varied lighting, resolution, and backgrounds.  

**Split:**  
- Training set: 80%  
- Validation set: 20%  

If you don’t have the dataset, you can use the [Garbage Classification Dataset on Kaggle]([https://www.kaggle.com](https://www.kaggle.com/datasets/sumn2u/garbage-classification-v2?utm_source=chatgpt.com)).  

---

## Exploratory Data Analysis (EDA)  
- **Class distribution** showed imbalance across categories (plastics and paper dominant).  
- **Sample visualisations** confirmed labelling quality but highlighted noise such as cluttered backgrounds.  
- **Image pre-processing** included resizing, normalisation, and augmentation (rotation, flips, zoom).  

EDA findings informed augmentation strategies and guided model selection for better robustness.  

---
---

## Streamlit Dashboard  

The project includes an interactive **Streamlit dashboard** for real-time garbage image classification. The dashboard provides a simple and intuitive interface where users can upload an image of waste and receive immediate predictions about its category.  

### Key Features  
- **Image Upload**: Drag and drop or browse to upload an image.  
- **Real-Time Prediction**: The model classifies the image into categories such as plastics, paper, glass, metals, or organic matter.  
- **Visual Feedback**: The uploaded image is displayed alongside the predicted category.  
- **Lightweight & Fast**: Powered by transfer learning (MobileNetV2/EfficientNetB0).  

### Run Locally  
To launch the dashboard:  
```bash
streamlit run app/streamlit_app.py
```
---

## Conclusion  

This project demonstrates the effectiveness of **computer vision and deep learning** techniques in tackling real-world waste management challenges. By automating garbage classification, the system has the potential to reduce manual sorting, improve recycling efficiency, and support sustainable practices. The combination of a custom CNN and transfer learning models (MobileNetV2, EfficientNetB0) ensures a balance of performance and efficiency, making the solution practical for deployment in lightweight environments.  

---

## Future Improvements  

Potential directions to further enhance the system include:  

- **Model Fine-Tuning**: Unfreezing pre-trained layers to boost classification accuracy.  
- **Larger Dataset**: Incorporating more diverse and balanced samples across waste categories.  
- **Edge Deployment**: Optimising models for low-power devices like Raspberry Pi or mobile phones.  
- **Explainability**: Adding Grad-CAM visualisations to highlight decision-making regions.  
- **Multi-Label Classification**: Handling mixed waste images with multiple categories.  

---

## Contributing  

Contributions are welcome! To contribute:  

1. **Fork** the repository  
2. **Create a new branch** (`git checkout -b feature-branch`)  
3. **Commit changes** (`git commit -m "Add new feature"`)  
4. **Push to branch** (`git push origin feature-branch`)  
5. **Open a Pull Request**  

Please ensure that your code follows best practices and is well-documented.  

---

## License  

This project is licensed under the **MIT License**.  
You are free to use, modify, and distribute this project with proper attribution.  

---

