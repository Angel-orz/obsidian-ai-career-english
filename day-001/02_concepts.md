# Supervised Learning

## Definition (English)
Supervised Learning is a type of machine learning where a model learns to map inputs to outputs by training on a dataset of labeled examples. Each training example consists of an input (features) and the correct output (label). The model learns the underlying function `f(x) = y` by minimizing the error between its predictions and the true labels.

## Chinese Explanation
监督学习是机器学习的一种类型，模型通过在标注数据集上训练来学习从输入到输出的映射。每个训练样本包含输入（特征）和正确的输出（标签）。模型通过最小化预测值与真实标签之间的误差来学习底层函数 f(x) = y。

## German Explanation
Überwachtes Lernen ist eine Art des maschinellen Lernens, bei der ein Modell durch Training auf einem beschrifteten Datensatz lernt, Eingaben auf Ausgaben abzubilden. Jedes Trainingsbeispiel besteht aus einer Eingabe (Merkmale) und der richtigen Ausgabe (Label). Das Modell lernt die zugrundeliegende Funktion f(x) = y, indem es den Fehler zwischen seinen Vorhersagen und den wahren Labels minimiert.

## Intuition
Think of teaching a child to identify animals. You show pictures and say "this is a dog" or "this is a cat." After seeing many labeled examples, the child learns to distinguish them. Supervised learning works the same way: the algorithm is the child, the labeled images are the flashcards, and the "supervision" is the correct answers telling it when it's right or wrong.

The key insight: **the algorithm doesn't need to be explicitly programmed with rules** (e.g., "dogs have floppy ears"). It discovers the patterns from data.

## How It Works

### Step 1: Collect Labeled Data
Gather a dataset where each input has a known correct output. Example: 10,000 house listings with features (size, location, bedrooms) and labels (sale price).

### Step 2: Split the Data
Divide into three sets:
- **Training set (60-80%)**: Used to teach the model
- **Validation set (10-20%)**: Used to tune hyperparameters and check for overfitting during training
- **Test set (10-20%)**: Used only at the end to evaluate final performance

### Step 3: Choose a Model
Select an algorithm based on the problem type:
- Classification → Logistic Regression, Decision Trees, SVM
- Regression → Linear Regression, Random Forest, Gradient Boosting

### Step 4: Train the Model
Feed training data through the model. The model makes predictions, the loss function computes the error, and an optimization algorithm (like Gradient Descent) adjusts the model parameters to reduce this error. This repeats for many iterations (epochs).

### Step 5: Validate and Tune
Use the validation set to monitor performance. If validation error starts increasing while training error keeps decreasing → overfitting detected. Adjust hyperparameters accordingly.

### Step 6: Test
Evaluate on the test set exactly once. This gives the unbiased estimate of real-world performance.

## Real-world Example

**Spam Detection (Classification)**
- Input: Email content, sender, subject line
- Label: "Spam" or "Not Spam"
- Training data: Millions of emails that users have manually marked as spam
- Result: Gmail catches 99.9% of spam using supervised learning

**House Price Prediction (Regression)**
- Input: Square meters, number of rooms, location, building year
- Label: Sale price in Euros
- Training data: Historical property sales records
- Result: ImmobilienScout24 and similar platforms use this for price estimates

**Medical Diagnosis**
- Input: Patient symptoms, lab results, medical images
- Label: Disease present or not
- Training data: Historical patient records with confirmed diagnoses
- Result: Models can detect certain cancers from X-rays with accuracy matching radiologists

## Interview Answer

> "Supervised learning is one of the main paradigms in machine learning. The core idea is that we train a model using labeled data — data where we know the correct answer for each example. The model learns a mapping function from inputs to outputs by minimizing a loss function that measures the difference between its predictions and the true labels.
>
> The typical workflow involves: collecting labeled data, splitting it into train/validation/test sets, choosing an appropriate model for the task — classification or regression —, training by iteratively updating parameters via gradient descent, validating to tune hyperparameters and prevent overfitting, and finally testing on unseen data.
>
> The key advantage is that supervised learning works very well when you have abundant labeled data. The main limitation is the cost and effort of creating labeled datasets — data labeling can be expensive and time-consuming. This is why techniques like transfer learning and semi-supervised learning have become popular."

## Related Concepts
- [[Unsupervised Learning]]
- [[Classification]]
- [[Regression]]
- [[Gradient Descent]]
- [[Overfitting]]
- [[Labeled Data]]
- [[Loss Function]]
- [[Feature Engineering]]
