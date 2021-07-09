# BNN-Training

First, install pytorch.

## CPU-based Training 

If no GPU is available, just run

```python run_fashion_cpu.py --batch-size=256 --epochs=100 --lr=0.001 --step-size=25 --no-cuda```.


## CUDA-based Training

For faster training CUDA support is needed. To enable it, install pybind11 and CUDA toolkit.

Then, to install CUDA-kernels for fast binarization, go to folder ```code/cuda/binarizationPM1``` and run

```python setup.py install --user```

After successful installation, run the GPU-based training with

```python run_fashion.py --batch-size=256 --epochs=10 --lr=0.001 --step-size=25```.


The code is based on the MNIST example in https://github.com/pytorch/examples/tree/master/mnist.
