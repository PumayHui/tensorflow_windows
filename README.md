# tensorflow_windows
Tensorflow with GPU and AVX options enabled for Windows 64.
Built using a Dell XPS 9560 i7-7700HQ (GPU: Nvidia 1050), taking around 3 hours.
This was built using Visual Studio 2017 against the Python 3.5.3.

Instructions that were followed: 

https://github.com/tensorflow/tensorflow/tree/master/tensorflow/contrib/cmake

Issue referenced: 

https://github.com/tensorflow/tensorflow/issues/9470

Configuration:

Microsoft Windows 10

Microsoft Visual Studio 2017

Anaconda 4.3.1 (Python 3.5.3)

Git for Windows version 2.13.2

swigwin-3.0.12

NVidia CUDA Toolkit 8.0

NVidia CUDNN 5.1

CMake 3.9.0 rc5

cmake command:

For CPU:
cmake .. -G "Visual Studio 15 2017 Win64" -DCMAKE_BUILD_TYPE=Release -DSWIG_EXECUTABLE=C:/tools/swigwin-3.0.12/swig.exe -DPYTHON_EXECUTABLE=C:\Users\ALuo\Anaconda3\python.exe -DPYTHON_LIBRARIES=C:\Users\ALuo\Anaconda3\libs\python35.lib -Dtensorflow_WIN_CPU_SIMD_OPTIONS=/arch:AVX

MSBuild /p:Configuration=Release tf_python_build_pip_package.vcxproj

Working:
CPU - Compiled using VS 2017 w/ AVX support and python 3.5.3, no modifications
GPU - Compiled using VS 2015 w/o AVX support and python 3.5.3, CUDA arch is 3.0, 5.2, 6.1 (changed from 3.0, 3.5, 5.2). Using CUDA 8.0.61 and cuDNN 5.1
Testing:
GPU - Compiled using VS 2015 w/ AVX support and python 3.5.3, CUDA arch is 3.0, 5.2, 6.1, imaginary number related modifications. Currently batchnorm is failing
