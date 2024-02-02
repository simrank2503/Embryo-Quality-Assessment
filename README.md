# Embryo-Quality-Assessment

## Abstract :
In the realm of assisted reproductive technology, In Vitro Fertilization (IVF) has brought hope to countless aspiring parents. A critical factor influencing IVF success is the quality of embryos. Traditional assessment methods rely on subjective human judgment, but the future of IVF is witnessing a transformative shift. Leveraging cutting-edge image analysis technology, we are paving the way for a more precise and objective evaluation of embryo quality.A good quality embryo increases chances of pregnancy rate and decreases number of embryo transfers hence, decreasing the cost of the IVF treatment. Below shows the process of IVF for context.


## Introduction:
Embryos are selected for transfer on the basis of developmental rate and morphological features.A good quality embryo increases chances of pregnancy rate and decreases number of embryo transfers hence, decreasing the cost of the IVF treatment.


## The Significance of Embryo Quality:
Embryo quality is a pivotal determinant in the success of IVF treatments. High-quality embryos possess the greatest potential for successful implantation and development. Traditionally, embryologists have relied on manual grading, introducing subjectivity and potential variability. Our project seeks to redefine this process, offering a more accurate, efficient, and consistent approach.


## Project Objective:
The primary objective of our project is to develop an advanced image analytics solution that utilizes machine learning and computer vision techniques to analyze and classify embryos.We want to provide a more accurate, consistent, and objective method for distinguishing between embryos with higher and lower potential for successful development, thereby enhancing the overall effectiveness and success rates of IVF treatments. The graphic below shows the stages of embryo development; we will be focusing primarily on images from the 2 cell / 4 cell stages.


## Technology at the Forefront:
Embarking on a journey to redefine the assessment of embryo quality, our project leverages advanced technologies and data-driven methodologies. With a dataset comprising 840 training images from a Kaggle competition, each depicting embryos at 256x256 pixel size on both day 3 and day 5 of development, our multi-faceted approach combines Exploratory Data Analysis (EDA), Convolutional Neural Networks (CNNs), and Structural Similarity Index (SSIM) to revolutionize IVF success. The process is shown below.


## Project Methodology:

### Data Description :
Our dataset featured 840 embryo images in JPG format, predominantly sized at 256x256 pixels. These images represented embryos at two developmental stages: Day 3 (D3) and Day 5 (D5). A significant observation from our analysis was the higher number of D3 images compared to D5, nearly double in both our training and testing sets.


### Data Preprocessing Exploration:
Normalized and resized images to create a standardized input for the model, CNN and SSIM.


We began with an in-depth Exploratory Data Analysis (EDA). This phase is vital for uncovering insights into our dataset and guiding our approach in subsequent stages of the study.


When examining the quality classification of these embryos, we encountered a notable imbalance. A vast majority, 82% of the images, were classified as “Bad” (Class 0), while a mere 18% were classified as “Good” (Class 1). This translated to 716 bad and 124 good embryos. The imbalance was especially stark in the D3 images, with a distribution of 22 good to 560 bad embryos, while the D5 category, though still imbalanced, had a less skewed ratio with 102 good embryos against 280 bad ones.


Bad (0) vs. Good (1) for overall dataset


Bad (0) vs. Good (1) for D3


Bad (0) vs. Good (1) for D5

This finding is crucial for several reasons. Firstly, it highlights a challenge in machine learning: when a dataset is imbalanced like ours, it can make it harder for our models to learn how to correctly identify the less common class — in our case, the ‘Good’ embryos. It’s akin to trying to learn a language when you mostly hear just one dialect; you might not get proficient at understanding the others. Secondly, this imbalance might reflect the real-world situation in IVF clinics, where more embryos are classified as ‘Bad’ than ‘Good’, giving us a glimpse into the reality of IVF success rates. Thirdly, it suggests that the stage of embryo development (D3 vs. D5) might influence how embryos are classified, hinting at deeper biological factors at play. Lastly, it points to the need for a cautious approach when using this data in clinical settings like IVF clinics, ensuring accurate selection of the best embryos.

With these insights from our EDA, we have uncovered key aspects of our dataset, including the distribution of embryo stages, the imbalance in quality classification, and variations in image sizes. These findings are instrumental in understanding the challenges and potential biases in our dataset, informing our next steps in the analysis.

## Data Modelling

### CNN Architecture:

Designed and trained CNNs to learn and extract features associated with embryo quality.CNNs, the backbone of our analysis, were employed to extract intricate features from embryo images. The architecture was designed to discern patterns crucial for differentiating between embryos at various developmental stages. Through iterative training on the Kaggle dataset, the CNNs learned to correlate visual features with embryo quality, providing a robust predictive model.

### SSIM Integration:
Incorporated SSIM to quantify the structural similarity between predicted and actual embryo images. To enhance the precision of our embryo quality assessment, we incorporated the Structural Similarity Index (SSIM). SSIM measures the similarity between two images, providing a quantitative metric for evaluating the quality of our model’s predictions against ground truth labels. This additional layer of analysis ensures a more nuanced evaluation, accounting for structural variations beyond what the human eye perceives.

### Algorithm Development:
Employing computer vision techniques and machine learning algorithms to identify relevant features associated with embryo quality.


### Model Training:
Training and fine-tuning our machine learning models using the annotated dataset to ensure accuracy and generalizability.

### Validation and Testing:
Rigorous validation and testing of the developed system using independent datasets to assess its performance and reliability.

## Benefits of Image Analysis in IVF:
Objective Grading: Eliminating subjectivity in embryo grading ensures consistent and reliable assessments, reducing the likelihood of human error.
Time Efficiency: Automated image analysis significantly accelerates the grading process, allowing embryologists to allocate more time to critical decision-making.
Enhanced Predictability: By analyzing a multitude of features beyond human perception, our system aims to provide a more comprehensive and predictive evaluation of embryo viability.
Results and Implications:

Our integrated approach, combining CNNs and SSIM, demonstrates promising results in assessing embryo quality. The combination of deep learning and structural similarity metrics provides a more nuanced and accurate prediction compared to traditional methods. This has significant implications for the field of assisted reproductive technologies, potentially elevating success rates in IVF treatments.


## Future Directions:
The success of our project lays the foundation for future research and innovation in the field. Ongoing efforts include expanding the dataset, refining the CNN architecture, and exploring additional image analysis techniques to further improve predictive accuracy.


## Conclusion:
In the quest to redefine embryo quality assessment, our project represents a convergence of cutting-edge technologies and comprehensive data analysis. By seamlessly integrating EDA, CNNs, and SSIM, we aim to offer a transformative solution that not only enhances IVF success rates but also opens doors to new possibilities in assisted reproduction. The journey continues, fueled by the collective commitment to reshaping the landscape of reproductive medicine.

Code link : https://colab.research.google.com/drive/1IDd8YBLMRZdypg1NnIy_RslvjLgMAWOU?usp=sharing

Presentation Link : https://docs.google.com/presentation/d/17-IPYaxYWiT5rHYpviSfdU5_MlhzQZfYDwlzPHZujag/edit#slide=id.g29f27c995e2_6_14 

## References:
- https://www.institutobernabeu.com/en/blog/criteria-for-embryo-classification/
- https://www.geeksforgeeks.org/embryo-development-development-process-of-fetus/
- https://www.selectivf.com/ivf-process-georgia/
- https://tandon-a.github.io/CycleGAN_ssim/
- https://github.com/Po-Hsun-Su/pytorch-ssim
