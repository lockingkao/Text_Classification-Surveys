# Text Classification papers/surveys...

This repository contains resources for Natural Language Processing (NLP) with a focus on the task of Text Classification. The content is mainly from paper 《A Survey on Text Classification: From Shallow to Deep Learning》


# Table of Contents

- [Surveys](#surveys)
- [Deep Learning Models](#deep-learning-models)
- [Shallow Learning Models](#shallow-learning-models)
- [Datasets](#datasets)
- [Evaluation Metrics](#evaluation-metrics)
- [Future Research Challenges](#future-research-challenges)
- [Tools and Repos](#tools-and-repos)
</p></blockquote></details>



# Surveys
[:arrow_up:](#table-of-contents)

<details/>
<summary/>
<a href="https://arxiv.org/pdf/2008.00364.pdf">A Survey on Text Classification: From Shallow to Deep Learning,2020</a> by<i> Qian Li, Hao Peng, Jianxin Li, Congying Xia, Renyu Yang, Lichao Sun, Philip S. Yu, Lifang He
</a></summary><blockquote><p align="justify">
Text classification is the most fundamental and essential task in natural language processing. The last decade has seen a surge of research in this area due to the unprecedented success of deep learning. Numerous methods, datasets, and evaluation metrics have been proposed in the literature, raising the need for a comprehensive and updated survey. This paper fills the gap by reviewing the state of the art approaches from 1961 to 2020, focusing on models from shallow to deep learning. We create a taxonomy for text classification according to the text involved and the models used for feature extraction and classification. We then discuss each of these categories in detail, dealing with both the technical developments and benchmark datasets that support tests of predictions. A comprehensive comparison between different techniques, as well as identifying the pros and cons of various evaluation metrics are also provided in this survey. Finally, we conclude by summarizing key implications, future research directions, and the challenges facing the research area.

  
![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/picture1.png)

![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/picture2.png)

</p></blockquote></details>



# Deep Learning Models
[:arrow_up:](#table-of-contents)

#### 2020
 <details/>
<summary/>
  <a href="https://transacl.org/ojs/index.php/tacl/article/view/1853">Spanbert: Improving pre-training by representing and predicting spans</a>  --- SpanBERT--- by<i> Mandar Joshi, Danqi Chen, Yinhan Liu, Daniel S. Weld, Luke Zettlemoyer, Omer Levy
</a>(<a href="https://github.com/facebookresearch/SpanBERT">Github</a>)</summary><blockquote><p align="justify">
We present SpanBERT, a pre-training method that is designed to better represent and predict spans of text. Our approach extends BERT by (1) masking contiguous random spans, rather than random tokens, and (2) training the span boundary representations to predict the entire content of the masked span, without relying on the individual token representations within it. SpanBERT consistently outperforms BERT and our better-tuned baselines, with substantial gains on span selection tasks such as question answering and coreference resolution. In particular, with the same training data and model size as BERT-Large, our single model obtains 94.6% and 88.7% F1 on SQuAD 1.1 and 2.0 respectively. We also achieve a new state of the art on the OntoNotes coreference resolution task (79.6% F1), strong performance on the TACRED relation extraction benchmark, and even gains on GLUE.
  

![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/picture3.png)

</p></blockquote></details>



 <details/>
<summary/>
  <a href="https://openreview.net/forum?id=H1eA7AEtvS">ALBERT: A lite BERT for self-supervised learning of language representations</a> --- ALBERT--- by<i> Zhenzhong Lan, Mingda Chen, Sebastian Goodman, Kevin Gimpel, Piyush Sharma, Radu Soricut
</a> (<a href="https://github.com/google-research/ALBERT">Github</a>)</summary><blockquote><p align="justify">
Increasing model size when pretraining natural language representations often results in improved performance on downstream tasks. However, at some point further model increases become harder due to GPU/TPU memory limitations and longer training times. To address these problems,  we present two parameter-reduction techniques to lower memory consumption and increase the training speed of BERT~\citep{devlin2018bert}. Comprehensive empirical evidence shows that our proposed methods lead to models that scale much better compared to the original BERT. We also use a self-supervised loss that focuses on modeling inter-sentence coherence, and show it consistently helps downstream tasks with multi-sentence inputs. As a result, our best model establishes new state-of-the-art results on the GLUE, RACE, and \squad benchmarks while having fewer parameters compared to BERT-large. The code and the pretrained models are available at https://github.com/google-research/ALBERT.
  

</p></blockquote></details>

#### 2019
 <details/>
<summary/>
  <a href="https://arxiv.org/abs/1907.11692">Roberta: A robustly optimized BERT pretraining approach</a> --- Roberta--- by<i> Yinhan Liu, Myle Ott, Naman Goyal, Jingfei Du, Mandar Joshi, Danqi Chen, Omer Levy, Mike Lewis, Luke Zettlemoyer, Veselin Stoyanov
</a>  (<a href="https://github.com/pytorch/fairseq">Github</a>)</summary><blockquote><p align="justify">
Language model pretraining has led to significant performance gains but careful comparison between different approaches is challenging. Training is computationally expensive, often done on private datasets of different sizes, and, as we will show, hyperparameter choices have significant impact on the final results. We present a replication study of BERT pretraining (Devlin et al., 2019) that carefully measures the impact of many key hyperparameters and training data size. We find that BERT was significantly undertrained, and can match or exceed the performance of every model published after it. Our best model achieves state-of-the-art results on GLUE, RACE and SQuAD. These results highlight the importance of previously overlooked design choices, and raise questions about the source of recently reported improvements. We release our models and code.
  

</p></blockquote></details>

 <details/>
<summary/>
  <a href="http://papers.nips.cc/paper/8812-xlnet-generalized-autoregressive-pretraining-for-language-understanding">Xlnet: Generalized autoregressive pretraining for language understanding</a> --- Xlnet--- by<i> Zhilin Yang, Zihang Dai, Yiming Yang, Jaime Carbonell, Russ R. Salakhutdinov, Quoc V. Le
</a>  (<a href="https://github.com/zihangdai/xlnet">Github</a>)</summary><blockquote><p align="justify">
With the capability of modeling bidirectional contexts, denoising autoencoding based pretraining like BERT achieves better performance than pretraining approaches based on autoregressive language modeling. However, relying on corrupting the input with masks, BERT neglects dependency between the masked positions and suffers from a pretrain-finetune discrepancy. In light of these pros and cons, we propose XLNet, a generalized autoregressive pretraining method that (1) enables learning bidirectional contexts by maximizing the expected likelihood over all permutations of the factorization order and (2) overcomes the limitations of BERT thanks to its autoregressive formulation. Furthermore, XLNet integrates ideas from Transformer-XL, the state-of-the-art autoregressive model, into pretraining. Empirically, under comparable experiment setting, XLNet outperforms BERT on 20 tasks, often by a large margin, including question answering, natural language inference, sentiment analysis, and document ranking.
  

  
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/picture4.png)  
  
</p></blockquote></details>




 <details/>
<summary/>
  <a href="https://www.aclweb.org/anthology/P19-1441/">Multi-task deep neural networks for natural language understanding</a> --- MT-DNN--- by<i> Xiaodong Liu, Pengcheng He, Weizhu Chen, Jianfeng Gao
</a>  (<a href="https://github.com/namisan/mt-dnn">Github</a>)</summary><blockquote><p align="justify">
In this paper, we present a Multi-Task Deep Neural Network (MT-DNN) for learning representations across multiple natural language understanding (NLU) tasks. MT-DNN not only leverages large amounts of cross-task data, but also benefits from a regularization effect that leads to more general representations to help adapt to new tasks and domains. MT-DNN extends the model proposed in Liu et al. (2015) by incorporating a pre-trained bidirectional transformer language model, known as BERT (Devlin et al., 2018). MT-DNN obtains new state-of-the-art results on ten NLU tasks, including SNLI, SciTail, and eight out of nine GLUE tasks, pushing the GLUE benchmark to 82.7% (2.2% absolute improvement) as of February 25, 2019 on the latest GLUE test set. We also demonstrate using the SNLI and SciTail datasets that the representations learned by MT-DNN allow domain adaptation with substantially fewer in-domain labels than the pre-trained BERT representations. Our code and pre-trained models will be made publicly available.
  
 
![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/picture5.png)  
  
</p></blockquote></details>

  


 <details/>
<summary/>
  <a href="https://doi.org/10.18653/v1/n19-1423">BERT: pre-training of deep bidirectional transformers for language understanding</a> --- BERT--- by<i> Jacob Devlin, Ming-Wei Chang, Kenton Lee, Kristina Toutanova
</a> (<a href="https://github.com/google-research/bert">Github</a>)</summary><blockquote><p align="justify">
We introduce a new language representation model called BERT, which stands for Bidirectional Encoder Representations from Transformers. Unlike recent language representation models (Peters et al., 2018a; Radford et al., 2018), BERT is designed to pre-train deep bidirectional representations from unlabeled text by jointly conditioning on both left and right context in all layers. As a result, the pre-trained BERT model can be fine-tuned with just one additional output layer to create state-of-the-art models for a wide range of tasks, such as question answering and language inference, without substantial task-specific architecture modifications. BERT is conceptually simple and empirically powerful. It obtains new state-of-the-art results on eleven natural language processing tasks, including pushing the GLUE score to 80.5 (7.7 point absolute improvement), MultiNLI accuracy to 86.7% (4.6% absolute improvement), SQuAD v1.1 question answering Test F1 to 93.2 (1.5 point absolute improvement) and SQuAD v2.0 Test F1 to 83.1 (5.1 point absolute improvement).
  

![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/picture6.png)  
  
</p></blockquote></details>

  

 <details/>
<summary/>
  <a href="https://wvvw.aaai.org/ojs/index.php/AAAI/article/view/4725">Graph convolutional networks for text classification</a> --- TextGCN---  by<i> Liang Yao, Chengsheng Mao, Yuan Luo
</a>(<a href="https://github.com/yao8839836/text_gcn">Github</a>)</summary><blockquote><p align="justify">
Text classification is an important and classical problem in natural language processing. There have been a number of studies that applied convolutional neural networks (convolution on regular grid, e.g., sequence) to classification. However, only a limited number of studies have explored the more flexible graph convolutional neural networks (convolution on non-grid, e.g., arbitrary graph) for the task. In this work, we propose to use graph convolutional networks for text classification. We build a single text graph for a corpus based on word co-occurrence and document word relations, then learn a Text Graph Convolutional Network (Text GCN) for the corpus. Our Text GCN is initialized with one-hot representation for word and document, it then jointly learns the embeddings for both words and documents, as supervised by the known class labels for documents. Our experimental results on multiple benchmark datasets demonstrate that a vanilla Text GCN without any external word embeddings or knowledge outperforms state-of-the-art methods for text classification. On the other hand, Text GCN also learns predictive word and document embeddings. In addition, experimental results show that the improvement of Text GCN over state-of-the-art comparison methods become more prominent as we lower the percentage of training data, suggesting the robustness of Text GCN to less training data in text classification.
  

![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure7.png)  

</p></blockquote></details>



#### 2018

 <details/>
<summary/>
  <a href="https://doi.org/10.18653/v1/d18-1380">Multi-grained attention network for aspect-level sentiment classification</a> --- MGAN --- by<i> Feifan Fan, Yansong Feng, Dongyan Zhao
</a>(<a href="https://github.com/songyouwei/ABSA-PyTorch">Github</a>)</summary><blockquote><p align="justify">
We propose a novel multi-grained attention network (MGAN) model for aspect level sentiment classification. Existing approaches mostly adopt coarse-grained attention mechanism, which may bring information loss if the aspect has multiple words or larger context. We propose a fine-grained attention mechanism, which can capture the word-level interaction between aspect and context. And then we leverage the fine-grained and coarse-grained attention mechanisms to compose the MGAN framework. Moreover, unlike previous works which train each aspect with its context separately, we design an aspect alignment loss to depict the aspect-level interactions among the aspects that have the same context. We evaluate the proposed approach on three datasets: laptop and restaurant are from SemEval 2014, and the last one is a twitter dataset. Experimental results show that the multi-grained attention network consistently outperforms the state-of-the-art methods on all three datasets. We also conduct experiments to evaluate the effectiveness of aspect alignment loss, which indicates the aspect-level interactions can bring extra useful information and further improve the performance.
  
  
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure8.png)  
</p></blockquote></details>

 <details/>
<summary/>
  <a href="https://doi.org/10.18653/v1/d18-1350">Investigating capsule networks with dynamic routing for text classification</a> --- TextCapsule --- by<i> Min Yang, Wei Zhao, Jianbo Ye, Zeyang Lei, Zhou Zhao, Soufei Zhang
</a>(<a href="https://github.com/andyweizhao/capsule_text_classification">Github</a>)</summary><blockquote><p align="justify">
In this study, we explore capsule networks with dynamic routing for text classification. We propose three strategies to stabilize the dynamic routing process to alleviate the disturbance of some noise capsules which may contain “background” information or have not been successfully trained. A series of experiments are conducted with capsule networks on six text classification benchmarks. Capsule networks achieve state of the art on 4 out of 6 datasets, which shows the effectiveness of capsule networks for text classification. We additionally show that capsule networks exhibit significant improvement when transfer single-label to multi-label text classification over strong baseline methods. To the best of our knowledge, this is the first work that capsule networks have been empirically investigated for text modeling.
  
  
    ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure9.png)  
</p></blockquote></details>


 <details/>
<summary/>
  <a href="https://doi.org/10.24963/ijcai.2018/584">Constructing narrative event evolutionary graph for script event prediction</a> --- SGNN ---  by<i> Zhongyang Li, Xiao Ding, Ting Liu
</a>(<a href="https://github.com/eecrazy/ConstructingNEEG_IJCAI_2018">Github</a>)</summary><blockquote><p align="justify">
Script event prediction requires a model to predict the subsequent event given an existing event context. Previous models based on event pairs or event chains cannot make full use of dense event connections, which may limit their capability of event prediction. To remedy this, we propose constructing an event graph to better utilize the event network information for script event prediction. In particular, we first extract narrative event chains from large quantities of news corpus, and then construct a narrative event evolutionary graph (NEEG) based on the extracted chains. NEEG can be seen as a knowledge base that describes event evolutionary principles and patterns. To solve the inference problem on NEEG, we present a scaled graph neural network (SGNN) to model event interactions and learn better event representations. Instead of computing the representations on the whole graph, SGNN processes only the concerned nodes each time, which makes our model feasible to large-scale graphs. By comparing the similarity between input context event representations and candidate event representations, we can choose the most reasonable subsequent event. Experimental results on widely used New York Times corpus demonstrate that our model significantly outperforms state-of-the-art baseline methods, by using standard multiple choice narrative cloze evaluation.


  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure10.png)  
    
</p></blockquote></details>

 <details/>
<summary/>
  <a href="https://www.aclweb.org/anthology/C18-1330/">SGM: sequence generation model for multi-label classification</a> --- SGM ---  by<i> Pengcheng Yang, Xu Sun, Wei Li, Shuming Ma, Wei Wu, Houfeng Wang
</a>(<a href="https://github.com/lancopku/SGM">Github</a>)</summary><blockquote><p align="justify">
Multi-label classification is an important yet challenging task in natural language processing. It is more complex than single-label classification in that the labels tend to be correlated. Existing methods tend to ignore the correlations between labels. Besides, different parts of the text can contribute differently for predicting different labels, which is not considered by existing models. In this paper, we propose to view the multi-label classification task as a sequence generation problem, and apply a sequence generation model with a novel decoder structure to solve it. Extensive experimental results show that our proposed methods outperform previous work by a substantial margin. Further analysis of experimental results demonstrates that the proposed methods not only capture the correlations between labels, but also select the most informative words automatically when predicting different labels.
  
  
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure11.png)  
  
</p></blockquote></details>


 <details/>
<summary/>
  <a href="https://www.aclweb.org/anthology/P18-1216/">Joint embedding of words and labelsfor text classification</a> --- LEAM ---  by<i> Guoyin Wang, Chunyuan Li, Wenlin Wang, Yizhe Zhang, Dinghan Shen, Xinyuan Zhang, Ricardo Henao, Lawrence Carin
</a>(<a href="https://github.com/guoyinwang/LEAM">Github</a>)</summary><blockquote><p align="justify">
Word embeddings are effective intermediate representations for capturing semantic regularities between words, when learning the representations of text sequences. We propose to view text classification as a label-word joint embedding problem: each label is embedded in the same space with the word vectors. We introduce an attention framework that measures the compatibility of embeddings between text sequences and labels. The attention is learned on a training set of labeled samples to ensure that, given a text sequence, the relevant words are weighted higher than the irrelevant ones. Our method maintains the interpretability of word embeddings, and enjoys a built-in ability to leverage alternative sources of information, in addition to input text sequences. Extensive results on the several large text datasets show that the proposed framework outperforms the state-of-the-art methods by a large margin, in terms of both accuracy and speed.
  
  
   ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure12.png)  
</p></blockquote></details>

 <details/>
<summary/>
  <a href="https://www.aclweb.org/anthology/P18-1031/">Universal language model fine-tuning for text classification</a> --- ULMFiT ---  by<i> Jeremy Howard, Sebastian Ruder
</a>(<a href="http://nlp.fast.ai/category/classification.html">Github</a>)</summary><blockquote><p align="justify">
Inductive transfer learning has greatly impacted computer vision, but existing approaches in NLP still require task-specific modifications and training from scratch. We propose Universal Language Model Fine-tuning (ULMFiT), an effective transfer learning method that can be applied to any task in NLP, and introduce techniques that are key for fine-tuning a language model. Our method significantly outperforms the state-of-the-art on six text classification tasks, reducing the error by 18-24% on the majority of datasets. Furthermore, with only 100 labeled examples, it matches the performance of training from scratch on 100 times more data. We open-source our pretrained models and code.
  
 
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure13.png)  
</p></blockquote></details>

 <details/>
<summary/>
  <a href="https://dl.acm.org/doi/10.1145/3178876.3186005">Large-scale hierarchical text classification withrecursively regularized deep graph-cnn</a> --- DGCNN --- by<i> Hao Peng, Jianxin Li, Yu He, Yaopeng Liu, Mengjiao Bao, Lihong Wang, Yangqiu Song, Qiang Yang
</a>(<a href="https://github.com/HKUST-KnowComp/DeepGraphCNNforTexts">Github</a>)</summary><blockquote><p align="justify">
Text classification to a hierarchical taxonomy of topics is a common and practical problem. Traditional approaches simply use bag-of-words and have achieved good results. However, when there are a lot of labels with different topical granularities, bag-of-words representation may not be enough. Deep learning models have been proven to be effective to automatically learn different levels of representations for image data. It is interesting to study what is the best way to represent texts. In this paper, we propose a graph-CNN based deep learning model to first convert texts to graph-of-words, and then use graph convolution operations to convolve the word graph. Graph-of-words representation of texts has the advantage of capturing non-consecutive and long-distance semantics. CNN models have the advantage of learning different level of semantics. To further leverage the hierarchy of labels, we regularize the deep architecture with the dependency among labels. Our results on both RCV1 and NYTimes datasets show that we can significantly improve large-scale hierarchical text classification over traditional hierarchical text classification and existing deep models.
  
</p></blockquote></details>


 <details/>
<summary/>
  <a href="https://doi.org/10.18653/v1/n18-1202">Deep contextualized word rep-resentations</a> --- ELMo --- by<i> Matthew Peters, Mark Neumann, Mohit Iyyer, Matt Gardner, Christopher Clark, Kenton Lee, Luke Zettlemoyer
</a>(<a href="https://github.com/flairNLP/flair">Github</a>)</summary><blockquote><p align="justify">
We introduce a new type of deep contextualized word representation that models both (1) complex characteristics of word use (e.g., syntax and semantics), and (2) how these uses vary across linguistic contexts (i.e., to model polysemy). Our word vectors are learned functions of the internal states of a deep bidirectional language model (biLM), which is pre-trained on a large text corpus. We show that these representations can be easily added to existing models and significantly improve the state of the art across six challenging NLP problems, including question answering, textual entailment and sentiment analysis. We also present an analysis showing that exposing the deep internals of the pre-trained network is crucial, allowing downstream models to mix different types of semi-supervision signals.
  
</p></blockquote></details>


#### 2017
 <details/>
<summary/>
  <a href="https://www.aclweb.org/anthology/D17-1047/">Recurrent Attention Network on Memory for Aspect Sentiment Analysis</a> --- RAM --- by<i> Peng Chen, Zhongqian Sun, Lidong Bing, Wei Yang
</a>(<a href="https://github.com/songyouwei/ABSA-PyTorch">Github</a>)</summary><blockquote><p align="justify">
We propose a novel framework based on neural networks to identify the sentiment of opinion targets in a comment/review. Our framework adopts multiple-attention mechanism to capture sentiment features separated by a long distance, so that it is more robust against irrelevant information. The results of multiple attentions are non-linearly combined with a recurrent neural network, which strengthens the expressive power of our model for handling more complications. The weighted-memory mechanism not only helps us avoid the labor-intensive feature engineering work, but also provides a tailor-made memory for different opinion targets of a sentence. We examine the merit of our model on four datasets: two are from SemEval2014, i.e. reviews of restaurants and laptops; a twitter dataset, for testing its performance on social media data; and a Chinese news comment dataset, for testing its language sensitivity. The experimental results show that our model consistently outperforms the state-of-the-art methods on different types of data.
  
  
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure14.png) 
</p></blockquote></details>

 <details/>
<summary/>
  <a href="https://doi.org/10.18653/v1/d17-1169">Using millions of emoji occurrences to learn any-domain representations for detecting sentiment, emotion and sarcasm</a> --- DeepMoji --- by<i> Bjarke Felbo, Alan Mislove, Anders Søgaard, Iyad Rahwan, Sune Lehmann
</a>(<a href="https://github.com/bfelbo/DeepMoji">Github</a>)</summary><blockquote><p align="justify">
NLP tasks are often limited by scarcity of manually annotated data. In social media sentiment analysis and related tasks, researchers have therefore used binarized emoticons and specific hashtags as forms of distant supervision. Our paper shows that by extending the distant supervision to a more diverse set of noisy labels, the models can learn richer representations. Through emoji prediction on a dataset of 1246 million tweets containing one of 64 common emojis we obtain state-of-the-art performance on 8 benchmark datasets within emotion, sentiment and sarcasm detection using a single pretrained model. Our analyses confirm that the diversity of our emotional labels yield a performance improvement over previous distant supervision approaches.
  
 
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure15.png) 
</p></blockquote></details>

 <details/>
