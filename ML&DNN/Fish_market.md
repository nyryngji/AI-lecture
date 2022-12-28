## Fish Market

> **1. 분포도 파악**

> 
    import csv
    import matplotlib.pyplot as plt

    f = open('Fish.csv','r')
    data = csv.reader(f)
    header = next(data)

    bream_w = []
    bream_l = []

    smelt_w = []
    smelt_l = []

    for row in data:
       if (row[0] == 'Bream'):
           bream_w.append(float(row[1]))
           bream_l.append(float(row[3]))
       if (row[0] == 'Smelt'):
           smelt_w.append(float(row[1]))
           smelt_l.append(float(row[3]))

    f.close()
    plt.rc('font',family='Malgun Gothic')
    plt.scatter(bream_l,bream_w,label='도미')
    plt.scatter(smelt_l,smelt_w,label='빙어')
    plt.scatter(30,600,label='의문의 피쉬',marker='*',s=[200],c='black')
    plt.xlabel('length[cm]')
    plt.ylabel('weight[g]')
    plt.legend()
    plt.grid(True)
    plt.show()
   
<br>

> **2.**
