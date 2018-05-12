# Auto-clean-CNN-model

This is our implementation for the paper:

​Chen, H., Xu, J., Xiao, G., Wu, Q., & Zhang, S. (2017). Fast auto-clean CNN model for online prediction of food materials. Journal of Parallel and Distributed Computing.

## Documentation

### [imagedata](https://github.com/Winckwu/Auto-clean-CNN-model/tree/master/imgdata) 

Data preprocessing scripts used in this thesis, 
- `Validate` is the food materials datasets used for model validation, `all-others` are dirty images, and the other folders are clean food materials images datasets.
- The two text files `train.txt` and `test.txt` are lists of training images and test images
- Use `create_lmdb.sh` to call the convert_imageset command to convert the data format
- Use `create_mean.sh` to calculate the mean and save the file
- Convert the mean file to python readable format using `convert_mean.py`
- Since the food materials datasets are already used for business, if you need these datasets, please let us know and can be obtained by emailing winck.wu@gmail.com.

### [netconfig](https://github.com/Winckwu/Auto-clean-CNN-model/tree/master/netconfig)
- We modified the `solver.prototxt` and `train_auto_clean.prototxt` files to train the model.
- Run `train.sh` script to start training the model
- `deploy_auto_clean.prototxt` is the network configuration file for testing
- Test data with `classify_auto_clean.py`

## Environment
- STRIX-GTX1060 GPU
- Ubuntu 16.04.1
- Python version: '2.7'
- We made use of the deep learning framework [BVLC/Caffe](https://github.com/BVLC/caffe), the caffe installation tutorial can see https://github.com/Winckwu/Caffe-GPU-ubuntu16.04-install
