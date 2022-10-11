# Colorindo Imagens Astronômicas - SIFSC 12

Baixem os dados [aqui](https://github.com/hirobuda/curso-sifsc12).

Notebook, post e NGC3132 aqui(algum dia).

copiem essas funções:

```python
def show_img(img_list, nrow, ncol):

    fig = plt.figure(figsize=(5*(ncol+1), 5*(nrow+1))) 

    gs = gridspec.GridSpec(nrow, ncol,
             wspace=0.05, hspace=0.0, 
             top=1.-0.5/(nrow+1), bottom=0.5/(nrow+1), 
             left=0.5/(ncol+1), right=1-0.5/(ncol+1)) 
    idx = [(0,0), (0,1), (0,2), (1,0), (1,1), (1,2)]

    for i in range(ncol*nrow):
        ax = plt.subplot(gs[idx[i]])
        ax.imshow(img_list[i], "gray")
        ax.set_xticks([])
        ax.set_yticks([])
```

```python
def hist_eq(img, nbins=2**16):

    img_hist, bins = np.histogram(img.flatten(), nbins, density=True)
    cdf = img_hist.cumsum()
    cdf = (nbins-1) * cdf / cdf[-1]

    img_eq = np.interp(img.flatten(), bins[:-1], cdf)

    return img_eq.reshape(img.shape)
```
