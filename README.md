### 汇报人：李泽政

### 汇报日期：2019.07.23

------

#### 1. 复现医疗领域命名实体识别的代码 [done]

目的：为了确定Bi-Lstm + CRF在医疗领域命名实体识别中的可行性与有效性

方法：选择GitHub上的代码 https://github.com/liuhuanyong/MedicalNamedEntityRecognition

框架：keras

结果：

| P | R | F1 |
   | :--- | :---: | :---: |
   |0.3301 | 0.3446 | 0.3372 |

#### 2.该模型在春雨医生数据集上测试 [done]

迁移结果：

| P | R | F1 |
   | :--- | :---: | :---: |
   |0.1688 | 0.1383 | 0.1520 |

发现问题：

('维', 'CHECK-B'), ('生', 'CHECK-B'), ('素', 'TREATMENT-I')

讨论问题：

因为数据量过小导致CRF无法发挥效用

实验与分析：

在同等规模数据集上用LSTM+CRF模型在其他领域命名实体识别数据集上测试，发现效果很好，说明不是由于数据量过小而导致的问题

领域调研：

CCKS2017 该任务 评测最好成绩

| P | R | F1 |
   | :--- | :---: | :---: |
   |0.9449 | 0.8789 | 0.9102 |

CCKS2018 该任务 评测最好成绩 F1 = 0.8913

#### 3.改进医疗领域命名实体识别模型 [continue, 50%]

方法：选择GitHub上的代码 https://github.com/fangwater/Medical-named-entity-recognition-for-ccks2017/tree/master/LSTM-CRF%20NER

框架：PyTorch

| P | R | F1 |
   | :--- | :---: | :---: |
   |0.8443 | 0.8573 | 0.8508 |
   
应用到春雨医生（自己标注）的数据集

| P | R | F1 |
   | :--- | :---: | :---: |
   |0.4148 | 0.1818 | 0.2523 |

原因分析

| P | R | F1 |
   | :--- | :---: | :---: |
   |0.8443 | 0.8573 | 0.8508 |
   | :--- | :---: | :---: |
   |0.8443 | 0.8573 | 0.8508 |

