# PMFSNet

论文复现：

![image-20250604153728722](assets/image-20250604153728722.png)

数据集：[MMTO](https://pan.baidu.com/share/init?surl=0AT7fqgbK2s507tr1MfpTQ&pwd=mo3c)

训练命令参数：

```py
--dataset: dataset name
--model: model name
--pretrain_weight: pre-trained weight file path
--dimension: dimension of dataset images and models, for PMFSNet only
--scaling_version: scaling version of PMFSNet, for PMFSNet only
--epoch: training epoch
```

训练命令：

```py
python ./train.py --dataset MMOTU --model PMFSNet --pretrain_weight ./pretrain/PMFSNet2D-basic_ILSVRC2012.pth --dimension 2d --scaling_version BASIC --epoch 2000
```

测试集验证命令(命令参数同训练)：

```py
python ./test.py --dataset MMOTU --model PMFSNet --pretrain_weight ./pretrain/PMFSNet2D-BASIC_MMOTU.pth --dimension 2d --scaling_version BASIC
```

图片分割推理命令：

```py
python ./inference.py --dataset MMOTU --model PMFSNet --pretrain_weight ./pretrain/PMFSNet2D-BASIC_MMOTU.pth --dimension 2d --scaling_version BASIC --image_path ./images/453.JPG
```

