Tensorflow 1.4 w/ cuDNN 7 in progress.

Optimized tensorflow builds for Windows x64.
Built on Dell XPS 15, 9560 i7-7700HQ (GPU: Nvidia 1050)

 - Main folder
	 -  Testing (This contains builds that are broken in someway)
		 - Tensorflow GPU 1.2.1 Py 3.5.3, (AVX + CUDA 5.1 SM30, 52, 61) broken batchnorm
		 - Tensorflow GPU 1.2.1, Py 3.6.2 (CUDA 5.1 SM30, 52, 61) broken batchnorm
		 - Tensorflow GPU 1.2.1, Py 3.6.2 (CUDA 6 SM30, 52, 61) broken batchnorm
		 - Tensorflow GPU 1.2.1, Py 3.6.2 (CUDA 5.1 SM30, 35, 52) broken batchnorm
	 -  Working (This contains builds that are functional)
		 - Tensorflow CPU 1.2.1 Py 3.5.3 (AVX)
		 - Tensorflow GPU 1.2.1 Py 3.5.3 (CUDA 5.1 SM30, 52, 61)

See also [Matching SM architectures (CUDA arch and CUDA gencode) for various NVIDIA cards](http://arnon.dk/matching-sm-architectures-arch-and-gencode-for-various-nvidia-cards/)

| Category | Name | Compiler | CUDA/cuDNN | AVX | Notes |
|-----------------|---------------------|------------------|-------------------|---------------|---------------|
| Testing | tensorflow_gpu-1.2.1-cp35-cp35m-win_amd64.whl | VS2015 Update 3 | 8.0.61/5.1 | Yes | SM30,52,61, Py 3.5.3 |
| Testing | tensorflow_gpu-1.2.1-cp36-cp36m-win_amd64_cuDNN5_1.whl | VS2015 Update 3 | 8.0.61.2/5.1 | No | SM30,52,61, Py 3.6.2 |
| Testing | tensorflow_gpu-1.2.1-cp36-cp36m-win_amd64_cuDNN6.whl | VS2015 Update 3 | 8.0.61.2/6.0 | No | SM30,52,61, Py 3.6.2 |
| Testing | tensorflow_gpu-1.2.1-cp36-cp36m-win_amd64.whl | VS2015 Update 3 | 8.0.61.2/5.1 | No | SM30,35,52, Py 3.6.2 |
| Working | tensorflow-1.2.1-cp35-cp35m-win_amd64.whl | VS2017 15.2 | NaN/NaN | Yes | Py 3.5.3 |
| Working | tensorflow_gpu-1.2.1-cp35-cp35m-win_amd64.whl | VS2015 Update 3 | 8.0.61/5.1 | No | SM30,52,61, Py 3.5.3|
