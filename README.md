# Exploration of Machine Learning for Signal Processing Topics in Image Denoising 

# About this repo 

In the spring of 2023, I created my own special course at DTU, under the guidance of Tommy. My goal for this was to continue exploring the concepts from Machine Learning for Signal Processing (20477), a course I took in the Fall of 2022. While the intersection of data and signal processing was a topic I have enjoyed in the past, I was not sure what work in this field actually looked like, in terms of where it could be used, and what are the specific methods and algorithms that people working in this field are using right now. My goal with this course were to answer these questions, and I went about doing it in two parts: first I conducted a literature review to develop an overview understanding of the field, then I choose a couple of algorithms from my literature review and implemented them. Additionally, I had wanted to apply the algorithms I created to a real-world topic, but ran out of time (more on this below). 

This repo contains the code for the implementation of the algorithms that I have learned during my special course, as well as small experiments that test the properties of those algorithms. This readme will serve as the landing page for my work, and here you will be able to read about the algorithms I explored and how to run my implementations. The reader will also find my final report in this repo, which explores my process and takeaways in greater depth. 

# Repo Structure 

This repo is divided into two main sections: an exploration on unrolled ISTA and on unrolled optimization with deep priors. In each of the respective subfolders you will find notebooks with isolated explorations into the topics. Below you will find two tables describing the notebooks in each subfolder. 

### Unrolled ISTA 

Unrolled ISTA involves taking the ISTA algorithm, which is an iterative sparsity promoting signal processing algorithm, and represents each iteration as a layer in a neural network. Although we covered ISTA in class, I was still a bit hazy on the material, so I dedicate the first notebook in this series for gaining a better intuition for it. In the second, I experiment with applying traditional ISTA to image denoising. In the last, I implement the unrolled ISTA algorithm and also apply it to image denoising.

| File 	| Short Description 	|
|---	|---	|
| ISTA_preliminary.ipynb 	| An implementation of the ISTA and FISTA algorithms, applied to a small example 	|
| ISTA_pyproximal.ipynb 	| Using pyproximal's ISTA and FISTA implementations to denoise images and observe results 	|
| ISTA_unrolled.ipynb 	| An implementation of unrolled ISTA, applied to image denoising 	|

### Unrolled Optimization with Deep Priors

Unrolled optimization with deep priors revolves around the idea of also running traditional iterative algorithms, but with the caveat of having a neural network learn the hyperparameters. 

| File 	| Short Description 	|
|---	|---	|
| unrolled_deep_priors.ipynb 	| An implementation of unrolled optimization with deep priors applied to image denoising 	|

# How to run the repo 

## Downloading and preparing the image denoising files 

I test both algorithms on the BSDS500 image dataset. In order to run the files, this dataset will need to be downloaded, which can be done [here](https://www2.eecs.berkeley.edu/Research/Projects/CS/vision/bsds/). 

Note that I also ran most of files on Google Colab, which pulls the files from Google Drive. I suggest that the user also save the dataset to a Google Drive folder titled 'BSDS500'. 

After the user has done that they will need to format their data to the correct structure.

I created a script to prepare the files according to the instructions that Diamond et al used to prepare the same data for *Unrolled Optimization*. This script is called `dataPreprocessing.ipynb` and can be found in this repo. 


## Running the files

All the notebooks are designed to be run in Google colab. 

# Additional Resources 

My literature review can be found [here](https://www.zotero.org/alli105/collections/J5PMCFZH).
