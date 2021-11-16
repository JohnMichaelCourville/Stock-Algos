# Stock-Algos
Producing buy or sell signals using machine and/or deep learning.


Open the Predictor-A1 file to begin. 

Change 'data = pd.read_csv("BABA.csv")' by updating BABA.csv to any daily stock data you pull from yahoo finance. 

Modify stop and take to change your stop loss and take profice percent change. 

labels = []
for i in range(len(data)-1):
    price = data.Open[i]
    stop = price*.95
    take = price*1.10
    a = i + 1
    while stop < data.Close[a] < take and a+1 < len(data):
        a += 1
