# Adversarial Attacks on Aerial Object Detection (YOLO + DOTA)

This repository provides implementations of several adversarial attack methods targeting aerial object detection models trained on the DOTA dataset.  
The dataset is sourced from the **Aerial-YOLO-DOTA** project:

- Repository: https://github.com/davidgeorgewilliams/Aerial-YOLO-DOTA  
- Dataset (Google Drive): https://drive.google.com/file/d/13fAWtcBEvLfUkQgUkHvcqWxI1HZNOin6/view?usp=sharing

Due to the dataset’s large size, training from scratch on limited compute (e.g., Colab Free) was not feasible. Instead, this project uses pretrained YOLO model weights trained for 250 epochs, shared by the community:

- Pretrained Model Weights (Issue Comment):  
  https://github.com/davidgeorgewilliams/Aerial-YOLO-DOTA/issues/2#issuecomment-2925552459

## Repository Structure

The repository contains three Jupyter notebooks implementing different adversarial attacks:

### `DE_pixel_attack.ipynb`
Implements one-pixel and three-pixel black-box adversarial attacks, which modify a very small number of pixels to disrupt object detection.

### `Patch_Attack_Black_Box.ipynb`
Implements a basic black-box patch attack that generates and applies an adversarial patch to reduce model accuracy.

### `RobustDPatch_Attack.ipynb`
Implements the RobustDPatch attack using the **Adversarial Robustness Toolbox (ART)**, producing robust, transformation-resistant adversarial patches.

## Requirements for Running the Attacks

To run any of the attack notebooks:

1. **Download the DOTA dataset** from the link provided above.  
2. **Download the pretrained YOLO model weights** from the GitHub issue link.  
3. **Update all dataset paths and model paths inside the notebooks** to point to the locations where you store these files on your machine.

All notebooks currently contain **absolute file paths** from the original development environment, so these must be modified before execution.
