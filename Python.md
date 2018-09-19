pickle

    import pickle
    
    with open("dir/target.pkl", 'wb') as file_handle:
        pickle.dump(target, file_handle)
    
    with open("dir/target.pkl", 'rb') as file_handle:
        target = pickle.load(file_handle)


matplotlib
    
    import matplotlib as mpl
    import mpl.pyplot as plt
    
    ## draw distribution
    plt.hist(data, bins = )
    plt.show()
    
    ## save
    fig = plt.figure(0)
    fig.clf()
    plt.plot(data, label = "o", color = 'r',ms=0.5)  # ms: marker size
    plt.xlabel("")
    plt.ylabel("")
    plt.title("")
    fig.savefig("dir/target.png")
    
    ## change x,y axis range.
    axes = plt.gca()
    axes.set_xlim([xmin,xmax])
    axes.set_ylim([None,ymax])
    
    x1,x2,y1,y2 = plt.axis()
    plt.axis((x1,x2,25,250))
    
numpy

    import numpy as np
    np.argmax(a, axis = )  # get the index of the maximum in an array
    
    import numpy.random as nrand 
    nrand.permutation(int,List,range)   # return a List.
    nrand.shuffle(List)   #change the List.

pandas
    
    import pandas as pd
    
