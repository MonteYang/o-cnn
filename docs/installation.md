# Installation

## PyTorch

The code has been tested with Ubuntu 16.04 and PyTorch 1.6.0.

1. Install PyTorch and relevent packages with the following commands:
   ```shell
   conda create --name pytorch-1.6.0 python=3.7
   conda activate pytorch-1.6.0
   conda install pytorch torchvision cudatoolkit=10.1 -c pytorch
   conda install tqdm yacs -c conda-forge
   ```
2. Build O-CNN under PyTorch.
   ```shell
   cd pytorch
   python setup.py install --build_octree
   ```

3. Run the test cases.
   ```shell
   python -W ignore test/test_all.py -v
   ```