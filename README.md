Optimized tensorflow builds for Windows x64.
Built on Dell XPS 15, 9560 i7-7700HQ (GPU: Nvidia 1050)

 - Main folder
	 -  Testing (This contains builds that are broken in someway)
		 - Tensorflow GPU 1.2.1, (AVX + CUDA SM30, 52, 61) broken batchnorm
	 -  Working (This contains builds that are functional)
		 - Tensorflow CPU 1.2.1 (AVX)
		 - Tensorflow GPU 1.2.1 (CUDA SM30, 52, 61)

See also [Matching SM architectures (CUDA arch and CUDA gencode) for various NVIDIA cards](http://arnon.dk/matching-sm-architectures-arch-and-gencode-for-various-nvidia-cards/)
Attempt | #1 | #2 | #3 | #4 | #5 | #6 | #7 | #8 | #9 | #10 | #11
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- |--- |---
Seconds | 301 | 283 | 290 | 286 | 289 | 285 | 287 | 287 | 272 | 276 | 269
