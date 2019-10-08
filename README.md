# Show, Infer and Tell: Contextual Inference for Creative Captioning
Code for the paper, "Show, Infer and Tell: Contextual Inference for Creative Captioning". Paper link: https://bmvc2019.org/wp-content/uploads/papers/0655-paper.pdf 

**The research has been selected for ORAL paper presentations in BMVC 2019. It further received Best Student Paper Award Honourable Mention during the conference.**  

## Code supports:
- Self Critical Sequence Training
- Model Ensemble Averaging 
- Multi-GPU training
- Adam optimizer with reduce on plateau (learning rate reduction when plateaued)

## Requirements
- Python 2.7 (because there is no [coco-caption](https://github.com/tylin/coco-caption) version for python 3)
- PyTorch 0.4 (along with torchvision)
- cider

## Download COCO captions and preprocess them
Extract `dataset_coco.json` from the zip file included in this repository and copy it in to `data/`. This file provides preprocessed captions and also standard train-val-test splits.

The code is based on [ruotianluo](https://github.com/ruotianluo/self-critical.pytorch) and [neuratalk2](https://github.com/karpathy/neuraltalk2). Please refer them for more details on setup.

## Notes about Training
Final model with LSTM size 2048 units is over 2 GB. With a batch size of 10 it take 3GB of GPU space. 

## Evaluate on Karpathy's test split and COCO split
Code includes COCO split option and evaluation script for testing on COCO server.

## Reference
If you use the code, please consider citing:
```
@article{khareshow,
  title={Show, Infer and Tell: Contextual Inference for Creative Captioning},
  author={Khare, Ankit and Huber, Manfred}
}
```

## Acknowledgements
Thanks to google cloud for giving free trial credits, the original [neuraltalk2](https://github.com/karpathy/neuraltalk2),  [rluo](https://github.com/ruotianluo/self-critical.pytorch) and awesome PyTorch team.

