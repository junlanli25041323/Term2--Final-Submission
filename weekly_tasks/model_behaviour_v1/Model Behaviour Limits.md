# Model Behaviour Limits

## Expected behaviour

The model performed as expected when the input closely matched the training examples.
For example, when the hand was clearly raised or lowered and the face was fully visible, the model produced stable predictions with relatively high confidence scores. This suggests the model learned strong visual patterns from the dataset.

## Unstable predictions

However, the model became unstable when the input was ambiguous or slightly different from the training images. Small movements or partial hand positions sometimes caused the prediction to flip between labels such as **Hand Raised**, **Hand Position**, and **Hand Lowered**. This instability suggests the model struggles with transitional poses.

## Misleading confidence scores

In several cases the model produced high confidence scores even when the prediction was incorrect. For example, a lowered hand could still be classified as **Hand Raised** with a confidence above 0.9. This indicates that the confidence score reflects pattern similarity rather than true correctness.

## Relationship to dataset structure

Some of the misclassifications may be related to the structure of the dataset. The categories **Hand Position**, **Hand Raised**, and **Hand Lowered** overlap conceptually, making it difficult for the model to separate them clearly. The model therefore relies on small visual cues that may not always be reliable.

## Limits of the label design

The label system forces complex human gestures into simplified categories. For humans, it is obvious when a hand is transitioning between positions, but the model must always choose a single label. As a result, nuanced differences between gestures collapse into simplified classifications.

## Missing distinctions

The model cannot interpret intention, context, or meaning behind the gesture. It only recognises patterns in the training data. For example, partial visibility of the face or hand may cause confusion because the model has no understanding of body structure.

## Reflection on dataset decisions

The decisions made during dataset creation and labeling strongly influenced the behaviour of the model. The examples chosen as training data effectively act as behavioural rules. If certain poses were underrepresented or ambiguous, the model reproduces those limitations during prediction.