<summary/>
  <a href="https://www.ijcai.org/Proceedings/2017/568">Interactive attention networks for aspect-level sentiment classification</a> --- IAN --- by<i> Dehong Ma, Sujian Li, Xiaodong Zhang, Houfeng Wang
</a>(<a href="https://github.com/songyouwei/ABSA-PyTorch">Github</a>)</summary><blockquote><p align="justify">
Aspect-level sentiment classification aims at identifying the sentiment polarity of specific target in its context. Previous approaches have realized the importance of targets in sentiment classification and developed various methods with the goal of precisely modeling thier contexts via generating target-specific representations. However, these studies always ignore the separate modeling of targets. In this paper, we argue that both targets and contexts deserve special treatment and need to be learned their own representations via interactive learning. Then, we propose the interactive attention networks (IAN) to interactively learn attentions in the contexts and targets, and generate the representations for targets and contexts separately. With this design, the IAN model can well represent a target and its collocative context, which is helpful to sentiment classification. Experimental results on SemEval 2014 Datasets demonstrate the effectiveness of our model.
  
  
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure16.png) 
</p></blockquote></details>

 <details/>
<summary/>
  <a href="https://doi.org/10.18653/v1/P17-1052">Deep pyramid convolutional neural networks for text categorization</a> --- DPCNN --- by<i> Rie Johnson, Tong Zhang
