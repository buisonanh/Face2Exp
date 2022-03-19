# Face2Exp
## Abstract
Facial expression recognition (FER) is challenging due to the class imbalance caused by data collection. Existing studies tackle the data bias problem using only labeled facial expression dataset. Orthogonal to existing FER methods, we propose to utilize large unlabeled face recognition (FR) datasets to enhance FER. However, this raises another data bias problem---the distribution mismatch between FR and FER data. To combat the mismatch, we propose the Meta-Face2Exp framework, which consists of a base network and an adaptation network. The base network learns prior expression knowledge on class-balanced FER data while the adaptation network is trained to fit the pseudo labels of FR data generated by the base model. To combat the mismatch between FR and FER data, Meta-Face2Exp uses a circuit feedback mechanism, which improves the base network with the feedback from the adaptation network. Experiments show that our Meta-Face2Exp achieves comparable accuracy to state-of-the-art FER methods with 10% of the labeled FER data utilized by the baselines. We also demonstrate that the circuit feedback mechanism successfully eliminates data bias.
## Framework
![img](MetaFace2Exp_Framework.png)
## Command
The training command for affectnet is:
> python main.py --seed 5 --name aff --num-classes 7 --total-steps 180000 --eval-step 100 --randaug 2 16 --batch-size 8 --teacher_lr 1e-3 --student_lr 1e-3 --amp --resize 224 --world-size 2 --workers 16 

## Details
The selected labeled data is placed in the directory of data, as the format of csv.
Our model is stored in the [Google drive](https://drive.google.com/file/d/1y81cKJLDWs7Dzp9k8lm3zNG78C5qGyqd/view?usp=sharing). 
For test program, just run the test.ipynb file after modifying the model path to test the accuracy and predict a single image.

## Contact
If you have any questions, please contact authors: 

Dan Zeng: zengd@sustech.edu.cn

Zhiyuan Lin: 12132456@mail.sustech.edu.cn
