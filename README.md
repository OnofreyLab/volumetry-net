# Automated MRI liver segmentation for anatomical segmentation, liver volumetry, and the extraction of radiomics

Moritz Gross<sup>1, 2</sup>, M.S.; Steffen Huber<sup>1</sup>, M.D.; Sandeep Arora<sup>1</sup>, M.D.; Tal Ze'evi<sup>3</sup>, M.Sc.; Stefan P. Haider<sup>1, 4</sup>, M.D.; Ahmet S. Kucukkaya<sup>1, 2</sup>, M.S.; Simon Iseke<sup>1, 5</sup>, M.S.; Tom Niklas Kuhn<sup>1, 6</sup>, M.S.; Bernhard Gebauer<sup>2</sup>, M.D.; Florian Michallek<sup>2</sup>, M.D.; Marc Dewey<sup>2</sup>, M.D.; Valérie Vilgrain<sup>7, 8</sup>, M.D.; Riccardo Sartoris<sup>7, 8</sup>, M.D.; Maxime Ronot<sup>7, 8</sup>, M.D.; Ariel Jaffe<sup>9</sup>, M.D.; Mario Strazzabosco<sup>9</sup>, M.D., Ph.D.; Julius Chapiro<sup>1, 3</sup>, M.D.; Ph.D.; John A. Onofrey<sup>1, 3, 10</sup>, Ph.D.


[Cite this article](#cite-this-article)

## Abstract

**Objectives:** To develop and evaluate a deep convolutional neural network (DCNN) for automated liver segmentation, volumetry, and radiomic feature extraction on contrast-enhanced portal-venous phase magnetic resonance imaging (MRI).

**Materials and Methods:** This retrospective study included hepatocellular carcinoma patients from an institutional database with portal-venous MRI. After manual segmentation, the data was randomly split into independent training, validation, and internal testing sets. From a collaborating institution, de-identified scans were used for external testing. The public LiverHccSeg dataset was used for further external validation. A 3D DCNN was trained to automatically segment the liver. Segmentation accuracy was quantified by Dice Similarity Coefficient (DSC) with respect to manual segmentation. A Mann-Whitney U test was used to compare the internal and external test sets. Agreement of volumetry and radiomic features was assessed using the intraclass correlation coefficient (ICC). 

**Results:** 470 patients met the inclusion criteria (63.9±8.2 years; 376 males) and 20 patients were used for external validation (41±12 years; 13 males). DSC segmentation accuracy of the DCNN was similarly high between the internal- (0.97±0.01) and external test set (0.96±0.03) (p=.28), and demonstrated robust segmentation performance on public testing (0.93±0.03). Agreement of liver volumetry was satisfactory in the internal- (ICC, 0.99), external- (ICC, 0.97), and public test set (ICC, 0.85). Radiomic features demonstrated excellent agreement in the internal- (mean ICC, 0.98±0.04), external- (mean ICC, 0.94±0.10), and public dataset (mean ICC, 0.91±0.09).

**Conclusion:** Automated liver segmentation yields robust and generalizable segmentation performance on MRI data and can be used for volumetry and radiomic feature extraction.

**Clinical relevance statement:** Liver volumetry, anatomic localization, and extraction of quantitative imaging biomarkers require accurate segmentation, but manual segmentation is time-consuming. A deep convolutional neural network demonstrates fast and accurate segmentation performance on T1-weighted portal-venous MRI.



## Using Volumetry-Net

### Prerequisites

Clone this repository to your local machine.
Install the necessary dependencies by creating a conda environment from the `environment.yml` file located in the root directory of this repository.

### Using the Liver Segmentation Model on Portal-Venous Phase MRI

To perform model inference on your data, follow these steps:
1. Activate the conda environment from the `environment.yml` file
2. Open the `Automated Segmentation Inference.ipynb` notebook from the notebooks directory. The notebook contains detailed instructions for running the model inference.
3. Update the `MODEL_ROOT_PATH` variable within the notebook to point to the directory where you have saved the trained model on your local machine.
4. Update the the `OUTPUT_PATH` variable within the notebook to point to the directory where you want to save out the generated liver segmentations.

Notice: If want to change the naming convention of the output segmentation masks you can modify the `output_file_name` parameter in the `inference` function.






## Author information

**Affiliations**

<sup>1</sup>	Department of Radiology and Biomedical Imaging, Yale University School of Medicine, New Haven, Connecticut, United States of America

<sup>2</sup>	Charité Center for Diagnostic and Interventional Radiology, Charité - Universitätsmedizin Berlin, Berlin, Germany

<sup>3</sup>	Department of Biomedical Engineering, Yale University, New Haven, Connecticut, United States of America

<sup>4</sup>	Department of Otorhinolaryngology, University Hospital of Ludwig Maximilians Universität München, Munich, Germany

<sup>5</sup>	Department of Diagnostic and Interventional Radiology, Pediatric Radiology and Neuroradiology, Rostock University Medical Center, Rostock, Germany

<sup>6</sup>	Department of Diagnostic and Interventional Radiology, University Duesseldorf, Duesseldorf, Germany

<sup>7</sup>	Université Paris Cité, Paris, Île-de-France, France

<sup>8</sup>	Department of Radiology, Hôpital Beaujon, AP-HP.Nord, Department of Radiology, Clichy, Île-de-France, France

<sup>9</sup>	Department of Internal Medicine, Yale University School of Medicine, New Haven, Connecticut, United States of America

<sup>10</sup>	Department of Urology, Yale University School of Medicine, New Haven, Connecticut, United States of America




## Cite this article

Gross, M., Huber, S., Arora, S. et al. Automated MRI liver segmentation for anatomical segmentation, liver volumetry, and the extraction of radiomics. Eur Radiol (2024). https://doi.org/10.1007/s00330-023-10495-5
