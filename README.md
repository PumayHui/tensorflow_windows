# tensorflow_windows
Tensorflow with GPU and AVX options enabled for Windows 64.
Built using a Dell XPS 9560 i7-7700HQ (GPU: Nvidia 1050), taking around 3 hours.
This was built using Visual Studio 2015 against the Intel Distribution for Python 3.5.3 (2017 Update 3) and Nvidia CUDA 8.0 cuDNN 5.1.

Instructions that were followed: 

https://github.com/tensorflow/tensorflow/tree/master/tensorflow/contrib/cmake

Issue referenced: 

https://github.com/tensorflow/tensorflow/issues/9470

Time to build: 2 hours 35 minutes

Configuration:

Microsoft Windows 10

Microsoft Visual Studio Enterprise 2015 with Visual C++ 2015
Intel distribution for Python 3.5.3 - Anaconda 4.3.1 (2017 Update 3)
Git for Windows version 2.13.0
swigwin-3.0.12
NVidia CUDA Toolkit 8.0
NVidia CUDNN 5.1
CMake 3.9.0 rc3

cmake command:

cmake .. -A x64 -DCMAKE_BUILD_TYPE=Release -DSWIG_EXECUTABLE=C:/tools/swigwin-3.0.12/swig.exe -DPYTHON_EXECUTABLE=C:/IntelPython3/python.exe -DPYTHON_LIBRARIES=C:/IntelPython3/libs/python35.lib -Dtensorflow_ENABLE_GPU=ON -DCUDNN_HOME="C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\bin" -Dtensorflow_WIN_CPU_SIMD_OPTIONS=/arch:AVX

MSBuild /p:Configuration=Release tf_python_build_pip_package.vcxproj
