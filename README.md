
# O-CNN on PyTorch

1. Download [ModelNet40](http://modelnet.cs.princeton.edu/ModelNet40.zip) dataset
   and unzip it to the folder `dataset/ModelNet40` via the following command:
    ```
    python ../data/cls_modelnet.py --run download_m40
    ```

2. Convert triangle meshes (in `off` format) to point clouds (in `points` format)
   with the [virtual_scanner](https://github.com/wang-ps/O-CNN/tree/master/virtual_scanner).
   This process can be automatically executed by the following command.
   Remember to provide actual `<The path of the virtual_scanner>` to run the command.
    ```shell
    python ../data/cls_modelnet.py --run m40_convert_mesh_to_points \
                                   --scanner <The path of the virtual_scanner>
    ```
   The generated point clouds are very dense, and if you would like to save disk
   spaces, you can optionally run the following command to simplify the point cloud.
    ```shell
    python ../data/cls_modelnet.py --run m40_simplify_points 
    ```
   We also provide the converted `point clouds` for convenience. Download the zip file
   [here](https://www.dropbox.com/s/m233s9eza3acj2a/ModelNet40.points.zip?dl=0) and
   unzip it to the folder `dataset/ModelNet40.points`.
   ```shell
   python ../data/cls_modelnet.py --run download_m40_points
   ```

3. Run the following command to train the network.
   ```
   python classification.py --config configs/cls_lenet.yaml
   ```
   
