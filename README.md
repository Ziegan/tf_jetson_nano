# [How to run Keras model on Jetson Nano](https://www.dlology.com/blog/how-to-run-keras-model-on-jetson-nano/) | DLology Blog


## How to Run
Require [Python 3.5+](https://www.python.org/ftp/python/3.6.7/python-3.6.7.exe) and [Jupyter notebook](https://jupyter.readthedocs.io/en/latest/install.html) installed
### Clone or download this repo
```
git clone https://github.com/Tony607/tf_jetson_nano
```

### Install required libraries for your development machine
`pip3 install -r requirements.txt`

### Step1: Convert Keras model into TensorRT model (On development machine/[Google Colab](https://colab.research.google.com))
Start a terminal, then run,
```
jupyter notebook
```

In the opened browser window open
```
Step1_Colab_TensorRT.ipynb
```

### Step2: Make prediction (On Jetson Nano)
To run notebook on Jetson Nano and make it accessible from another machine, in its terminal run,
```
jupyter notebook --ip=0.0.0.0
```
In another machine's browser, open the notebook,
```
http://<Jetson Nano's LAN IP address>:8888/notebooks/Step2_keras-jetson-ImageNet-predict.ipynb
```