</a>(<a href="https://github.com/Cheneng/DPCNN">Github</a>)</summary><blockquote><p align="justify">
This paper proposes a low-complexity word-level deep convolutional neural network (CNN) architecture for text categorization that can efficiently represent long-range associations in text. In the literature, several deep and complex neural networks have been proposed for this task, assuming availability of relatively large amounts of training data. However, the associated computational complexity increases as the networks go deeper, which poses serious challenges in practical applications. Moreover, it was shown recently that shallow word-level CNNs are more accurate and much faster than the state-of-the-art very deep nets such as character-level CNNs even in the setting of large training data. Motivated by these findings, we carefully studied deepening of word-level CNNs to capture global representations of text, and found a simple network architecture with which the best accuracy can be obtained by increasing the network depth without increasing computational cost by much. We call it deep pyramid CNN. The proposed model with 15 weight layers outperforms the previous best models on six benchmark datasets for sentiment classification and topic categorization.
  
 
   ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure17.png) 
</p></blockquote></details>


 <details/>
<summary/>
  <a href="https://openreview.net/forum?id=rJbbOLcex">Topicrnn: A recurrent neural network with long-range semantic dependency</a> --- TopicRNN ---  by<i> Adji B. Dieng, Chong Wang, Jianfeng Gao, John Paisley
</a>(<a href="https://github.com/dangitstam/topic-rnn">Github</a>)</summary><blockquote><p align="justify">
In this paper, we propose TopicRNN, a recurrent neural network (RNN)-based language model designed to directly capture the global semantic meaning relating words in a document via latent topics. Because of their sequential nature, RNNs are good at capturing the local structure of a word sequence – both semantic and syntactic – but might face difficulty remembering long-range dependencies. Intuitively, these long-range dependencies are of semantic nature. In contrast, latent topic models are able to capture the global underlying semantic structure of a document but do not account for word ordering. The proposed TopicRNN model integrates the merits of RNNs and latent topic models: it captures local (syntactic) dependencies using an RNN and global (semantic) dependencies using latent topics. Unlike previous work on contextual RNN language modeling, our model is learned end-to-end. Empirical results on word prediction show that TopicRNN outperforms existing contextual RNN baselines. In addition, TopicRNN can be used as an unsupervised feature extractor for documents. We do this for sentiment analysis on the IMDB movie review dataset and report an error rate of 6.28%. This is comparable to the state-of-the-art 5.91% resulting from a semi-supervised approach. Finally, TopicRNN also yields sensible topics, making it a useful alternative to document models such as latent Dirichlet allocation.
  
  
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure18.png) 
</p></blockquote></details>


 <details/>
