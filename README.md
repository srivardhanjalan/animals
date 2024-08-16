# Animals
An App to do Machine Learning Classification on Animals. 

### Learning Resources

#### GIT
1. https://blog.gitguardian.com/8-easy-steps-to-set-up-multiple-git-accounts/ [Manage Multiple GIT Accounts on MAC]
   
#### Fast AI
1. https://course.fast.ai (Fast AI Course)
2. https://github.com/fastai/fastbook/tree/master (Fast AI Book)
3. https://docs.fast.ai

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

## Model Training Steps
1. Go to Google Colab to train the model. This Step will create Notebook: https://huggingface.co/spaces/srivardhanjalan/dog-cat-classifier/blob/main/dogs_cats_classifier_model.ipynb
2. Export & Download the Model in the above Notebook after training is done. This Step will generate the file: https://huggingface.co/spaces/srivardhanjalan/dog-cat-classifier/blob/main/dog-cat-classifier-model.pkl
3. Launch Jupyter Notebook Locally
4. Create a Notebook to use the Trained Model above. This Step will create Notebook: https://huggingface.co/spaces/srivardhanjalan/dog-cat-classifier/blob/main/dogs-cats-classifier-app.ipynb
5. Add `#|export` to each cell the will be part of the final Huggingface App.
6. Use `nbdev` to export the App 
```
import nbdev
nbdev.export.nb_export('dogs-cats-classifier-app.ipynb', 'app')
```
7. Create a Huggingface Space for the App, and push the code to the Huggingface Git Repo. Do not forget to include the `requirements.txt` file.
8. Test the App on Huggingface.
9. Use the Gradio API link, at the bottom of the Huggingface App Page to get the Python/Javacript/Curl Documenttaion to access the Model via API
10. Use Github Pages to invoke the Gradio API, and access the model hosted on Huggingface.
11. Checkin all the code. 
12. Done!

## Dog & Cat Classifier
### Huggingface Model & App Repo
https://huggingface.co/spaces/srivardhanjalan/dog-cat-classifier/tree/main


