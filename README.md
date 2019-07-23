### 汇报人：李泽政

### 汇报日期：2019.07.23

------

#### 1. 复现医疗领域命名实体识别的代码 [done]

目的：为了确定Bi-Lstm + CRF在医疗领域命名实体识别中的可行性与有效性

方法：选择GitHub上的代码 https://github.com/liuhuanyong/MedicalNamedEntityRecognition

原理图如下

 ![] (https://image.baidu.com/search/detail?ct=503316480&z=0&ipn=d&word=Bi-LSTM%20%2B%20CRF&step_word=&hs=0&pn=25&spn=0&di=28270&pi=0&rn=1&tn=baiduimagedetail&is=0%2C0&istype=0&ie=utf-8&oe=utf-8&in=&cl=2&lm=-1&st=undefined&cs=1605203935%2C2482397711&os=2668076504%2C3043543768&simid=4185926742%2C699985741&adpicid=0&lpn=0&ln=267&fr=&fmq=1563847736690_R&fm=&ic=undefined&s=undefined&hd=undefined&latest=undefined&copyright=undefined&se=&sme=&tab=0&width=undefined&height=undefined&face=undefined&ist=&jit=&cg=&bdtype=0&oriquery=&objurl=http%3A%2F%2Fs4.51cto.com%2Fwyfs02%2FM01%2F96%2FC1%2FwKiom1klLeviklU9AADp1rf6zz8162.jpg&fromurl=ippr_z2C%24qAzdH3FAzdH3Fooo_z%26e3Btpusy_z%26e3Brv-usy_z%26e3Bv54AzdH3Fw6ptvsjAzdH3Fr-v6u%2B%25El%25bD%25ld%25En%25bd%25bc%25Ec%25lF%25bm%25Ec%25Am%25AF%25Ed%25ba%25Bn%25E0%25ba%25B0_z%26e3Bip4s&gsm=0&rpstart=0&rpnum=0&islist=&querylist=&force=undefined)

结果：

| P | R | F1 |

|0.3301 | 0.3446 | 0.3372 |

#### 2.模型在春雨医生数据集上测试 [done]

迁移结果：

| P | R | F1 |

|0.1688 | 0.1383 | 0.1520 |

发现问题：

('维', 'CHECK-B'), ('生', 'CHECK-B'), ('素', 'TREATMENT-I')

讨论问题：

会不会是因为数据量过小导致CRF无法发挥效用

实验与分析：

在同等规模数据集上用LSTM+CRF模型在其他领域命名实体识别数据集上测试，发现效果很好，说明不是由于数据量过小而导致的问题

领域调研：

CCKS2017 TASK2 评测

#### 2.改进医疗领域命名实体识别模型 [continue, 50%]