<summary/>
  <a href="https://openreview.net/forum?id=r1X3g2_xl">Adversarial training methods for semi-supervised text classification</a> --- Miyato et al. ---  by<i> Takeru Miyato, Andrew M. Dai, Ian Goodfellow
</a>(<a href="https://github.com/tensorflow/models/tree/master/adversarial_text">Github</a>)</summary><blockquote><p align="justify">
Adversarial training provides a means of regularizing supervised learning algorithms while virtual adversarial training is able to extend supervised learning algorithms to the semi-supervised setting. However, both methods require making small perturbations to numerous entries of the input vector, which is inappropriate for sparse high-dimensional inputs such as one-hot word representations. We extend adversarial and virtual adversarial training to the text domain by applying perturbations to the word embeddings in a recurrent neural network rather than to the original input itself. The proposed method achieves state of the art results on multiple benchmark semi-supervised and purely supervised tasks. We provide visualizations and analysis showing that the learned word embeddings have improved in quality and that while training, the model is less prone to overfitting.
  
  
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure19.png) 
</p></blockquote></details>


 <details/>
<summary/>
  <a href="https://doi.org/10.18653/v1/e17-2068">Bag of tricks for efficient text classification</a> --- FastText ---  by<i> Armand Joulin, Edouard Grave, Piotr Bojanowski, Tomas Mikolov
</a>(<a href="https://github.com/SeanLee97/short-text-classification">Github</a>)</summary><blockquote><p align="justify">
This paper explores a simple and efficient baseline for text classification. Our experiments show that our fast text classifier fastText is often on par with deep learning classifiers in terms of accuracy, and many orders of magnitude faster for training and evaluation. We can train fastText on more than one billion words in less than ten minutes using a standard multicore CPU, and classify half a million sentences among 312K classes in less than a minute.
  
  
   ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure20.png) 
</p></blockquote></details>



#### 2016

 <details/>
<summary/>
  <a href="https://doi.org/10.18653/v1/d16-1053">Long short-term memory-networks for machine reading</a> --- LSTMN ---  by<i> Jianpeng Cheng, Li Dong, Mirella Lapata
</a>(<a href="https://github.com/JRC1995/Abstractive-Summarization">Github</a>)</summary><blockquote><p align="justify">
In this paper we address the question of how to render sequence-level networks better at handling structured input. We propose a machine reading simulator which processes text incrementally from left to right and performs shallow reasoning with memory and attention. The reader extends the Long Short-Term Memory architecture with a memory network in place of a single memory cell. This enables adaptive memory usage during recurrence with neural attention, offering a way to weakly induce relations among tokens. The system is initially designed to process a single sequence but we also demonstrate how to integrate it with an encoder-decoder architecture. Experiments on language modeling, sentiment analysis, and natural language inference show that our model matches or outperforms the state of the art.
  
 
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure21.png) 
</p></blockquote></details>

 <details/>
<summary/>
  <a href="https://www.ijcai.org/Abstract/16/408">Recurrent neural network for text classification with multi-task learning</a> --- Multi-Task --- by<i> Pengfei Liu, Xipeng Qiu, Xuanjing Huang
</a>(<a href="https://github.com/baixl/text_classification">Github</a>)</summary><blockquote><p align="justify">
Neural network based methods have obtained great progress on a variety of natural language processing tasks. However, in most previous works, the models are learned based on single-task supervised objectives, which often suffer from insufficient training data. In this paper, we use the multi-task learning framework to jointly learn across multiple related tasks. Based on recurrent neural network, we propose three different mechanisms of sharing information to model text with task-specific and shared layers. The entire network is trained jointly on all these tasks. Experiments on four benchmark text classification tasks show that our proposed models can improve the performance of a task with the help of other related tasks.
  
  
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure22.png) 
</p></blockquote></details>

 <details/>
<summary/>
  <a href="https://doi.org/10.18653/v1/n16-1174">Hierarchical attention networks for document classification</a> --- HAN --- by<i> Zichao Yang, Diyi Yang, Chris Dyer, Xiaodong He, Alex Smola, Eduard Hovy
</a>(<a href="https://github.com/richliao/textClassifier">Github</a>)</summary><blockquote><p align="justify">
We propose a hierarchical attention networkfor document classification.  Our model hastwo distinctive characteristics: (i) it has a hier-archical structure that mirrors the hierarchicalstructure of documents; (ii) it has two levelsof attention mechanisms applied at the word-and sentence-level, enabling it to attend dif-ferentially to more and less important con-tent when constructing the document repre-sentation. Experiments conducted on six largescale text classification tasks demonstrate thatthe proposed architecture outperform previousmethods by a substantial margin. Visualiza-tion of the attention layers illustrates that themodel selects qualitatively informative wordsand sentences.
  
  
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure23.png) 
</p></blockquote></details>


#### 2015

 <details/>
<summary/>
  <a href="http://papers.nips.cc/paper/5782-character-level-convolutional-networks-for-text-classification">Character-level convolutional networks for text classification</a> --- CharCNN --- by<i> Xiang Zhang, Junbo Zhao, Yann LeCun
</a>(<a href="https://github.com/mhjabreel/CharCNN">Github</a>)</summary><blockquote><p align="justify">
This article offers an empirical exploration on the use of character-level convolutional networks (ConvNets) for text classification. We constructed several large-scale datasets to show that character-level convolutional networks could achieve state-of-the-art or competitive results. Comparisons are offered against traditional models such as bag of words, n-grams and their TFIDF variants, and deep learning models such as word-based ConvNets and recurrent neural networks.
  
 
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure24.png) 
</p></blockquote></details>

 <details/>
<summary/>
  <a href="https://doi.org/10.3115/v1/p15-1150">Improved semantic representations from tree-structured long short-term memory networks</a> --- Tree-LSTM ---  by<i> Kai Sheng Tai, Richard Socher, Christopher D. Manning
</a>(<a href="https://github.com/stanfordnlp/treelstm">Github</a>)</summary><blockquote><p align="justify">
Because  of  their  superior  ability  to  pre-serve   sequence   information   over   time,Long  Short-Term  Memory  (LSTM)  net-works,   a  type  of  recurrent  neural  net-work with a more complex computationalunit, have obtained strong results on a va-riety  of  sequence  modeling  tasks.Theonly underlying LSTM structure that hasbeen  explored  so  far  is  a  linear  chain.However,  natural  language  exhibits  syn-tactic properties that would naturally com-bine words to phrases.  We introduce theTree-LSTM, a generalization of LSTMs totree-structured network topologies.  Tree-LSTMs  outperform  all  existing  systemsand strong LSTM baselines on two tasks:predicting the semantic relatedness of twosentences  (SemEval  2014,  Task  1)  andsentiment  classification  (Stanford  Senti-ment Treebank).
  
 
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure25.png) 
</p></blockquote></details>


 <details/>
<summary/>
  <a href="https://doi.org/10.3115/v1/p15-1162">Deep unordered composition rivals syntactic methods for text classification</a> --- DAN ---  by<i> Mohit Iyyer, Varun Manjunatha, Jordan Boyd-Graber, Hal Daumé III
</a>(<a href="https://github.com/miyyer/dan">Github</a>)</summary><blockquote><p align="justify">
Many  existing  deep  learning  models  fornatural language processing tasks focus onlearning thecompositionalityof their in-puts, which requires many expensive com-putations. We present a simple deep neuralnetwork that competes with and, in somecases,  outperforms  such  models  on  sen-timent  analysis  and  factoid  question  an-swering tasks while taking only a fractionof the training time.  While our model issyntactically-ignorant, we show significantimprovements over previous bag-of-wordsmodels by deepening our network and ap-plying a novel variant of dropout.  More-over, our model performs better than syn-tactic models on datasets with high syn-tactic variance.  We show that our modelmakes similar errors to syntactically-awaremodels, indicating that for the tasks we con-sider, nonlinearly transforming the input ismore important than tailoring a network toincorporate word order and syntax.
  
 
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure26.png) 
</p></blockquote></details>


 <details/>
<summary/>
  <a href="http://www.aaai.org/ocs/index.php/AAAI/AAAI15/paper/view/9745">Recurrent convolutional neural networks for text classification</a> --- TextRCNN ---  by<i> Siwei Lai, Liheng Xu, Kang Liu, Jun Zhao
</a>(<a href="https://github.com/roomylee/rcnn-text-classification">Github</a>)</summary><blockquote><p align="justify">
Text classification is a foundational task in many NLP applications. Traditional text classifiers often rely on many human-designed features, such as dictionaries, knowledge bases and special tree kernels. In contrast to traditional methods, we introduce a recurrent convolutional neural network for text classification without human-designed features. In our model, we apply a recurrent structure to capture contextual information as far as possible when learning word representations, which may introduce considerably less noise compared to traditional window-based neural networks. We also employ a max-pooling layer that automatically judges which words play key roles in text classification to capture the key components in texts. We conduct experiments on four commonly used datasets. The experimental results show that the proposed method outperforms the state-of-the-art methods on several datasets, particularly on document-level datasets.
  
