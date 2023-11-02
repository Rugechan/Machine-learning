`python
import pandas as pd #读取、处理表格的包
import numpy as np #处理数组的包
import pickle	
`

# 打开要加载的.pkl文件
file_path = "R:\Machine learning\Data_file\hERG.pkl"  # 修改为正确的文件路径
with open(file_path, 'rb') as file: #r 读取；b 二进制
    hERG = pickle.load(file)
print(hERG)
y_train = hERG

# 打开要加载的.txt文件
file_path = "R:\Machine learning\Data_file\hERG_test.txt"  # 修改为正确的文件路径
with open(file_path, 'r') as file: #r 读取；b 二进制
    hERG_test = file.read()
print(hERG_test)
y_test = hERG_test

import numpy as np
from sklearn.preprocessing import LabelEncoder

# 假设y_test是一个包含类别标签的字符串，格式为 "[1 2 3]"
y_test = y_test.replace("[", "").replace("]", "").split()  # 清理字符串并拆分为单独的值
y_test = np.array(y_test, dtype=int)  # 转换为整数数组

labelencoder = LabelEncoder()
y_test_encoded = labelencoder.fit_transform(y_test)  # 对整数数组进行编码
print(y_test_encoded)

file_path = "R:\\Machine learning\\Data_file\\test_feature.pkl"  # 修改为正确的文件路径
with open(file_path, 'rb') as file:
    test_feature = pickle.load(file)
print(test_feature)
x_test = test_feature	


file_path = "R:\\Machine learning\\Data_file\\train_feature.pkl"  # 修改为正确的文件路径
with open(file_path, 'rb') as file:
    train_feature = pickle.load(file)
print(train_feature)
x_train = train_feature

result = combined_data.isnull().sum()
if result.any(): #any判断是否有非0值，True为有非0值
    print("There are missing values in the DataFrame.")
else:
    print("There are no missing values in the DataFrame.")
