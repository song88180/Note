## sum by column or row
```R
rowSums() #sum by rows
colSums() #sum by column
sum(Data$Column) #sum by column

## Convert the values in a column into row names 
rownames(df) <- df[,1]
df[,1] <- NULL # or df <- df[,-1]

## Convert the values in a row into column names 
rownames(df) <- df[1,]
df[1,] <- NULL # or df <- df[-1,]


```