</p></blockquote></details>



#### 2014
 <details/>
<summary/>
  <a href="http://proceedings.mlr.press/v32/le14.html">Distributed representations of sentences and documents</a> --- Paragraph-Vec ---  by<i> Quoc Le, Tomas Mikolov
</a>(<a href="https://github.com/inejc/paragraph-vectors">Github</a>)</summary><blockquote><p align="justify">
Many machine learning algorithms require the input to be represented as a fixed length feature vector. When it comes to texts, one of the most common representations is bag-of-words. Despite their popularity, bag-of-words models have two major weaknesses: they lose the ordering of the words and they also ignore semantics of the words. For example, "powerful," "strong" and "Paris" are equally distant. In this paper, we propose an unsupervised algorithm that learns vector representations of sentences and text documents. This algorithm represents each document by a dense vector which is trained to predict words in the document. Its construction gives our algorithm the potential to overcome the weaknesses of bag-of-words models. Empirical results show that our technique outperforms bag-of-words models as well as other techniques for text representations. Finally, we achieve new state-of-the-art results on several text classification and sentiment analysis tasks.
  
 
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure27.png)
</p></blockquote></details>

 <details/>
<summary/>
  <a href="https://doi.org/10.3115/v1/p14-1062">A convolutional neural network for modelling sentences</a> --- DCNN ---  by<i> Nal Kalchbrenner, Edward Grefenstette, Phil Blunsom
</a>(<a href="https://github.com/kinimod23/ATS_Project">Github</a>)</summary><blockquote><p align="justify">
The ability to accurately represent sentences is central to language understanding. We describe a convolutional architecture dubbed the Dynamic Convolutional Neural Network (DCNN) that we adopt for the semantic modelling of sentences. The network uses Dynamic k-Max Pooling, a global pooling operation over linear sequences. The network handles input sentences of varying length and induces a feature graph over the sentence that is capable of explicitly capturing short and long-range relations. The network does not rely on a parse tree and is easily applicable to any language. We test the DCNN in four experiments: small scale binary and multi-class sentiment prediction, six-way question classification and Twitter sentiment prediction by distant supervision. The network achieves excellent performance in the first three tasks and a greater than 25% error reduction in the last task with respect to the strongest baseline.
  
   
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure28.png)
</p></blockquote></details>

 <details/>
<summary/>
  <a href="https://www.aclweb.org/anthology/D14-1181.pdf">Convolutional Neural Networks for Sentence Classification</a> --- TextCNN --- by<i> Yoon Kim
</a>(<a href="https://github.com/alexander-rakhlin/CNN-for-Sentence-Classification-in-Keras">Github</a>)</summary><blockquote><p align="justify">
We report on a series of experiments with convolutional neural networks (CNN) trained on top of pre-trained word vectors for sentence-level classification tasks. We show that a simple CNN with little hyperparameter tuning and static vectors achieves excellent results on multiple benchmarks. Learning task-specific vectors through fine-tuning offers further gains in performance. We additionally propose a simple modification to the architecture to allow for the use of both task-specific and static vectors. The CNN models discussed herein improve upon the state of the art on 4 out of 7 tasks, which include sentiment analysis and question classification.
  
 
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure29.png)
</p></blockquote></details>

#### 2013
 <details/>
<summary/>
  <a href="https://www.aclweb.org/anthology/D13-1170/">Recursive deep models for semantic compositionality over a sentiment treebank</a> --- RNTN --- by<i> Richard Socher, Alex Perelygin, Jean Wu, Jason Chuang, Christopher D. Manning, Andrew Ng, Christopher Potts
</a>(<a href=" https://github.com/pondruska/DeepSentiment">Github</a>)</summary><blockquote><p align="justify">
Semantic word spaces have been very useful but cannot express the meaning of longer phrases in a principled way. Further progress towards understanding compositionality in tasks such as sentiment detection requires richer supervised training and evaluation resources and more powerful models of composition. To remedy this, we introduce a Sentiment Treebank. It includes fine grained sentiment labels for 215,154 phrases in the parse trees of 11,855 sentences and presents new challenges for sentiment composition-ality. To address them, we introduce the Recursive Neural Tensor Network. When trained on the new treebank, this model outperforms all previous methods on several metrics. It pushes the state of the art in single sentence positive/negative classification from 80% up to 85.4%. The accuracy of predicting fine-grained sentiment labels for all phrases reaches 80.7%, an improvement of 9.7% over bag of features baselines. Lastly, it is the only model that can accurately capture the effects of negation and its scope at various tree levels for both positive and negative phrases.
  
  
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure30.png)
</p></blockquote></details>


#### 2012
 <details/>
<summary/>
  <a href="https://www.aclweb.org/anthology/D12-1110/">Semantic compositionality through recursive matrix-vector spaces</a> --- MV-RNN --- by<i> Richard Socher, Brody Huval, Christopher D. Manning, Andrew Y. Ng
</a>(<a href="https://github.com/github-pengge/MV_RNN">Github</a>)</summary><blockquote><p align="justify">
Single-word vector space models have been very successful at learning lexical information. However, they cannot capture the compositional meaning of longer phrases, preventing them from a deeper understanding of language. We introduce a recursive neural network (RNN) model that learns compositional vector representations for phrases and sentences of arbitrary syntactic type and length. Our model assigns a vector and a matrix to every node in a parse tree: the vector captures the inherent meaning of the constituent, while the matrix captures how it changes the meaning of neighboring words or phrases. This matrix-vector RNN can learn the meaning of operators in propositional logic and natural language. The model obtains state of the art performance on three different experiments: predicting fine-grained sentiment distributions of adverb-adjective pairs; classifying sentiment labels of movie reviews and classifying semantic relationships such as cause-effect or topic-message between nouns using the syntactic path between them.
  
  
   ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure31.png)
</p></blockquote></details>

#### 2011
 <details/>
<summary/>
  <a href="https://www.aclweb.org/anthology/D11-1014/">Semi-supervised recursive autoencoders forpredicting sentiment distributions</a> --- RAE --- by<i> Richard Socher, Jeffrey Pennington, Eric H. Huang, Andrew Y. Ng, Christopher D. Manning
</a>(<a href="https://github.com/alexander-rakhlin/CNN-for-Sentence-Classification-in-Keras">Github</a>)</summary><blockquote><p align="justify">
We introduce a novel machine learning frame-work based on recursive autoencoders for sentence-level prediction of sentiment labeldistributions. Our method learns vector spacerepresentations for multi-word phrases. In sentiment prediction tasks these represen-tations outperform other state-of-the-art ap-proaches on commonly used datasets, such asmovie reviews, without using any pre-definedsentiment lexica or polarity shifting rules. Wealso  evaluate  the  model’s  ability to predict sentiment distributions on a new dataset basedon confessions from the experience project. The dataset consists of personal user storiesannotated with multiple labels which, whenaggregated, form a multinomial distributionthat captures emotional reactions. Our algorithm can more accurately predict distri-butions over such labels compared to severalcompetitive baselines.
  
  
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure32.png)
   
</p></blockquote></details>




# Shallow Learning Models
[:arrow_up:](#table-of-contents)

#### 2017
 <details/>
<summary/>
  <a href="http://papers.nips.cc/paper/6907-lightgbm-a-highly-efficient-gradient-boosting-decision-tree">Lightgbm: A highly efficient gradient boosting decision tree</a> --- LightGBM --- by<i> Guolin Ke, Qi Meng, Thomas Finley, Taifeng Wang, Wei Chen, Weidong Ma, Qiwei Ye, Tie-Yan Liu
</a>(<a href="https://github.com/creatist/text_classify">Github</a>)</summary><blockquote><p align="justify">
Gradient Boosting Decision Tree (GBDT) is a popular machine learning algorithm, and has quite a few effective implementations such as XGBoost and pGBRT. Although many engineering optimizations have been adopted in these implementations, the efficiency and scalability are still unsatisfactory when the feature dimension is high and data size is large. A major reason is that for each feature, they need to scan all the data instances to estimate the information gain of all possible split points, which is very time consuming. To tackle this problem, we propose two novel techniques: \emph{Gradient-based One-Side Sampling} (GOSS) and \emph{Exclusive Feature Bundling} (EFB). With GOSS, we exclude a significant proportion of data instances with small gradients, and only use the rest to estimate the information gain. We prove that, since the data instances with larger gradients play a more important role in the computation of information gain, GOSS can obtain quite accurate estimation of the information gain with a much smaller data size. With EFB, we bundle mutually exclusive features (i.e., they rarely take nonzero values simultaneously), to reduce the number of features. We prove that finding the optimal bundling of exclusive features is NP-hard, but a greedy algorithm can achieve quite good approximation ratio (and thus can effectively reduce the number of features without hurting the accuracy of split point determination by much). We call our new GBDT implementation with GOSS and EFB \emph{LightGBM}. Our experiments on multiple public datasets show that, LightGBM speeds up the training process of conventional GBDT by up to over 20 times while achieving almost the same accuracy.
  
</p></blockquote></details>

#### 2016
 <details/>
<summary/>
  <a href="https://dl.acm.org/doi/10.1145/2939672.2939785">Xgboost: A scalable tree boosting system</a> --- XGBoost ---  by<i> Tianqi Chen, Carlos Guestrin
</a>(<a href="https://xgboost.readthedocs.io/en/latest">Github</a>)</summary><blockquote><p align="justify">
Tree boosting is a highly effective and widely used machine learning method. In this paper, we describe a scalable end-to-end tree boosting system called XGBoost, which is used widely by data scientists to achieve state-of-the-art results on many machine learning challenges. We propose a novel sparsity-aware algorithm for sparse data and weighted quantile sketch for approximate tree learning. More importantly, we provide insights on cache access patterns, data compression and sharding to build a scalable tree boosting system. By combining these insights, XGBoost scales beyond billions of examples using far fewer resources than existing systems.
  
  
  ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/figure33.png)
