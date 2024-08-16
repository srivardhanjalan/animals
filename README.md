# Animals
An App to do Machine Learning Classification on Animals. 

### Learning Resources
#### Fast AI
1. https://course.fast.ai
2. https://docs.fast.ai

#### Google Colab
** Remember to change to GPU or TPU while training models. While on your Colab Jupyter Notebook, Go to -> Runtime -> Change Runtime Type -> Select the GPU or TPU for the session.
1. https://www.datacamp.com/blog/tpu-vs-gpu-ai

#### Github Pages
1. https://docs.github.com/en/pages/quickstart
2. https://dev.to/scc33/deploying-to-github-pages-using-gh-pages-2d95
3. https://gist.github.com/promto-c/e46ca197f324a2148af919e18c18b5e6 [Deploying a General Web App (HTML, CSS, JS) on GitHub Pages]

#### Local Deployment
1. After developing & training the ML Model on Google Colab, we download the model locally.
2. After the .pkl Model file has been downloaded we can load the trained Model and run queries against it.
3. This can be done locally using Jupyter Notebooks (as we only need Colab and the GPU respurces to train the model). 
4. Local Setup (Run the following on the Terminal)
```
  conda install pytorch torchvision -c pytorch
  conda install -c fastai fastai  
  conda install conda-forge::gradio
  conda install -c fastai nbdev
  conda install jupyter
  jupyter notebook --no-browser
```


## Dog & Cat Classifier
### Huggingface Model Repo
https://huggingface.co/spaces/srivardhanjalan/dog-cat-classifier/tree/main
### Google Colab Notebook
https://colab.research.google.com/#fileId=https%3A//huggingface.co/spaces/srivardhanjalan/dog-cat-classifier/blob/main/dogs-cats-classifier-app.ipynb


