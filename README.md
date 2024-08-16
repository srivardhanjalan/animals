# Animals
An App to do Machine Learning Classification on Animals. 

### Resources

#### GIT
1. [Manage Multiple GIT Accounts on MAC](https://blog.gitguardian.com/8-easy-steps-to-set-up-multiple-git-accounts/)
   
#### Fast AI
1. [Fast AI Course](https://course.fast.ai)
2. [Fast AI Book](https://github.com/fastai/fastbook/tree/master)
3. [Fast AI Docs](https://docs.fast.ai)
4. [Fast AI Forum - Part 1: Lesson 1 to 8](https://forums.fast.ai/t/lesson-1-official-topic/95287)
5. [Fast AI Forum - Part 2: Lesson 9 to 25](https://forums.fast.ai/t/lesson-9-official-topic/100562)

#### Huggingface
1. Create a [Huggingface Account](https://www.huggingface.co/) - This is needed to Host the trained Model
2. Next, Click on the [Spaces](https://huggingface.co/spaces) Tab and create a new Space for your Model.
3. Select `Gradio` as the Space SDK
   
#### Google Colab
1. [Google Colab](https://colab.research.google.com) - This is needed to Train the Model
```
Remember to change the Runtime Environment to GPU or TPU while training models. This will have a major performance increase while Model Training, than CPU (default selection).
While on your Colab Jupyter Notebook, Go to -> Runtime -> Change Runtime Type -> Select the GPU or TPU for the session.
```
2. [TPU VS GPU Comparison](https://www.datacamp.com/blog/tpu-vs-gpu-ai)

#### Github Pages
1. [Github Pages Quickstart](https://docs.github.com/en/pages/quickstart)
2. [Deploying to Github Pages using gh-pages](https://dev.to/scc33/deploying-to-github-pages-using-gh-pages-2d95)
3. [Deploying a General Web App (HTML, CSS, JS) on GitHub Pages](https://gist.github.com/promto-c/e46ca197f324a2148af919e18c18b5e6)

#### Jupyter Notebooks
1. [Jupyter Notebooks 101](https://www.kaggle.com/code/jhoward/jupyter-notebook-101)

#### Gradio
1. https://www.gradio.app

#### Local Development Setup
1. After developing & training the ML Model on Google Colab, we export and download the Model (.pkl file) to our local machine.
2. Downloading the Model to our local machine will enable us to launch Jupter Notebooks locally, and run queries against the Trained Model.
3. We can run queries against the Trained Model locally, as it does not require GPU resources to run. 
4. Local Setup (Run the following on the Terminal)
```
# clone git repo: https://github.com/fastai/fastsetup
git clone https://github.com/fastai/fastsetup.git

# run the following command to setup conda
./fastsetup/setup-conda.sh

# install libraries using conda
conda install pytorch torchvision -c pytorch
conda install -c fastai fastai  
conda install conda-forge::gradio
conda install -c fastai nbdev

# install and run Jupyter Notebook locally
conda install jupyter
jupyter notebook --no-browser
```

## Model Training Steps
1. Go to Google Colab to train the model. This Step will create Notebook: [dogs_cats_classifier_model.ipynb](https://huggingface.co/spaces/srivardhanjalan/dog-cat-classifier/blob/main/dogs_cats_classifier_model.ipynb)
2. Export & Download the Model in the above Notebook after training is done. This Step will generate the file: [dog-cat-classifier-model.pkl](https://huggingface.co/spaces/srivardhanjalan/dog-cat-classifier/blob/main/dog-cat-classifier-model.pkl)
3. Launch Jupyter Notebook Locally
4. Create a Notebook to use the Trained Model above. This Step will create Notebook: [dogs-cats-classifier-app.ipynb](https://huggingface.co/spaces/srivardhanjalan/dog-cat-classifier/blob/main/dogs-cats-classifier-app.ipynb)
5. Add `#|export` to each cell the will be part of the final Huggingface App.
6. Use `nbdev` to export the App 
```
import nbdev
nbdev.export.nb_export('dogs-cats-classifier-app.ipynb', 'app')
```
7. The above step will generate a `app.py` file with the code in the cell marked with `#|export` in the Notebook from Step 4.
8. Create a Huggingface Space for the App, and push the code to the Huggingface Git Repo. Do not forget to include the `requirements.txt` file.
9. Test the App on Huggingface.
10. Use the Gradio API link, at the bottom of the Huggingface App Page to get the Python/Javacript/Curl Documenttaion to access the Model via API
11. Add a new Page in the Github Repo, with the HTML and Javascript needed to invoke the Gradio API, and access the model hosted on Huggingface.
12. Ensure Github Pages shows the new Page.
13. Done!

## Code Checking Steps
Ensure the following files are checked-in to the Huggingface Spaces Git Repo for each Model
1. The Jupyter Notebook used for Model Training from Google Colab. All Colab Notebooks are stored in [Google Drive](https://drive.google.com/drive/home) under the folder `Colab Notebooks`.
2. The Training Data used to Train the Model.
3. The .pkl Trained Model File.
4. The Jupyter Notebook used to run queries on the Trained Model locally.
5. The `app.py` File, generated using the local Jupyter Notebook.

## Dog & Cat Classifier
### Huggingface Model & App Repo
https://huggingface.co/spaces/srivardhanjalan/dog-cat-classifier/tree/main