</p></blockquote></details>


#### 2001
<details/>
<summary/>
 <a href="https://link.springer.com/article/10.1023%2FA%3A1010933404324"> --- Random Forests (RF) --- by<i> Leo Breiman 
</a></a> (<a href="https://github.com/hexiaolang/RandomForest-In-text-classification">{Github}</a>) </summary><blockquote><p align="justify">
  Random forests are a combination of tree predictors such that each tree depends on the values of a random vector sampled independently and with the same distribution for all trees in the forest. The generalization error for forests converges a.s. to a limit as the number of trees in the forest becomes large. The generalization error of a forest of tree classifiers depends on the strength of the individual trees in the forest and the correlation between them. Using a random selection of features to split each node yields error rates that compare favorably to Adaboost (Y. Freund & R. Schapire, Machine Learning: Proceedings of the Thirteenth International conference, ***, 148–156), but are more robust with respect to noise. Internal estimates monitor error, strength, and correlation and these are used to show the response to increasing the number of features used in the splitting. Internal estimates are also used to measure variable importance. These ideas are also applicable to regression.
  
</p></blockquote></details>

#### 1998
<details/>
<summary/>
<a href="https://xueshu.baidu.com/usercenter/paper/show?paperid=58aa6cfa340e6ae6809c5deadd07d88e&site=xueshu_se">Text categorization with Support Vector Machines: Learning with many relevant features (SVM)</a>  by<i> JOACHIMS,T.
</a> (<a href="https://github.com/Gunjitbedi/Text-Classification">{Github}</a>) </summary><blockquote><p align="justify">
  This paper explores the use of Support Vector Machines (SVMs) for learning text classifiers from examples. It analyzes the particular properties of learning with text data and identifies why SVMs are appropriate for this task. Empirical results support the theoretical findings. SVMs achieve substantial improvements over the currently best performing methods and behave robustly over a variety of different learning tasks. Furthermore they are fully automatic, eliminating the need for manual parameter tuning.
  
 </p></blockquote></details>

#### 1993
<details/>
<summary/>
<a href="https://link.springer.com/article/10.1007/BF00993309">C4.5: Programs for Machine Learning (C4.5)</a> by<i> Steven L. Salzberg 
</a>  (<a href="https://github.com/Cater5009/Text-Classify">{Github}</a>) </summary><blockquote><p align="justify">
</p></blockquote></details>

#### 1984
<details/>
<summary/>
<a href="https://dblp.org/img/paper.dark.empty.16x16.png">Classification and Regression Trees (CART)</a> by<i> Chyon-HwaYeh
</a> (<a href="https://github.com/sayantann11/all-classification-templetes-for-ML">{Github}</a>) </summary><blockquote><p align="justify">
  </p></blockquote></details>

#### 1967
<details/>
<summary/>
<a href="https://dl.acm.org/doi/10.1145/321075.321084">Nearest neighbor pattern classification (k-nearest neighbor classification,KNN)</a> by<i> M. E. Maron
</a> (<a href="https://github.com/raimonbosch/knn.classifier">{Github}</a>) </summary><blockquote><p align="justify">
  The nearest neighbor decision rule assigns to an unclassified sample point the classification of the nearest of a set of previously classified points. This rule is independent of the underlying joint distribution on the sample points and their classifications, and hence the probability of errorRof such a rule must be at least as great as the Bayes probability of errorR^{\ast}--the minimum probability of error over all decision rules taking underlying probability structure into account. However, in a large sample analysis, we will show in theM-category case thatR^{\ast} \leq R \leq R^{\ast}(2 --MR^{\ast}/(M-1)), where these bounds are the tightest possible, for all suitably smooth underlying distributions. Thus for any number of categories, the probability of error of the nearest neighbor rule is bounded above by twice the Bayes probability of error. In this sense, it may be said that half the classification information in an infinite sample set is contained in the nearest neighbor.
  
 </p></blockquote></details>


#### 1961 

<details/>
<summary/>
<a href="https://dl.acm.org/doi/10.1145/321075.321084">Automatic indexing: An experimental inquiry</a> by<i> M. E. Maron
</a> (<a href="https://github.com/Gunjitbedi/Text-Classification">{Github}</a>) </summary><blockquote><p align="justify">
  This inquiry examines a technique for automatically classifying (indexing) documents according to their subject content. The task, in essence, is to have a computing machine read a document and on the basis of the occurrence of selected clue words decide to which of many subject categories the document in question belongs. This paper describes the design, execution and evaluation of a modest experimental study aimed at testing empirically one statistical technique for automatic indexing.
  
 </p></blockquote></details>





