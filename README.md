# RSNA-breast-cancer-detection

This work trains the model with screening mammograms obtained from regular screening.

This work improving the automation of detection in screening mammography may enable radiologists to be more accurate and efficient, improving the quality and safety of patient care. It could also help reduce costs and unnecessary medical procedures.

According to the WHO, breast cancer is the most commonly occurring cancer worldwide. In 2020 alone, there were 2.3 million new breast cancer diagnoses and 685,000 deaths. Yet breast cancer mortality in high-income countries has dropped by 40% since the 1980s when health authorities implemented regular mammography screening in age groups considered at risk. Early detection and treatment are critical to reducing cancer fatalities, and this machine learning models could help streamline the process radiologists use to evaluate screening mammograms.

Currently, early detection of breast cancer requires the expertise of highly-trained human observers, making screening mammography programs expensive to conduct. A looming shortage of radiologists in several countries will likely worsen this problem. Mammography screening also leads to a high incidence of false positive results. This can result in unnecessary anxiety, inconvenient follow-up care, extra imaging tests, and sometimes a need for tissue sampling (often a needle biopsy).

This work (a part of competition host), the Radiological Society of North America (RSNA) is a non-profit organization that represents 31 radiologic subspecialties from 145 countries around the world. RSNA promotes excellence in patient care and health care delivery through education, research, and technological innovation.

Your efforts in this competition could help extend the benefits of early detection to a broader population. Greater access could further reduce breast cancer mortality worldwide.

Files
[train/test]_images/[patient_id]/[image_id].dcm The mammograms, in dicom format. You can expect roughly 8,000 patients in the hidden test set. There are usually but not always 4 images per patient. Note that many of the images use the jpeg 2000 format which may you may need special libraries to load.

sample_submission.csv A valid sample submission. Only the first few rows are available for download.

[train/test].csv Metadata for each patient and image. Only the first few rows of the test set are available for download.

site_id - ID code for the source hospital.
patient_id - ID code for the patient.
image_id - ID code for the image.
laterality - Whether the image is of the left or right breast.
view - The orientation of the image. The default for a screening exam is to capture two views per breast.
age - The patient's age in years.
implant - Whether or not the patient had breast implants. Site 1 only provides breast implant information at the patient level, not at the breast level.
density - A rating for how dense the breast tissue is, with A being the least dense and D being the most dense. Extremely dense tissue can make diagnosis more difficult. Only provided for train.
machine_id - An ID code for the imaging device.
cancer - Whether or not the breast was positive for malignant cancer. The target value. Only provided for train.
biopsy - Whether or not a follow-up biopsy was performed on the breast. Only provided for train.
invasive - If the breast is positive for cancer, whether or not the cancer proved to be invasive. Only provided for train.
BIRADS - 0 if the breast required follow-up, 1 if the breast was rated as negative for cancer, and 2 if the breast was rated as normal. Only provided for train.
prediction_id - The ID for the matching submission row. Multiple images will share the same prediction ID. Test only.
difficult_negative_case - True if the case was unusually difficult. Only provided for train.
