cc_library(dynamic_loader SRCS dynamic_loader.cc DEPS glog gflags enforce)
nv_library(dynload_cuda SRCS cublas.cc cudnn.cc curand.cc nccl.cc
        DEPS dynamic_loader)
cc_library(dynload_warpctc SRCS warpctc.cc DEPS dynamic_loader warpctc)