# Datasets
[:arrow_up:](#table-of-contents)

#### Sentiment Analysis (SA) 情感分析
SA is the process of analyzing and reasoning the subjective text withinemotional color. It is crucial to get information on whether it supports a particular point of view fromthe text that is distinct from the traditional text classification that analyzes the objective content ofthe text. SA can be binary or multi-class. Binary SA is to divide the text into two categories, includingpositive and negative. Multi-class SA classifies text to multi-level or fine-grained labels. 


<details/>
<summary/> <a href="http://www.cs.cornell.edu/people/pabo/movie-review-data/">Movie Review (MR) </a></summary><blockquote><p align="justify">
The MR is a movie review dataset, each of which correspondsto a sentence. The corpus has 5,331 positive data and 5,331 negative data. 10-fold cross-validationby random splitting is commonly used to test MR. 
  
  </p></blockquote></details>

<details/>
<summary/> <a href="http://www.cs.uic.edu/∼liub/FBS/sentiment-analysis.html">Stanford Sentiment Treebank (SST) </a></summary><blockquote><p align="justify">
The SST [175] is an extension of MR. It has two cate-gories. SST-1 with fine-grained labels with five classes. It has 8,544 training texts and 2,210 testtexts, respectively. Furthermore, SST-2 has 9,613 texts with binary labels being partitioned into6,920 training texts, 872 development texts, and 1,821 testing texts.
  
</p></blockquote></details>

<details/>
<summary/> <a href="http://www.cs.pitt.edu/mpqa/">The Multi-Perspective Question Answering (MPQA)</a></summary><blockquote><p align="justify">
The MPQA is an opinion dataset. It has two class labels and also an MPQA dataset of opinion polarity detection sub-tasks.MPQA includes 10,606 sentences extracted from news articles from various news sources. It shouldbe noted that it contains 3,311 positive texts and 7,293 negative texts without labels of each text.
  
 </p></blockquote></details>

<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/kdd/DiaoQWSJW14">IMDB reviews IMDB评论</a></summary><blockquote><p align="justify">
The IMDB review is developed for binary sentiment classification of filmreviews with the same amount in each class. It can be separated into training and test groups onaverage, by 25,000 comments per group.
  
</p></blockquote></details>

<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/emnlp/TangQL15">Yelp reviews </a></summary><blockquote><p align="justify">
The Yelp review is summarized from the Yelp Dataset Challenges in 2013,2014, and 2015. This dataset has two categories. Yelp-2 of these were used for negative and positiveemotion classification tasks, including 560,000 training texts and 38,000 test texts. Yelp-5 is used todetect fine-grained affective labels with 650,000 training and 50,000 test texts in all classes.
  
 </p></blockquote></details>

<details/>
<summary/> <a href="https://www.kaggle.com/datafiniti/consumer-reviews-of-amazon-products">Amazon Reviews (AM) 亚马逊评论数据集</a></summary><blockquote><p align="justify">
The AM is a popular corpus formed by collecting Amazon websiteproduct reviews [190]. This dataset has two categories. The Amazon-2 with two classes includes 3,600,000 training sets and 400,000 testing sets. Amazon-5, with five classes, includes 3,000,000 and650,000 comments for training and testing.
  
 </p></blockquote></details>


#### News Classification (NC) 
News content is one of the most crucial information sources which hasa critical influence on people. The NC system facilitates users to get vital knowledge in real-time.News classification applications mainly encompass: recognizing news topics and recommendingrelated news according to user interest. The news classification datasets include 20NG, AG, R8, R52,Sogou, and so on. Here we detail several of the primary datasets.


<details/>
<summary/>
<a href="http://ana.cachopo.org/datasets-for-single-label-text-categorization">20 Newsgroups (20NG)</a></summary><blockquote><p align="justify">
 The 20NG is a newsgroup text dataset. It has 20 categories withthe same number of each category and includes 18,846 texts.
  

</p></blockquote></details>

<details/>
<summary/> <a href="http://www.di.unipi.it/~gulli/AG_corpus_of_news_articles.html">AG News (AG)</a></summary><blockquote><p align="justify">
The AG News is a search engine for news from academia, choosingthe four largest classes. It uses the title and description fields of each news. AG contains 120,000texts for training and 7,600 texts for testing.
  
</p></blockquote></details>

<details/>
<summary/> <a href="https://www.cs.umb.edu/~smimarog/textmining/datasets/">R8 and R52</a></summary><blockquote><p align="justify">
R8 and R52 are two subsets which are the subset of Reuters. R8 has 8categories, divided into 2,189 test files and 5,485 training courses. R52 has 52 categories, split into6,532 training files and 2,568 test files.
  
</p></blockquote></details>

<details/>
<summary/> <a href="https://dblp.org/rec/conf/cncl/SunQXH19.bib">Sogou News (Sogou) </a></summary><blockquote><p align="justify">
The Sogou News combines two datasets, including SogouCA andSogouCS news sets. The label of each text is the domain names in the URL.
 
</p></blockquote></details>

#### Topic Labeling (TL) 
The topic analysis attempts to get the meaning of the text by defining thesophisticated text theme. The topic labeling is one of the essential components of the topic analysistechnique, intending to assign one or more subjects for each document to simplify the topic analysis.


<details/>
<summary/> <a href="https://dblp.org/rec/journals/semweb/LehmannIJJKMHMK15.bib">DBpedia</a></summary><blockquote><p align="justify">
The DBpedia is a large-scale multi-lingual knowledge base generated usingWikipedia’s most ordinarily used infoboxes. It publishes DBpedia each month, adding or deletingclasses and properties in every version. DBpedia’s most prevalent version has 14 classes and isdivided into 560,000 training data and 70,000 test data. 
  
 </p></blockquote></details>

<details/>
<summary/> <a href="http://davis.wpi.edu/xmdv/datasets/ohsumed.html">Ohsumed</a></summary><blockquote><p align="justify">
The Ohsumed belongs to the MEDLINE database. It includes 7,400 texts andhas 23 cardiovascular disease categories. All texts are medical abstracts and are labeled into one ormore classes.
  
</p></blockquote></details>

<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">Yahoo answers (YahooA) </a></summary><blockquote><p align="justify">
The YahooA is a topic labeling task with 10 classes. It includes140,000 training data and 5,000 test data. All text contains three elements, being question titles,question contexts, and best answers, respectively.
  
</p></blockquote></details>


#### Question Answering (QA) 
The QA task can be divided into two types: the extractive QA and thegenerative QA. The extractive QA gives multiple candidate answers for each question to choosewhich one is the right answer. Thus, the text classification models can be used for the extractiveQA task. The QA discussed in this paper is all extractive QA. The QA system can apply the textclassification model to recognize the correct answer and set others as candidates. The questionanswering datasets include SQuAD, MS MARCO, TREC-QA, WikiQA, and Quora [209]. Here wedetail several of the primary datasets.



<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">Stanford Question Answering Dataset (SQuAD） </a></summary><blockquote><p align="justify">
The SQuAD is a set of question and answer pairs obtained from Wikipedia articles. The SQuAD has two categories. SQuAD1.1 contains 536 pairs of 107,785 Q&A items. SQuAD2.0 combines 100,000 questions in SQuAD1.1 with morethan 50,000 unanswerable questions that crowd workers face in a form similar to answerable questions.
  
</p></blockquote></details>

<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">MS MARCO</a></summary><blockquote><p align="justify">
The MS MARCO contains questions and answers. The questions and part ofthe answers are sampled from actual web texts by the Bing search engine. Others are generative. Itis used for developing generative QA systems released by Microsoft.
  
</p></blockquote></details>

<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">TREC-QA</a></summary><blockquote><p align="justify">
The TREC-QA includes 5,452 training texts and 500 testing texts. It has two versions. TREC-6 contains 6 categories, and TREC-50 has 50 categories.
  
</p></blockquote></details>

<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">WikiQA</a></summary><blockquote><p align="justify">
The WikiQA dataset includes questions with no correct answer, which needs toevaluate the answer.
  
</p></blockquote></details>



#### Natural Language Inference (NLI) 
NLI is used to predict whether the meaning of one text canbe deduced from another. Paraphrasing is a generalized form of NLI. It uses the task of measuringthe semantic similarity of sentence pairs to decide whether one sentence is the interpretation ofanother. The NLI datasets include SNLI, MNLI, SICK, STS, RTE, SciTail, MSRP, etc. Here we detailseveral of the primary datasets.


<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">The Stanford Natural Language Inference (SNLI)</a></summary><blockquote><p align="justify">
The SNLI is generally applied toNLI tasks. It contains 570,152 human-annotated sentence pairs, including training, development,and test sets, which are annotated with three categories: neutral, entailment, and contradiction.
  
</p></blockquote></details>

<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">Multi-Genre Natural Language Inference (MNLI)</a></summary><blockquote><p align="justify">
The Multi-NLI is an expansion of SNLI, embracing a broader scope of written and spoken text genres. It includes 433,000 sentencepairs annotated by textual entailment labels.
  
</p></blockquote></details>

<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">Sentences Involving Compositional Knowledge (SICK)</a></summary><blockquote><p align="justify">
The SICK contains almost10,000 English sentence pairs. It consists of neutral, entailment and contradictory labels.

</p></blockquote></details>

<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">Microsoft Research Paraphrase (MSRP)</a></summary><blockquote><p align="justify">
The MSRP consists of sentence pairs, usuallyfor the text-similarity task. Each pair is annotated by a binary label to discriminate whether theyare paraphrases. It respectively includes 1,725 training and 4,076 test sets.
  
</p></blockquote></details>



#### Dialog Act Classification (DAC) 
A dialog act describes an utterance in a dialog based on semantic,pragmatic, and syntactic criteria. DAC labels a piece of a dialog according to its category of meaningand helps learn the speaker’s intentions. It is to give a label according to dialog. Here we detailseveral of the primary datasets, including DSTC 4, MRDA, and SwDA.


<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">Dialog State Tracking Challenge 4 (DSTC 4)</a></summary><blockquote><p align="justify">
The DSTC 4 is used for dialog act classi-fication. It has 89 training classes, 24,000 training texts, and 6,000 testing texts.
  
</p></blockquote></details>

<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">ICSI Meeting Recorder Dialog Act (MRDA)</a></summary><blockquote><p align="justify">
The MRDA is used for dialog act classifi-cation. It has 5 training classes, 51,000 training texts, 11,000 testing texts, and 11,000 validation texts.
  
</p></blockquote></details>

<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">Switchboard Dialog Act (SwDA)</a></summary><blockquote><p align="justify">
The SwDA is used for dialog act classification. It has43 training classes, 1,003,000 training texts, 19,000 testing texts and 112,000 validation texts.
  
</p></blockquote></details>


#### Multi-label datasets 
In multi-label classification, an instance has multiple labels, and each la-bel can only take one of the multiple classes. There are many datasets based on multi-label textclassification. It includes Reuters, Education, Patent, RCV1, RCV1-2K, AmazonCat-13K, BlurbGen-reCollection, WOS-11967, AAPD, etc. Here we detail several of the main datasets.

<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">Reuters news</a></summary><blockquote><p align="justify">
The Reuters is a popularly used dataset for text classification fromReuters financial news services. It has 90 training classes, 7,769 training texts, and 3,019 testingtexts, containing multiple labels and single labels. There are also some Reuters sub-sets of data,such as R8, BR52, RCV1, and RCV1-v2.
  
</p></blockquote></details>


<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">Patent Dataset</a></summary><blockquote><p align="justify">
The Patent Dataset is obtained from USPTO1, which is a patent system gratingU.S. patents containing textual details such title and abstract. It contains 100,000 US patents awardedin the real-world with multiple hierarchical categories.
  
</p></blockquote></details>


<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">Reuters Corpus Volume I (RCV1) and RCV1-2K</a></summary><blockquote><p align="justify">
The RCV1 is collected from Reuters News articles from 1996-1997, which is human-labeled with 103 categories. It consists of 23,149 training and 784,446 testing texts, respectively. The RCV1-2K dataset has the same features as the RCV1. However, the label set of RCV1-2K has been expanded with some new labels. It contains2456 labels.
  
</p></blockquote></details>


<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">Web of Science (WOS-11967)</a></summary><blockquote><p align="justify">
The WOS-11967 is crawled from the Web of Science,consisting of abstracts of published papers with two labels for each example. It is shallower, butsignificantly broader, with fewer classes in total.
  
</p></blockquote></details>

<details/>
<summary/> <a href="https://dblp.org/rec/bib/conf/nips/ZhangZL15">Arxiv Academic Paper Dataset (AAPD)</a></summary><blockquote><p align="justify">
The AAPD is a large dataset in the computer science field for the multi-label text classification from website2. It has 55,840 papers, including the abstract and the corresponding subjects with 54 labels in total. The aim is to predict the corresponding subjects of each paper according to the abstract.
  
</p></blockquote></details>


#### Others 
There are some datasets for other applications, such as Geonames toponyms, Twitter posts,and so on.


# Evaluation Metrics
[:arrow_up:](#table-of-contents)

In terms of evaluating text classification models, accuracy and F1 score are the most used to assessthe text classification methods. Later, with the increasing difficulty of classification tasks or theexistence of some particular tasks, the evaluation metrics are improved. For example, evaluationmetrics such as P@K and Micro-F1 are used to evaluate multi-label text classification performance,and MRR is usually used to estimate the performance of QA tasks.


#### Single-label metrics 
Single-label text classification divides the text into one of the most likelycategories applied in NLP tasks such as QA, SA, and dialogue systems [9]. For single-label textclassification, one text belongs to just one catalog, making it possible not to consider the relationsamong labels. Here we introduce some evaluation metrics used for single-label text classificationtasks.



<details/>
<summary/> <a>Accuracy and Error Rate</a></summary><blockquote><p align="justify">
Accuracy and Error Rate are the fundamental metrics for a text classification model. The Accuracy and Error Rate are respectively defined as
  
  
   ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/1.png)
</p></blockquote></details>

<details/>
<summary/> <a >Precision, Recall and F1</a></summary><blockquote><p align="justify">
These are vital metrics utilized for unbalanced test sets regardless ofthe standard type and error rate. For example, most of the test samples have a class label. F1 is theharmonic average of Precision and Recall. Accuracy, Recall, and F1 as defined
  
   
   ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/2.png)
  
  The desired results will be obtained when the accuracy, F1 and recall value reach 1. On the contrary,when the values become 0, the worst result is obtained. For the multi-class classification problem,the precision and recall value of each class can be calculated separately, and then the performanceof the individual and whole can be analyzed.
  
  </p></blockquote></details>

