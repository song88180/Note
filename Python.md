```python
##  concatenate element in the list
myList = ','.join(myList) 
# if elements are not string type
myList = ','.join(map(str, myList))   # separate with comma
```

pickle

```python
import pickle

with open("dir/target.pkl", 'wb') as file_handle:
    pickle.dump(target, file_handle)
    
with open("dir/target.pkl", 'rb') as file_handle:
    target = pickle.load(file_handle)
```

pyplot

```python

import matplotlib as mpl
import mpl.pyplot as plt
    
## draw histgram distribution
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
# Or
left,right = plt.xlim()
bottom,top = plt.ylim()
plt.xlim(left, right)
plt.ylim(bottom, top)
    
## Stacked Bar Graph
#plt.bar(x, height, width=0.8, bottom=None)
ind = np.arange(N)
p1 = plt.bar(ind, means1, width, color='#d62728', yerr=Std1)
p2 = plt.bar(ind, means2, width, bottom=means1, yerr=Std2)

## Stacked histogram
plt.hist([x1, x2, x3, ...], bins = N, stack = True)
plt.legend(('x1lable','x2lable','x3lable', ...))

```          
    
numpy

```python
import numpy as np
np.argmax(a, axis = )  # get the index of the maximum in an array
    
import numpy.random as nrand 
nrand.permutation(int,List,range)   # return a List.
nrand.shuffle(List)   #change the List.
nrand.choice(5, 3, replace = False)  ## This is equivalent to np.random.permutation(np.arange(5))[:3]
    
## return index of value
itemindex = numpy.where(array==item)

##Returns the indices of the maximum values along an axis.
np.argmax(matrix, axis=1)


```

pandas

```python    
import pandas as pd
```    

t test

```python
from scipy import stats
stats.ttest_ind(a, b, axis=0, equal_var=True)
```python
