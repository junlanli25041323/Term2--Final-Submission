# Taxonomy v2: Automatic Caption Recognition Error

## Overview
This revised taxonomy is designed for annotating errors across the full Week 1 dataset on automatic caption recognition and translation. It expands the classroom taxonomy into a more consistent system that can be applied across different types of spoken content, including conversational speech, lectures, interviews, and media clips.

## High-level Categories

### 1. Lexical Recognition Error
Errors where the spoken word is transcribed as the wrong word.

**Definition:**  
The system produces a word or phrase that does not match the original speech at the word level.

**Subcategories:**
- Homophone confusion
- Similar-sounding word substitution
- Partial word recognition
- Proper noun misrecognition

### 2. Omission
Errors where words, phrases, or full utterances are missing.

**Definition:**  
The system fails to capture part of the spoken content.

**Subcategories:**
- Missing word
- Missing phrase
- Missing sentence
- Dropped speaker turn

### 3. Addition
Errors where the system adds words that were not spoken.

**Definition:**  
The output includes content that is not present in the original audio.

**Subcategories:**
- Inserted filler
- Inserted lexical item
- Hallucinated phrase

### 4. Semantic Distortion
Errors where the literal transcription may appear plausible, but the meaning of the original utterance is changed.

**Definition:**  
The output alters, weakens, or reverses the intended meaning.

**Subcategories:**
- Meaning shift
- Contradictory meaning
- Loss of nuance
- Ambiguous reformulation

### 5. Speaker and Attribution Error
Errors related to who is speaking or how speech is assigned.

**Definition:**  
The system incorrectly identifies, merges, or separates speakers.

**Subcategories:**
- Wrong speaker assignment
- Merged speakers
- Unmarked speaker change

### 6. Temporal and Segmentation Error
Errors related to timing, chunking, and subtitle boundaries.

**Definition:**  
The subtitle unit does not align correctly with speech timing or sentence structure.

**Subcategories:**
- Delayed subtitle
- Premature subtitle
- Incorrect line break
- Split utterance
- Merged utterance

### 7. Translation and Cultural Context Error
Errors where translated captions fail to preserve context, idiom, or culturally specific meaning.

**Definition:**  
The system produces a translation that is linguistically or culturally inadequate.

**Subcategories:**
- Idiom mistranslation
- Literal translation
- Register mismatch
- Cultural reference loss

## Revisions from the Classroom Taxonomy

The classroom taxonomy focused mainly on visible surface errors such as wrong words and missing words. For the full dataset, the taxonomy has been revised in four ways:

1. It now separates **surface recognition errors** from **meaning-level distortion**.
2. It includes **speaker attribution** and **temporal segmentation**, which became more important across longer recordings.
3. It adds **translation and cultural context** to account for multilingual and subtitling conditions.
4. It is designed to be scalable, allowing each annotation to be assigned a high-level category and, when needed, a subcategory.

## Application to the Full Dataset

To make the taxonomy usable across the whole Week 1 dataset, each record should be annotated using:

- one primary category
- one optional subcategory
- a short evidence note
- a severity level if needed

This structure makes the taxonomy flexible enough for different media forms while keeping the categories consistent across the dataset.

## Annotation Rule
When multiple errors appear in one segment, the annotation should prioritise the error with the strongest impact on meaning. Secondary issues can be noted in the comment field if the annotation platform allows it.