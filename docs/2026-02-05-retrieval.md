---
hide:
  - navigation
---

# Similar instances enhances rejection. ![](./../images/rain_book.jpg){ align=right style="width:7.5em; margin-left: 7.5em; margin-top: 0.5em; border-radius: 1em;"}

<br>

<p style="color: blue;">Special thanks to Yi Li, Jiacheng Cheng and Nuno Vasconcelos for a lot of super valuable feedback and discussion on this post.</p>

## Motivation. 

Selective prediction is a classic problem in machine learning in which a model is allowed to decide when to make a prediction and when to abstain. The objective is to achieve high accuracy on the predictions it does make, while avoiding uncertain or potentially risky inputs.

Traditionally, one common (and widely used) approach relies on thresholding the model’s output confidence, often derived from logits or predicted probabilities. For instance, consider a classifier that must distinguish between a dog and a cat image. Now suppose the model produces a probability distribution over the two classes of say, 0.1 for dog and 0.9 for cat. This maximum probability (0.9) reflects the model’s confidence in its prediction. In selective prediction, we compare this confidence score to a predefined threshold (e.g., 0.6) and output the predicted class (cat here) when the confidence exceeds the threshold. Otherwise, the model simply abstains from making a prediction, signaling uncertainty.

While such a paradigm works well for option-based tasks with a fixed set of answers, it breaks down in the context of generative tasks (e.g. dense caption an image), where outputs are open-ended and confidence estimates are far less reliable. Why? Well, this is because we have a confidence score for each output token. 

How can one solve this problem? Has anyone solved this before? Will discuss some works and one solution in my subsequent posts.



## Existing works.







