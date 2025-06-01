


________________________________________________________________________
mathematical operations
mathematical functions like mean(), avg()
df["visits"].sum()

df.groupby("animal")["age"].mean()


________________________________________________________________________
SQL functions
Joins, Selections, grouping, filter

df.head(3)
df["age"]
df[["name","age"]]

df.loc[["a","b","c"],["age","name"]]
df.loc[df.index[[3,4,8]],["animal","age"]]
df.loc["f","age"] = 1.5

df.iloc[3,6]

conditionals
df[df["visits"]>2]
df[ (df["animal"]=="cat") & (df["age"]<3) ]

df[df["age"].isnull()]
df[ (df["age"]>1) & (df["age"]<5) ]

Groupings
df.groupby("animal")["age"].mean()
df.groupby("animal").value_counts()

Sorting
df.sort_values(by=["age","visits"],ascending=[False,True])

Special Functions
df["priority"] = df["priority"].map({"yes":True,"no":False})

df["animal"] = df["animal"].replace("snake","python")

df.pivot_table(index='animal', columns='visits', values='age', aggfunc='mean')
________________________________________________________________________

handling files
reading and writing to files; chunks;