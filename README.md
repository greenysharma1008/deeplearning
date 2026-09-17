# Deep Learning Practical: Fashion Image Classification

## Overview

This practical introduces **Deep Learning and Artificial Neural Networks** through a simple fashion product image classification project.

The project uses the **Fashion MNIST dataset** to train a neural network that can classify product images into 10 different fashion categories.

The practical connects Deep Learning concepts with a real-world **e-commerce business scenario**, where AI can assist with automatically categorizing product images.

---

## Business Scenario

An e-commerce company receives thousands of product images every day.

Manually identifying and categorizing every product can require significant time and effort. A Deep Learning model can assist employees by automatically predicting the category of a product from its image.

### Example Categories

* T-shirt / Top
* Trouser
* Pullover
* Dress
* Coat
* Sandal
* Shirt
* Sneaker
* Bag
* Ankle Boot

### Business Workflow

**Product Image → Deep Learning Model → Predicted Category → Human Review → Product Listing**

---

## Learning Objectives

By completing this practical, we learn how to:

* Use images as input for a Deep Learning model.
* Load and explore the Fashion MNIST dataset.
* Build a simple Artificial Neural Network.
* Understand input, hidden, and output layers.
* Prepare image data for training.
* Train a neural network using labelled images.
* Evaluate model accuracy.
* Use a trained model to make predictions.
* Connect AI predictions with an e-commerce business use case.
* Understand the importance of human review and model limitations.

---

## Dataset

The practical uses the **Fashion MNIST** dataset provided through TensorFlow/Keras.

The dataset contains grayscale images of fashion products.

Each image is:

* **28 × 28 pixels**
* Grayscale
* Associated with one of **10 product categories**

The dataset is downloaded automatically when the notebook is executed.

---

## Model Architecture

A simple Artificial Neural Network is used:

```text
Input Image
     ↓
Flatten Layer
     ↓
Dense Hidden Layer
     ↓
Output Layer
     ↓
Predicted Product Category
```

### Model Components

| Component | Purpose                                                                |
| --------- | ---------------------------------------------------------------------- |
| Flatten   | Converts the 28 × 28 image into a form suitable for the neural network |
| Dense(64) | Hidden layer that learns useful patterns                               |
| ReLU      | Activation function used in the hidden layer                           |
| Dense(10) | Produces an output for each of the 10 categories                       |
| Softmax   | Produces probabilities for the possible categories                     |

---

## Data Preparation

The original image pixel values range from **0 to 255**.

The practical normalizes these values to a range between **0 and 1**:

```text
Original pixel values → 0–255

Normalized values → 0–1
```

This makes the image data easier for the neural network to process.

---

## Training

The model is trained using the training images and their known labels.

The practical uses:

* **3 epochs**
* **10% validation split**
* Adam optimizer
* Sparse categorical cross-entropy loss
* Accuracy as the evaluation metric

An **epoch** means that the model has processed the training dataset once.

---

## Model Evaluation

After training, the model is evaluated using the test dataset.

The notebook displays the test accuracy:

```text
Test Accuracy: XX.XX %
```

The exact accuracy may vary slightly depending on the training process and environment.

### Understanding Accuracy

For example, if the model achieves **87% accuracy**, approximately 87 out of every 100 test images were classified correctly.

However, accuracy alone does not determine whether an AI system is ready for business deployment.

A company should also consider:

* Cost of incorrect classifications
* Customer experience
* Quality of training data
* Human review requirements
* Business impact of errors

---

## Prediction

The trained model can be used to predict the category of an unseen product image.

The notebook compares:

```text
Predicted Product
        vs.
Actual Product
```

For example:

```text
Predicted Product: Sneaker
Actual Product: Sneaker
```

Students can also change the image number to test different products.

---

## Business Application

### Traditional Process

```text
Product Image
     ↓
Employee manually identifies product
     ↓
Employee selects category
     ↓
Product is listed
```

### AI-Assisted Process

```text
Product Image
     ↓
Deep Learning Model
     ↓
Predicted Category
     ↓
Employee Review
     ↓
Product Listing
```

---

## Possible Business Benefits

A fashion e-commerce company could potentially use image classification to:

* Speed up product listing
* Reduce repetitive manual work
* Improve consistency in product categorization
* Support product search
* Process large numbers of product images
* Assist employees with routine classification tasks

These benefits depend on the quality and reliability of the deployed system.

---

## Limitations

The model may sometimes make incorrect predictions.

Possible reasons include:

* Similar-looking product categories
* Limited image information
* Differences between training and real-world images
* Insufficient or biased training data
* Model limitations

For a real business system, incorrect classifications could affect product listings, search results, recommendations, or customer experience.

Human review can therefore remain important, particularly for uncertain or high-impact predictions.

---

## Student Activities

The practical asks students to:

1. Identify the input given to the Deep Learning model.
2. Identify the output produced by the model.
3. Explain the role of the hidden layer.
4. Identify the activation function used in the hidden layer.
5. Record the test accuracy.
6. Find an image that was classified correctly.
7. Find an image that was classified incorrectly.
8. Explain the possible business impact of incorrect categorization.
9. Identify where human review could be useful.
10. Suggest another business problem where image classification could be applied.

---

## Key Concepts

### Deep Learning

Deep Learning uses neural networks with multiple computational layers to learn patterns from data.

### Artificial Neural Network

A neural network consists of interconnected layers that transform input data into an output prediction.

### Training

Training allows the model to learn patterns from labelled examples.

### Testing

Testing evaluates how well the trained model performs on previously unseen data.

### Classification

Classification assigns an input to one of several predefined categories.

### Prediction

Prediction is the model's estimated category for a new image.

---

## Technologies Used

* **Python**
* **TensorFlow**
* **Keras**
* **NumPy**
* **Matplotlib**
* **Google Colab**

---

## Files

Suggested repository structure:

```text
part-a/
└── deep-learning/
    ├── Deep_Learning_Fashion_Classification_Name.ipynb
    ├── README.md
    └── prediction-screenshot.png
```

---

## How to Run

1. Open the `.ipynb` notebook in Google Colab.
2. Run the cells from top to bottom.
3. Allow Fashion MNIST to download automatically.
4. Observe the sample product images.
5. Train the neural network.
6. Record the test accuracy.
7. Test different image numbers.
8. Identify at least one correct prediction.
9. Try to find an incorrect prediction.
10. Take a screenshot showing:

* Product image
* Predicted category
* Actual category

11. Add the screenshot to the repository.

---

## Submission

Rename the notebook as:

```text
Deep_Learning_Fashion_Classification_Name.ipynb
```

Upload the notebook and prediction screenshot to:

```text
part-a/deep-learning/
```

### Required Screenshot

The screenshot should show:

* A fashion product image
* Predicted product category
* Actual product category

---

## Final Takeaways

* Images can be used as input for Deep Learning models.
* Neural networks learn patterns from training examples.
* A model can classify images into predefined product categories.
* Test data helps evaluate model performance on unseen examples.
* Predictions are not always correct.
* Business deployment requires consideration of accuracy, risks, data quality, and human oversight.
* AI can assist employees without necessarily replacing the human review process.
