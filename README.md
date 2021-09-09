# Federated Deep AUC Maximization  [![pdf](https://img.shields.io/badge/Arxiv-pdf-orange.svg?style=flat)](https://arxiv.org/abs/2102.04635)

This is the official implementation of the paper "**Federated Deep AUC Maximization for Heterogeneous Data with a Constant Communication Complexity**" published on **ICML2021**. 

Requirements
---------
```
Tensorflow >= 2.0.0
PyTorch >= 1.3.0
```


How to run 
---------
```
python -m torch.distributed.launch --nproc_per_node=4 --nnodes=1 --node_rank=0 --master_addr='YOUR IP' --master_port=8888 \
            main_codasca_cifar.py --T0=4000 --imratio=0.1 --gamma=500 --lr=0.1 --I=8 --local_batchsize=32 --total_iter=20000
```

Citation
---------
If you find this repo helpful, please cite the following paper:
```
@InProceedings{DBLP:conf/icml/YuanGXYY21,
  title = 	 {Federated Deep AUC Maximization for Hetergeneous Data with a Constant Communication Complexity},
  author =       {Yuan, Zhuoning and Guo, Zhishuai and Xu, Yi and Ying, Yiming and Yang, Tianbao},
  booktitle = 	 {Proceedings of the 38th International Conference on Machine Learning},
  pages = 	 {12219--12229},
  year = 	 {2021},
  editor = 	 {Meila, Marina and Zhang, Tong},
  volume = 	 {139},
  series = 	 {Proceedings of Machine Learning Research},
  month = 	 {18--24 Jul},
  publisher =    {PMLR},
  pdf = 	 {http://proceedings.mlr.press/v139/yuan21a/yuan21a.pdf},
  url = 	 {https://proceedings.mlr.press/v139/yuan21a.html},
}

```
