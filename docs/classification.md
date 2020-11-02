# Shape Classification

## O-CNN on PyTorch

1. Data preparation. Change the working directory to `O-CNN/pytorch/projects`
   and follow the instructions [above](classification.md#o-cnn-on-tensorflow) to
   the second step. Place the preprocesed points files into the folder
   `dataset/ModelNet40.points`.

2. Run the following command to train the network.
   ```
   python classification.py --config configs/cls_lenet.yaml
   ```
   
