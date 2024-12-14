# mPLUG: Effective and Efficient Vision-Language Learning by Cross-modal Skip-connections.

[https://arxiv.org/abs/2205.12005](https://arxiv.org/abs/2205.12005)


* Pre-train Datasets

                                                                        
| | COCO | VG | SBU | CC3M | CC13M |
|------------------------|-------------------------------------------|------|------|------|------|
|image | 113K | 100K | 860K | 3M | 10M | 
|text | 567K | 769K | 860K | 3M | 10M |

## Requirements
* [PyTorch](https://pytorch.org/) version >= 1.11.0

* Install other libraries via
```
pip install -r requirements.txt
```

## Fine-tuning

[Download json files of downstream tasks](https://alice-open.oss-cn-zhangjiakou.aliyuncs.com/mPLUG/data.tar)

       
                                                                                          
### Image Captioning
     
                                                                                          
1. Download COCO Caption dataset from the original websites.
2. Download and extract the provided dataset json files.
3. Download language evalution tool([language_evalution](https://alice-open.oss-cn-zhangjiakou.aliyuncs.com/mPLUG/language_evaluation.tar)).
4. In configs/caption_mplug_base.yaml, set the paths for the json files and the image paths.
5. Finetune the pre-trained mplug_base or large model using 8 A100 GPUs:
<pre>sh scripts/caption_mplug_base.sh</pre> 
<pre>sh scripts/caption_mplug_large.sh</pre>  

### Run

1. Open `mPLUG_implementation.ipynb` and Change the paths in the code to your paths for dataset and other directories
2. After installing the requirements, run each cell in the order to the get the required results


                                                                                          






