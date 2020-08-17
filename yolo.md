- splits image into boxes and for each box outputs N * 8 values where N is the number of object classes. We use anchor boxes to extract box objects. Then run nms:

![yolo](https://i.gyazo.com/6a056008a9166f34f00f1f1bbf3ab412.png)


![nms](https://i.gyazo.com/813afea5d6577d7d09c481b227581b4f.png)


## what yolo sees
![see](https://i.gyazo.com/92e29e117ac76f22d9bf7e5d123616ce.png)
  - this is how a box finds the "center" of the object! after coloring each box according to the msot popular class, we can create a box for that object!
  
  
