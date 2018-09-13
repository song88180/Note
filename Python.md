pickle

    import pickle
    
    with open("dir/target.pkl", 'wb') as file_handle:
        pickle.dump(target, file_handle)
    
    with open("dir/target.pkl", 'rb') as file_handle:
        target = pickle.load(file_handle)
