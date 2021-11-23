# CenterPoint的配置
## 环境
ubuntu 18
pytorch 1.4.0
cuda 10.1
cudnn 7.5
spconv 1.0
apex 0.1
cmake 3.13.2
### 安装cmake
wget https://cmake.org/files/v3.13/cmake-3.13.2.tar.gz

tar -xzvf cmake-3.13.2.tar.gz

cd cmake-3.13.2

./bootstrap

make -j4

make install
