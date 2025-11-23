This project is under ongoing updates, with more resources being allocated over time to fine-tune T5 on the full CNN_DailyMail dataset—and even more datasets in the future!

<img src="https://mikky.video.blog/wp-content/uploads/2020/06/1_cd8wmb82csxacdtg8mlwhw.gif" style="width:100%;" />

Until now, this notebook finetunes T5 on **2% of the CNN/DailyMail dataset** due to Colab compute limits.
**The training code, architecture, data pipeline, and objective are identical** to a full-dataset finetuning run; only **the hyperparameters** (learning rate, batch size, epochs, etc.) would differ when scaling to the full dataset.

Finetuning on such a small subset **is not optimal for final model quality,** but **it allowed me to properly experiment with the training loop, scheduler, loss curve behavior, and hyperparameter ranges** that are required for real full-dataset training.

When training on 100% of the dataset:

- the same code can be used **without modification**

- only hyperparameters need adjusting

- larger datasets require lower LR and fewer epochs

The ([current notebooks](https://github.com/nabil-idrissi/T5-Base-Instruct-Finetuning/tree/main/notebooks)) focuses on **learning the finetuning pipeline only,** not producing a production-ready model yet.
