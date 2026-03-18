# Taxonomy Limits

## How the taxonomy works
This taxonomy works by converting complex captioning and translation failures into a manageable set of categories. It helps make recurring error patterns visible across the dataset and supports comparison between different subtitle segments. By using high-level categories and optional subcategories, the system remains structured while allowing some descriptive flexibility.

## Where meaning is forced or collapses
Meaning is sometimes forced into a single category even when an error could belong to several at once. For example, a mistranslated subtitle may also involve omission, semantic distortion, and cultural loss. In these cases, the taxonomy simplifies the event in order to make annotation possible. This means the annotation may flatten the complexity of the original communicative situation.

Meaning also collapses when the system treats speech as a sequence of isolated units rather than as context-dependent language. Tone, irony, hesitation, overlap, and affect are often reduced or lost.

## What the system still cannot express
The taxonomy does not fully express:
- uncertainty or ambiguity in speech
- emotional tone or interpersonal dynamics
- multimodal cues such as gesture, facial expression, or visual context
- the social consequences of an error for accessibility and understanding
- degrees of interpretive disagreement between annotators

It also struggles to represent cases where the subtitle is technically accurate at word level but pragmatically misleading.

## Distinctions that disappear at scale
At a larger scale, subtle distinctions tend to disappear. Differences between lexical error, semantic distortion, and cultural mistranslation can become blurred when annotators work quickly or apply rules inconsistently. Small contextual nuances are harder to preserve across hundreds of records.

As the dataset grows, annotation tends to favour repeatable categories over precise interpretation. This improves consistency but reduces sensitivity to edge cases, hybrid errors, and context-specific meanings.