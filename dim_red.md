
one applicatino of dimensionality reduction is **data compression**

![data_comp](https://i.gyazo.com/6bd9d995760b9c32d5b0285dbe01e777.png)
  - the benefit is we can train our learning algorithms on the compressed data, making it run faster
  
3D => 2D:

![data_comp_3d_to_2d](https://i.gyazo.com/2a7eedf55ab0fed9e2daa0a451234a33.png)

anoterh application is **data visualization**
  - we can summarize data much better
  
![all_data](https://i.gyazo.com/d5133e798be340903ea7069b4cbfb3dc.png)

to

![new_data](https://i.gyazo.com/faae2b7e9ff7e09b358c05ac859413a8.png)

**principal component analysis** is dimemsionality reduction
  -goal is to minimize sum of projected distances onto the lower dimensioned space
  
![PCA](https://i.gyazo.com/3f775f756d5578b01eb50c598095ff6d.png)


## pca algorithm

1. preprocess with feature scaling + mean normalization
2. reduce n-dim to k-dim:
  ![ntok](https://i.gyazo.com/63ae596e92ac029bff897c0273f1448f.png)
  - select first k columns in U matrix
  ![ntok](https://i.gyazo.com/347bf77b122358cce41e5ff9930f9942.png)
  
## reconstruction from compressed representation

![recon](https://i.gyazo.com/b8612a9d50355192e54221879923c3e4.png)

## choosing # of principal components (k)

![choose_k](https://i.gyazo.com/a4fb2e11f6118c226abf769bb8732aac.png)

algo:
![a;go](https://i.gyazo.com/d065dae5f540897b878f516f3bf062c2.png)
  - keeep incrementing k (max is k=n)

## advice for applyinc PCA

supervised learning with high dimensional data:
![sup](https://i.gyazo.com/f944efa6f59178bbc1fbb41fef6346f1.png)

application summary:
![sum](https://i.gyazo.com/942ebaa84e5cf61e46920e94413a1103.png)

bad usage of PCA:
  - do not use it simply to reduce # of features to prevent overfitting. high level idea is it doesnt take advantage that in supervised learning, we have labels. but pca ignores that info. 
  - better to use regularization
  
another (possibly) bad usage:
![pca_app](https://i.gyazo.com/b0f38f9fedb293ef07e5ccc620848981.png)


