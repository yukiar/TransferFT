# Transfer fine-tuned BERT models by paraphrases
This repository provides transfer fine-tuned BERT models by paraphrases, which show strong performance in sentence pair modeling tasks, e.g., paraphrase identification, semantic textual similarity aseessment, and natural language inference.
For details of model training, please refer to the following paper.

Yuki Arase and Junichi Tsujii. 2019. Transfer Fine-Tuning: A BERT Case Study. in Proc. of Conference on Empirical Methods in Natural Language Processing (EMNLP 2019). [paper at arXiv](https://arxiv.org/abs/1909.00931)

When you have any publication using our models, please cite the paper above.

## Models
Please download the trained models at [Zenodo](http://doi.org/10.5281/zenodo.3524708)

## Usage
### Pre-requisit
Our training codes depend on [pytorch-pretrained-bert](https://github.com/huggingface/transformers/releases/tag/v0.6.2) (former version of [transformers](https://github.com/huggingface/transformers)).
Please first install pytorch and pytorch-pretrained-bert. 

Note: Our models should work on transformers as well without any problem, but we have not tested yet.

### Load models
Once you have pytorch and pytorch-pretrained-bert installed, our models can be used in the same manner with BERT's pre-trained models. 
Just load our models like:
```python
self.bert = BertModel.from_pretrained('bert-base-uncased')
self.load_state_dict(torch.load('path-to-downloaded-model'))
```
