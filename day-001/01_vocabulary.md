# Labeled Data

## Definition (English)
Labeled data is a dataset where each input example is paired with a correct output label. It's the foundation of supervised learning — the model learns by comparing its predictions against these known correct answers.

## Chinese
标注数据（有标签数据）

## German
Beschriftete Daten (gelabelte Daten)

## Intuition
Think of labeled data as a textbook with answer keys. When you practice math problems, you need to know the correct answers to learn from your mistakes. Similarly, an ML model needs labeled examples to learn the mapping from input to output.

## Example
For a spam detection model, each email in the training set must be labeled as "spam" or "not spam". The model studies thousands of such labeled emails, learns patterns in spam messages, and eventually can classify new unseen emails.

## Spoken Version
"In our project, we need high-quality labeled data to train the model — essentially, each training example must have a ground truth annotation that the model can learn from."

## German Workplace Example
"Für das Training des Modells benötigen wir qualitativ hochwertige beschriftete Daten. Jedes Beispiel im Trainingsdatensatz muss eine Ground-Truth-Annotation haben."

## Related Concepts
- [[Supervised Learning]]
- [[Training Set]]
- [[Ground Truth]]
- [[Data Annotation]]

## Tags
#supervised-learning #data #fundamentals #training

---

# Training Set

## Definition (English)
The training set is the portion of labeled data used to teach the model. The model iteratively adjusts its parameters to minimize the difference between its predictions and the true labels on this set.

## Chinese
训练集

## German
Trainingsdatensatz (der Training Set)

## Intuition
The training set is like your practice problems before an exam. You study them repeatedly, identify patterns, and improve. But just like you shouldn't memorize the practice problems (overfitting), the model should generalize beyond the training set.

## Example
If you have 10,000 labeled images of cats and dogs, you might use 8,000 as the training set. The model sees these 8,000 images many times (epochs), adjusting its internal weights each time to better distinguish cats from dogs.

## Spoken Version
"We split the dataset so that 80% becomes the training set — this is what the model actually learns from during the optimization process."

## German Workplace Example
"Wir teilen den Datensatz so auf, dass 80% als Trainingsdatensatz verwendet werden. Das Modell lernt daraus während des Optimierungsprozesses."

## Related Concepts
- [[Labeled Data]]
- [[Validation Set]]
- [[Test Set]]
- [[Overfitting]]

## Tags
#supervised-learning #data-splitting #training

---

# Feature

## Definition (English)
A feature is an individual measurable property or characteristic of the data that the model uses as input to make predictions. Features are the "columns" in your training data table.

## Chinese
特征

## German
Merkmal (das Feature)

## Intuition
Features are the clues the model uses to solve the puzzle. To predict house prices, features might be: square footage, number of bedrooms, location, and year built. The model learns which features matter most and how they combine to produce the output.

## Example
For a credit scoring model predicting loan default, features include: applicant's income, credit history length, debt-to-income ratio, employment status, and number of previous loans. Each feature contributes differently to the final prediction.

## Spoken Version
"Feature engineering is often more impactful than model selection — choosing and transforming the right features can dramatically improve performance."

## German Workplace Example
"Feature Engineering ist oft wichtiger als die Modellauswahl. Die richtigen Merkmale zu identifizieren und zu transformieren, kann die Modellleistung erheblich verbessern."

## Related Concepts
- [[Feature Engineering]]
- [[Feature Selection]]
- [[Dimensionality]]
- [[Input Space]]

## Tags
#supervised-learning #features #data-preprocessing

---

# Loss Function

## Definition (English)
A loss function (or cost function) measures how far the model's predictions are from the true labels. It quantifies the "error" — the model's goal during training is to minimize this loss.

## Chinese
损失函数

## German
Verlustfunktion (die Loss Function)

## Intuition
Imagine throwing darts at a target. The loss function measures the distance from each dart to the bullseye. A good model has darts clustered near the center (low loss). Training is the process of adjusting your throw (model parameters) to reduce the average distance.

## Example
In linear regression predicting house prices, Mean Squared Error (MSE) is a common loss function. If the model predicts €300,000 but the actual price is €320,000, the squared error is (320,000 - 300,000)² = 400 million. The model adjusts to make this number smaller over time.

## Spoken Version
"We're using cross-entropy loss for this classification task — it penalizes confident wrong predictions more heavily, which helps the model converge faster."

## German Workplace Example
"Für diese Klassifikationsaufgabe verwenden wir Cross-Entropy-Loss. Diese Verlustfunktion bestraft selbstbewusste Fehlvorhersagen stärker, was dem Modell hilft, schneller zu konvergieren."

## Related Concepts
- [[Gradient Descent]]
- [[Optimization]]
- [[Mean Squared Error]]
- [[Cross-Entropy]]

## Tags
#supervised-learning #loss-function #optimization #training

---

# Overfitting

## Definition (English)
Overfitting happens when a model learns the training data too well — including its noise and random fluctuations — but fails to generalize to new, unseen data. The model "memorizes" rather than "learns."

## Chinese
过拟合

## German
Überanpassung (Overfitting)

## Intuition
Overfitting is like a student who memorizes every practice problem's exact numbers instead of understanding the underlying concept. They get 100% on practice tests but fail the real exam because the questions are slightly different. A good model learns patterns, not specifics.

## Example
A decision tree that keeps splitting until every training data point is perfectly classified — with 100% training accuracy but only 65% test accuracy — is overfitting. It has created rules for noise instead of learning the true decision boundary.

## Spoken Version
"We noticed the training accuracy is 99% but validation is only 72% — clear sign of overfitting. We should add regularization and potentially reduce model complexity."

## German Workplace Example
"Die Trainingsgenauigkeit liegt bei 99%, aber die Validierungsgenauigkeit nur bei 72% — ein klares Anzeichen für Überanpassung. Wir sollten Regularisierung hinzufügen und die Modellkomplexität reduzieren."

## Related Concepts
- [[Underfitting]]
- [[Regularization]]
- [[Generalization]]
- [[Bias-Variance Tradeoff]]

## Tags
#supervised-learning #overfitting #generalization #validation
