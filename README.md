# PS-12: Fresh vs Rotten Fruit Classification

CNN-based six-class fruit freshness classification using transfer learning with MobileNetV2 and TensorFlow/Keras.

## Problem
Classify fruit images into six categories: `freshapples`, `freshbanana`, `freshoranges`, `rottenapples`, `rottenbanana`, and `rottenoranges`.

## Dataset
- **Source:** [Fruits Fresh and Rotten for Classification — Kaggle](https://www.kaggle.com/datasets/sriramr/fruits-fresh-and-rotten-for-classification)
- The notebook downloads the dataset through the Kaggle CLI. To run it, upload your own Kaggle API credentials in Colab when prompted. **Never commit `kaggle.json` or any API key.**
- The notebook uses the provided `train` and `test` folders and creates a validation split from the training data. Check the notebook outputs for the exact split counts.

## Methodology
- TensorFlow/Keras and ImageNet-pretrained MobileNetV2
- Image resizing and MobileNetV2 preprocessing
- Frozen-backbone transfer learning followed by fine-tuning
- Six-class softmax output and sparse categorical cross-entropy
- Test-set evaluation with accuracy, per-class precision/recall/F1, macro F1 and a confusion matrix
- Additional analysis of misclassified test images and potential shortcut-learning risks

## Reported results
The existing notebook recorded **99.37% fine-tuned test accuracy on 2,698 test images**, compared with **99.00%** before fine-tuning. Re-run the notebook to reproduce outputs in your own Colab runtime and verify all final figures before submission.

## Run in Google Colab
1. Open the notebook in Colab.
2. Upload your Kaggle API token when prompted; do not save it in this repository.
3. Run the notebook cells in order.
4. Check that class-count tables, training curves, final test metrics, confusion matrix and at least four final-model misclassified examples render successfully.

## Responsible use and limitations
The reported score is based on this dataset's test split and does not establish performance on real-world images captured under different lighting, backgrounds, cameras or storage conditions. Visual models can learn dataset-specific shortcuts. Human inspection is recommended before making consequential food-safety decisions; appearance alone cannot guarantee food is safe to eat.

## AI assistance
AI assistance was used to help organize and review the notebook and submission documentation. The student should verify the code, outputs and explanations, and disclose AI assistance according to the course's academic-integrity rules.

## Citation
Dataset: *Fruits Fresh and Rotten for Classification*. Kaggle, `sriramr/fruits-fresh-and-rotten-for-classification`. https://www.kaggle.com/datasets/sriramr/fruits-fresh-and-rotten-for-classification
