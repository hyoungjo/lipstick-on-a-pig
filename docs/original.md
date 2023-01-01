# Lipstick on a Pig

This project includes the experiments described in the [paper](https://arxiv.org/pdf/1903.03862.pdf): 

**"Lipstick on a Pig: Debiasing Methods Cover up Systematic Gender Biases in Word Embeddings But do not Remove Them"**, Hila Gonen and Yoav Goldberg, NAACL 2019.

Full reimplementation of the experiments is available in "remaining_bias_2016.ipynb" for Bolukbasi's embeddings, and in "remaining_bias_2018.ipynb" for Zhao's embeddings.  

## About

The authors state as follows in the paper:

"Word embeddings derived from text corpora reflect gender biases in society. ... ... Both works ([Bolukbasi et al., 2016](https://proceedings.neurips.cc/paper/2016/file/a486cd07e4ac3d270571622f4f316ec5-Paper.pdf); [Zhao et al., 2018](https://arxiv.org/pdf/1809.01496.pdf)) substantially reduced gender bias with respect to the same definition: the projection on the gender direction (i.e. *he* - *she*). ... ... We argue that current debiasing methods, which lean on the above deﬁnition for gender bias and directly target it, are mostly hiding the bias rather than removing it."

> Bolukbasi et al., 2016. [Man is to Computer Programmer as Woman is to Homemaker? Debiasing Word Embeddings](https://arxiv.org/abs/1607.06520) (NeurIPS 2022)  
> Zhao et al., 2018. [Learning Gender-Neutral Word Embeddings](https://aclanthology.org/D18-1521) (EMNLP 2018)

Here, the authors use the term *systematic* gender bias, which refers to those biases that are hidden when seen with gender direction, but revealed with authors' experiments.

## Data and Experiments

To be brief, data (word embeddings) follows Bolukbasi et al. (2016) and reduce the vocabulary with several processings. This leaves 26,189 and 47,698 words for Bolukbasi et al. (2016) and Zhao et al. (2018), respectively. With those embeddings, authors conduct below five experiments to show that gender bias still exists after debiasing.

- Experiment 1: Male- and female-biased words cluster together
- Experiment 2: Bias-by-projection correlates to bias-by-neighbours
- Experiment 3: Professions
- Experiment 4: Association between female/male and female/male-stereotyped words
- Experiment 5: Classifying previously female- and male-biased words
