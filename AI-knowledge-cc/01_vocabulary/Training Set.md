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
