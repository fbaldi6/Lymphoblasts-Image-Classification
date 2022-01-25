# Classification of B-Cell Lymphoblasts versus Normal Cells in White Blood Cells Microscopic Images
The goal of this project, inspired by the ISBI 2019 C-NMC Challenge, was to develop a deep learning architecture that can solve the classification problem in cancer cell imaging. The full documentation can be found [here](Report.pdf).

## Introduction
Acute Lymphoblastic Leukemia (ALL) is a fast-growing cancer of the blood and bone marrow, characterized by the development of many immature lymphocytes called lymphoblasts. It is the most common type of leukemia in children, particularly those between the ages of two and five, and the most common cause of death from pediatric cancers. Treatment depends on the type of ALL, age at diagnosis, and other factors. 

In any case, early detection and diagnosis are key to a good change for a cure. In order to reach a decisive conclusion for the diagnosis of the disease and the degree of progression, it is of paramount importance to identify malignant cells with high accuracy. The task of distinguishing lymphoblasts from normal white blood cells under the microscope is however generally challenging, as morphologically the images of the two cell types appear similar. Computer-aided tools can be extremely useful in automating the process of identifying malignant cells and in helping pathologist and oncologist make quicker and data-driven inferences.

In recent years, the advent of convolutional neural networks has enabled to achieve excellent results in many image classification problems, including those in the field of medical imaging. With regard to the classification of leukemic B-lymphoblast cells, however, the task is challenging even when leveraging such technologies. Indeed, the visual similarity between abnormal and normal cells on the one hand, and the great diversity between cells from different subjects on the other hand, makes it particularly difficult to distinguish the two. For this reason, the ISBI Challenge 2019 was presented and, even after its completion, many researchers continue to study the problem.

## Results
In this work we tested both from scratch and pre-trained networks for the classification of malignant lymphoblasts cells. Then we proposed an ensemble solution able to combine the classification power of the best networks, optimizing the weights with a genetic algorithm. The results obtained are encouraging and show that it is possible to correctly classify almost all malignant cells, with a precision of 95.90% and a recall of 97.56%. Overall, our ensemble achieves an F1 weighted score of the 95.52%. 

Since we did not have high computational capabilities we could use only a part of the dataset, and this could lead to an unsatisfactory accuracy in the analysis of malignant cells of rare shape that are not present in our dataset. So, despite the
promising results, cell classification problem is far from solved.

There is still room for improvement, such as the use of hyperparameter optimization to further optimize our networks, which again for computational reasons was not possible. Finally, it would also be interesting to work directly on the raw images, while in the competition dataset they were already preprocessed.
