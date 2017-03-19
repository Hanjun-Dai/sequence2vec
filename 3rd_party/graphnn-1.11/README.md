# graphnn

#### Prerequisites

Tested under Ubuntu 14.04 and Mac OSX 10.10.5

##### Download and install cuda from https://developer.nvidia.com/cuda-toolkit

    wget http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1404/x86_64/cuda-repo-ubuntu1404_7.5-18_amd64.deb
    sudo dpkg -i cuda-repo-ubuntu1404_7.5-18_amd64.deb
    sudo apt-get update
    sudo apt-get install cuda
    
  in .bashrc, add the following path
  
    export CUDA_HOME=/usr/local/cuda
    export LD_LIBRARY_PATH=/usr/local/cuda/lib64:$LD_LIBRARY_PATH
    export LD_LIBRARY_PATH=/usr/local/lib:$LD_LIBRARY_PATH
    
##### Download and install intel mkl

  in .bashrc, add the following path
  
    source {path_to_your_intel_root/name_of_parallel_tool_box}/bin/psxevars.sh
    export MKL_ROOT={path_to_your_intel_root}/mkl
    
##### Install fmtlib

    check https://github.com/fmtlib/fmt for help
  
#### Build static library

    modify configurations in make_common file
    make
    
#### Run example

##### Run mnist

    cd examples/mnist
    make
    ./run_exp.sh

#### Reference

```bibtex
@article{dai2016discriminative,
  title={Discriminative Embeddings of Latent Variable Models for Structured Data},
  author={Dai, Hanjun and Dai, Bo and Song, Le},
  journal={arXiv preprint arXiv:1603.05629},
  year={2016}
}
```
