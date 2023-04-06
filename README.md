# MBP1413H_NuclearSeg
White Box attacks trained models for nuclear segmentation tasks

Abstract

Nuclei detection, indispensable for several pathological tests in the clinical setting, is often laborious, time-consuming, and inherently variable between and within trained clinicians. The aim of the 2018 Kaggle Data Science Bowl was to automate nuclei segmentation using a diverse dataset of microscopy images. The competition’s best model, a U-Net, is however at risk of collapse when faced with corrupted images via image perturbations, limiting the scope for clinical or research application. By using the white box adversarial attack, the Fast Sign Gradient Method (FGSM), we trained a simple and a complex model architecture, fully connected network (FCN) and U-Net, respectively using variably perturbed training images. We found U-Net models performed better compared to FCN models when no or little perturbation was added to test images. However, FCN models were more robust when faced with greater levels of noise. Our results indicate model designers should consider the trade-off between model accuracy and robustness when defining the optimal model for a given pathology related task.

Instructions for use:

1. Download training images and masks from the 2018 Kaggle Data Science Bowl (https://www.kaggle.com/competitions/data-science-bowl-2018)
2. Preprocess and augment images using 01.PreprocessingImages.ipynb
3. Designate training and testing data sets using 02.GeneratingTestImages.ipynb then 02.AddingAugTraining.ipynb
4. Train models, both U-Net and FCNs using variable perturbations using notebooks 03. and/or 04.
5. Test model performance and robustness using variable perturbations using 05.TestingModels_230327.ipynb
6. Visualize model architecture using 06.FinalViz.ipynb
