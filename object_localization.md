![local](https://i.gyazo.com/d8e04fc128035e8d7643f67fa56d7932.png)

localization builds on the classifier pipeline by outputting 4 values which give the boundding box of the object:
![local](https://i.gyazo.com/d447e0f7b11383a245a23cc1f02b9e69.png)

more formally:

![form](https://i.gyazo.com/5ad727d7001c5a53d4f2118b77de770d.png)
  - pc = 0 means object does not exist so all attributes become "dont cares"
  - if y1 = 0, then the object does not exist so loss is then calculated as whether or not an object was "found"
  