<details/>
<summary/> <a>Exact Match (EM)</a></summary><blockquote><p align="justify">
The EM is a metric for QA tasks measuring the prediction that matches all theground-truth answers precisely. It is the primary metric utilized on the SQuAD dataset.
  
</p></blockquote></details>


<details/>
<summary/> <a >Mean Reciprocal Rank (MRR)</a></summary><blockquote><p align="justify">
The EM is a metric for QA tasks measuring the prediction that matches all theground-truth answers precisely. It is the primary metric utilized on the SQuAD dataset.
  
</p></blockquote></details>

<details/>
<summary/> <a >Hamming-loss (HL)</a></summary><blockquote><p align="justify">
The HL assesses the score of misclassified instance-label pairs wherea related label is omitted or an unrelated is predicted.
  
</p></blockquote></details>


#### Multi-label metrics 
Compared with single-label text classification, multi-label text classifica-tion divides the text into multiple category labels, and the number of category labels is variable. These metrics are designed for single label text classification, which are not suitable for multi-label tasks. Thus, there are some metrics designed for multi-label text classification.


<details/>
<summary/> <a >Micro−F1</a></summary><blockquote><p align="justify">
The Micro−F1 is a measure that considers the overall accuracy and recall of alllabels. The Micro−F1is defined as
  
   
   ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/3.png)
    ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/4.png)
</p></blockquote></details>


<details/>
<summary/> <a >Macro−F1</a></summary><blockquote><p align="justify">
The Macro−F1 calculates the average F1 of all labels. Unlike Micro−F1, which setseven weight to every example, Macro−F1 sets the same weight to all labels in the average process. Formally, Macro−F1is defined as
  
  
   ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/5.png)
    ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/6.png)
</p></blockquote></details>

In addition to the above evaluation metrics, there are some rank-based evaluation metrics forextreme multi-label classification tasks, including P@K and NDCG@K.


<details/>
<summary/> <a >Precision at Top K (P@K)</a></summary><blockquote><p align="justify">
The P@K is the precision at the top k. ForP@K, each text has a set of L ground truth labels Lt={l0,l1,l2...,lL−1}, in order of decreasing probability Pt=p0,p1,p2...,pQ−1.The precision at k is
  
   
   ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/7.png)
</p></blockquote></details>

<details/>
<summary/> <a>Normalized Discounted Cummulated Gains (NDCG@K)</a></summary><blockquote><p align="justify">
The NDCG at k is
  
  
   ![image](https://github.com/xiaoqian19940510/text-classification-surveys/blob/master/figures/9.png)
  
</p></blockquote></details>


# Future Research Challenges
[:arrow_up:](#table-of-contents)






#### 数据层面

对于文本分类任务，无论是浅层学习还是深度学习方法，数据对于模型性能都是必不可少的。研究的文本数据主要包括多章，短文本，跨语言，多标签，少样本文本。对于这些数据的特征，现有的技术挑战如下：


<details/>
<summary/>
<a >Zero-shot/Few-shot learning</a> </summary><blockquote><p align="justify">
  当前的深度学习模型过于依赖大量标记数据。这些模型的性能在零镜头或少镜头学习中受到显着影响。
</p></blockquote></details>

<details/>
<summary/>
<a >外部知识</a>  </summary><blockquote><p align="justify">
  我们都知道，输入的有益信息越多，DNN的性能就越好。因此，认为添加外部知识(知识库或知识图)是提高模型性能的有效途径。然而，如何添加以及添加什么仍然是一个挑战。
</p></blockquote></details>

<details/>
<summary/>
<a >多标签文本分类任务</a>  </summary><blockquote><p align="justify">
  多标签文本分类需要充分考虑标签之间的语义关系，并且模型的嵌入和编码是有损压缩的过程。因此，如何减少训练过程中层次语义的丢失以及如何保留丰富而复杂的文档语义信息仍然是一个亟待解决的问题。
</p></blockquote></details>

<details/>
<summary/>
<a >具有许多术语词汇的特殊领域</a> </summary><blockquote><p align="justify">
  特定领域的文本（例如金融和医学文本）包含许多特定的单词或领域专家，可理解的语，缩写等，这使现有的预训练单词向量难以使用。
</p></blockquote></details>


#### 模型层面

现有的浅层和深度学习模型的大部分结构都被尝试用于文本分类，包括集成方法。BERT学习了一种语言表示法，可以用来对许多NLP任务进行微调。主要的方法是增加数据，提高计算能力和设计训练程序，以获得更好的结果如何在数据和计算资源和预测性能之间权衡是值得研究的。

#### 性能评估层面

浅层模型和深层模型可以在大多数文本分类任务中取得良好的性能，但是需要提高其结果的抗干扰能力。如何实现对深度模型的解释也是一个技术挑战。

<details/>
<summary/>
<a >模型的语义鲁棒性</a>  </summary><blockquote><p align="justify">
  近年来，研究人员设计了许多模型来增强文本分类模型的准确性。但是，如果数据集中有一些对抗性样本，则模型的性能会大大降低。因此，如何提高模型的鲁棒性是当前研究的热点和挑战。
</p></blockquote></details>

<details/>
<summary/>
<a >模型的可解释性</a> </summary><blockquote><p align="justify">
  DNN在特征提取和语义挖掘方面具有独特的优势，并且已经完成了出色的文本分类任务。但是，深度学习是一个黑盒模型，训练过程难以重现，隐式语义和输出可解释性很差。它对模型进行了改进和优化，丢失了明确的准则。此外，我们无法准确解释为什么该模型可以提高性能。
</p></blockquote></details>


# Tools and Repos
[:arrow_up:](#table-of-contents)


<details>
<summary><a href="https://github.com/Tencent/NeuralNLP-NeuralClassifier">NeuralClassifier</a></summary><blockquote><p align="justify">
腾讯的开源NLP项目
</p></blockquote></details>


<details>
<summary><a href="https://github.com/nocater/baidu_nlp_project2">baidu_nlp_project2</a></summary><blockquote><p align="justify">
百度NLP项目
</p></blockquote></details>



<details>
<summary><a href="https://github.com/TianWuYuJiangHenShou/textClassifier">Multi-label</a></summary><blockquote><p align="justify">
多标签文本分类项目
</p></blockquote></details>
