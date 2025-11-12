I’m saving a copy of the instruction-augmented test dataset of the cnn_dailymail, as I will use it to test both Flan-T5 and my fine-tuned T5 model. A fair comparison requires using the same test set for both models.

For instruction-based fine-tuning, I’m augmenting the cnn_dailymail dataset to allow the T5 model to learn from instructions. The augmentation is done as follows:

The first column (article) of the original cnn_dailymail dataset is combined with a randomly chosen instruction from a predefined list.

Example:

Original article:

LONDON, England (Reuters) -- Harry Potter star Daniel Radcliffe gains access to a reported £20 million...

Augmented with instruction:

Summarize this text: LONDON, England (Reuters) -- Harry Potter star Daniel Radcliffe gains access to a reported £20 million...

This ensures the model sees instruction + text pairs during fine-tuning, allowing it to generalize to similar summarization prompts at inference time.
