# CenterPoint的配置
## 环境
ubuntu 18
pytorch 1.4.0
cuda 10.1
cudnn 7.5
spconv 1.0
apex 0.1
cmake 3.13.2
## 安装cmake
wget https://cmake.org/files/v3.13/cmake-3.13.2.tar.gz

tar -xzvf cmake-3.13.2.tar.gz

cd cmake-3.13.2

./bootstrap

make -j4

make install

NOTICE:cmake version must >=3.13.2

## run code

创建数据：python tools/create_data.py nuscenes_data_prep --root_path=/media/lab414/5181a349-6af4-4c01-bd8e-6f511d314bd4/NUSCENES_DATASET_ROOT --version="v1.0-trainval" --nsweeps=10

开始训练:python -m torch.distributed.launch --nproc_per_node=1 ./tools/train.py configs/nusc/pp/nusc_centerpoint_pp_02voxel_two_pfn_10sweep.py 
