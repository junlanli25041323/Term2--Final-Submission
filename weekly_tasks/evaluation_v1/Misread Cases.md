# Misread Cases

This document records several cases where the sentiment model produced incorrect or unstable predictions when analysing inspirational quotations. The examples highlight how metaphor, rhetorical tone, and keyword bias can lead to misleading outputs.

---

## Case 1 — Inspirational quote misclassified as negative

**Input text:**  
"A woman is like a tea bag; you never know how strong it is until it's in hot water."

**Model output:**  
Label: NEGATIVE  
Confidence: 0.902669

**Reference label:**  
POSITIVE

**Why this feels incorrect or misleading**

The quote is motivational and metaphorical, encouraging resilience and inner strength. However, the model appears to interpret the phrase “hot water” as negative sentiment. This suggests the system struggles with metaphorical language and tends to interpret phrases literally.

**Issue type**

False negative / metaphor misinterpretation

---

## Case 2 — Perseverance statement misread

**Input text:**  
"I have not failed. I've just found 10,000 ways that won't work."

**Model output:**  
Label: NEGATIVE  
Confidence: 0.997591

**Reference label:**  
POSITIVE

**Why this feels incorrect or misleading**

This quote expresses persistence and optimism despite failure. The model likely reacts strongly to the words “failed” and “won't work”, interpreting them as negative indicators even though the message is motivational.

The very high confidence score (0.99) suggests that the model is overconfident in its prediction.

**Issue type**

False negative / keyword bias

---

## Case 3 — Literary humour misinterpreted

**Input text:**  
"The person, be it gentleman or lady, who has not pleasure in a good novel, must be intolerably stupid."

**Model output:**  
Label: NEGATIVE  
Confidence: 0.999681

**Reference label:**  
POSITIVE

**Why this feels incorrect or misleading**

Although the quote contains the word “stupid”, it is intended as humorous literary commentary rather than hostile sentiment. The model focuses on the negative keyword rather than recognising the rhetorical tone typical of classic literature.

**Issue type**

Context collapse / rhetorical tone misread

---

## Case 4 — Figurative humour interpreted literally

**Input text:**  
"A day without sunshine is like, you know, night."

**Model output:**  
Label: NEGATIVE  
Confidence: 0.990705

**Reference label:**  
NEGATIVE

**Why this may still be unstable**

Although the prediction matches the reference label, the sentence is humorous rather than expressing strong negative emotion. The model likely interprets the absence of “sunshine” and the word “night” as negative sentiment.

**Issue type**

Literal interpretation of figurative humour

---

## Case 5 — Toxicity score inconsistency

**Input text:**  
"The person, be it gentleman or lady, who has not pleasure in a good novel, must be intolerably stupid."

**Toxicity score:**  
0.868079

**Why this feels misleading**

The high toxicity score is triggered by the word “stupid”. However, in this context the statement is part of a humorous literary quote rather than a direct insult. This demonstrates how keyword-based toxicity detection can produce misleading results when context is ignored.

**Issue type**

False toxicity signal / keyword sensitivity