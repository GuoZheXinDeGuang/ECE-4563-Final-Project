# ECE-4563-Final-Project
This project is done by Leyang Wang, Zihan Liu, and David Jiang, in Fall 2024.

Our goal aims to utilize our learnings from Intro to Machine Learning, taught by Prof. Sandeep Rangan, to predict weather using past data.

The design is to preict weather using given data of percipation, temperature, and wind on that day. Our goal for this project is to find a good canidate that is suitable for weather prediction. In the future, we may consider actually predicting future weather based on past data.

The source of our data is provided below, and we prefered this dataset for its simplicity, while giving a reasonble span in time frame (amount of data).

### Source of Data
Our dataset came from Kaggle, titled [seattle-weather](https://www.kaggle.com/datasets/mahdiehhajian/seattle-weather), uploaded by user `MAHDIEH HAJIAN`.

### Project Summary

#### Formulation
- **Problem Statement**: The problem was clearly defined, focusing on evaluating machine learning models (Neural Networks, SVM, Logistic Regression) for classification tasks.
- **Objective Alignment**: The formulation tied directly to the goal of identifying the best model and hyperparameter configurations for the dataset.

#### Approach
- **Neural Network**: A multi-epoch training was conducted with regular accuracy evaluations on training and testing datasets. Overfitting was analyzed based on the performance gap.
- **SVM**: Various kernels (linear, polynomial, RBF, sigmoid) were tested with multiple `C` values to identify the best combination for accuracy.
- **Logistic Regression**: Tested across a range of regularization strengths (`C`) with attention to convergence warnings for large values.

#### Evaluation and Interpretation
- **Testing Methodology**: Comprehensive testing was conducted for all models, ensuring accuracy metrics were evaluated consistently.
- **Alternative Approaches**: The performance of different kernel functions and regularization strengths highlighted the best and worst methods for the dataset.
- **Data Usage**: No explicit mention of data preprocessing or augmentation, which could improve model generalization.


## Summary of Result

### Neural Network Training Summary

### Training and Testing Performance:
- The training accuracy improved steadily during the initial epochs but plateaued after epoch 30, reaching an average of around **85%** by the end.
- Test accuracy fluctuated slightly but showed a similar plateauing effect around **82%-83%** after epoch 40.
- There was a notable performance gap between training and testing accuracy in the earlier epochs, which reduced over time but indicated slight overfitting.

### Key Observations:
- Early epochs saw consistent improvement in both train and test accuracy, reflecting effective learning.
- Overfitting became evident after epoch 10 as the training accuracy continued to rise, while test accuracy plateaued.
- Final results indicate that the model could benefit from regularization techniques or additional data augmentation to enhance generalization.

---

### SVM Results

### Kernel and Parameter Analysis:
- **Linear kernel** performed best with larger values of `C`:
  - Best accuracy: **82.93%** with `C=10.0`.
- **Polynomial kernel** showed relatively poor performance:
  - Best accuracy: **75.42%** with `C=10.0`.
- **RBF kernel** achieved moderate results:
  - Best accuracy: **79.52%** with `C=10.0`.
- **Sigmoid kernel** consistently performed the worst:
  - Best accuracy: **70.31%** with `C=0.1`.

### Key Observations:
- The **linear kernel** is well-suited for the dataset, indicating that the data is linearly separable.
- Poor performance of the **sigmoid kernel** suggests it is less appropriate for this dataset.
- The polynomial kernel may overfit with higher degrees, as evidenced by lower performance.

---

### Logistic Regression Results

### Performance Across `C` Values:
- Increasing the value of `C` led to higher accuracy, but diminishing returns were observed:
  - **Best accuracy:** **83.28%** for `C=1`, `C=10`, and `C=100`.
- Convergence issues arose for large `C` values, as indicated by warnings to increase `max_iter` or scale the data.

In sum, the results of the Neural Network, SVM, and Logistic Regression were very similar, with all three models achieving accuracy levels around **82%-85%**. This suggests that all three approaches performed comparably well on this dataset, with no significant difference in their final outcomes.











