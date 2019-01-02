```python
##  concatenate element in the list
myList = ','.join(myList) 
# if elements are not string type
myList = ','.join(map(str, myList))   # separate with comma

dict.fromkeys([key1, key2, key3, key4]) # initialize a dict with keys from a list and empty value.
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
itemindex = numpy.where(array==item)[0]

##Returns the indices of the maximum values along an axis.
np.argmax(matrix, axis=1)

##calculate std
np.std(a, axis=0)


```

pandas

```python    
import pandas as pd

## create a dictionary of two pandas Dataframe columns
df = DataFrame(randint(0,10,10000).reshape(5000,2),columns=['A','B'])
dict(zip(df.A,df.B)) # common
Series(df.A.values,index=df.B).to_dict() . # faster

## insert column into existed dataframe
df['My new column'] = 'default value' # most common
df.insert(0, 'new column', 'default value') # this one specifies the order

```    

t test

```python
from scipy import stats
stats.ttest_ind(a, b, axis=0, equal_var=True)
```

re
https://docs.python.org/2/library/re.html
```python
import re
#Split string by the occurrences of pattern.
re.split(pattern, string, maxsplit=0, flags=0)  

#Compile a regular expression pattern into a regular expression object, which can be used for matching using its match() and search() methods
prog = re.compile(pattern)
result = prog.match(string)

re.match("c", "abcdef")    # No match
re.search("c", "abcdef")   # Match
```

conda
```bash
#export environment.yml
conda info --envs # See all available conda environments
source activate [myenv] # Activate the environment to export
conda env export > environment.yml # export
```
