pickle

    import pickle
    
    with open("dir/target.pkl", 'wb') as file_handle:
        pickle.dump(target, file_handle)
    
    with open("dir/target.pkl", 'rb') as file_handle:
        target = pickle.load(file_handle)


matplotlib
    
    import matplotlib as mpl
    import mpl.pyplot as plt
    
    plt.hist(data, bins = )
    plt.show()
    
    fig = plt.figure(0)
    fig.clf()
    plt.plot(data, label = "o", color = 'r',ms=0.5)  # ms: marker size
    plt.xlabel("")
    plt.ylabel("")
    plt.title("")
    fig.savefig("dir/target.png")

numpy

    numpy.argmax(a, axis = )  # get the index of the maximum in an array
