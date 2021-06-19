# LabelFusion Docker
Base image : nvidia/cudagl:9.2-devel-ubuntu16.04
- system Ubuntu 16.04
- CUDA 9.2
- openGL
- Director
- Elasticfusion
## Usage

Building docker image
```
source build.sh
```

Enter Label Fusion
```
./docker_run.sh /path of data
```

### Director
director : [using ianchen-tw / director](https://github.com/ianchen-tw/director) 

#### Required Dependencies
The required 3rd party dependencies are:
- Qt 4.8
- VTK 5.8 or 5.10
- Python 2.7 and numpy

### Elasticfusion
elasticfusion : ![using ianchen-tw / ElasticFusion](https://github.com/peteflorence/ElasticFusion)
    - comment the CUDA_ARCH_BIN
    - add RGeForce RTX 2060 config
```
	    icpStepMap["GeForce RTX 2060"] = std::pair<int, int>(96, 112);
	    rgbStepMap["GeForce RTX 2060"] = std::pair<int, int>(112, 80);
	    rgbResMap["GeForce RTX 2060"] = std::pair<int, int>(320, 496);
	    so3StepMap["GeForce RTX 2060"] = std::pair<int, int>(128, 48);
```

#### Required Dependencies
- CMake
- OpenGL
- CUDA >= 7.0
- OpenNI2
- SuiteSparse
- Eigen
- zlib
- libjpeg
- Pangolin

