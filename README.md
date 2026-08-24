import pandas as pd

columns = ["unit", "cycle", "op1", "op2", "op3"] + [    "sensor_" + str(i) for i in range(1, 22)
] 
train = pd.read_csv("train_FD001.txt", sep=r"\\s+",                   
header=None, names=columns)
test = pd.read_csv("test_FD001.txt", sep=r"\\s+",                   
header=None, names=columns)
rul_test = pd.read_csv("RUL_FD001.txt",                       
header=None, names=["RUL"]) 


print("NASA C-MAPSS FD001 data loaded successfully!")
print("Training shape:", train.shape) 
print("Test shape:", test.shape) print(train.head())
