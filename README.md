Optimized tensorflow builds for Windows x64.
Built on Dell XPS 15, 9560 i7-7700HQ (GPU: Nvidia 1050)

 - Main folder
	 -  Testing (This contains builds that are broken in someway)
		 - Tensorflow GPU 1.2.1, (AVX + CUDA SM30, 52, 61) broken batchnorm
	 -  Working (This contains builds that are functional)
		 - Tensorflow CPU 1.2.1 (AVX)
		 - Tensorflow GPU 1.2.1 (CUDA SM30, 52, 61)

See also [Matching SM architectures (CUDA arch and CUDA gencode) for various NVIDIA cards](http://arnon.dk/matching-sm-architectures-arch-and-gencode-for-various-nvidia-cards/)

| **`Linux CPU`** | **`Linux GPU`** | **`Mac OS CPU`** | **`Windows CPU`** | **`Android`** |
|-----------------|---------------------|------------------|-------------------|---------------|
| [![Build Status](https://ci.tensorflow.org/buildStatus/icon?job=tensorflow-master-cpu)](https://ci.tensorflow.org/job/tensorflow-master-cpu) | [![Build Status](https://ci.tensorflow.org/buildStatus/icon?job=tensorflow-master-linux-gpu)](https://ci.tensorflow.org/job/tensorflow-master-linux-gpu) | [![Build Status](https://ci.tensorflow.org/buildStatus/icon?job=tensorflow-master-mac)](https://ci.tensorflow.org/job/tensorflow-master-mac) | [![Build Status](https://ci.tensorflow.org/buildStatus/icon?job=tensorflow-master-win-cmake-py)](https://ci.tensorflow.org/job/tensorflow-master-win-cmake-py) | [![Build Status](https://ci.tensorflow.org/buildStatus/icon?job=tensorflow-master-android)](https://ci.tensorflow.org/job/tensorflow-master-android) |
