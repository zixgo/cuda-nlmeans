# cuda-nlmeans

�Ա��˲�ͬ�ľ���ͼ��ȥ�뷽����Ч���� Non-local Means ȥ�뷽���ļ���Ч���������鿴 `article.pdf`��

## ȥ�뷽���ͼ���ƽ̨

ȥ�뷽������ֵ�˲�����˹�˲���˫���˲��ͷǾֲ���ֵ�˲���

����ƽ̨�����̣߳����߳�(OpenMP)��CUDA��

## �� Google Colab ������

ʹ�� [vcpkg](https://github.com/microsoft/vcpkg) ��˻��������У�CUDA �ǿ�ѡ������Ҫ���� CUDA ��صĴ��룬���޸� Colab ������ʱΪ**Ӳ��������-GPU**��

Google Colab �����нű���

```
# cuda-nlmeans env setup
!apt update
!apt install -y build-essential tar curl zip unzip gcc g++ gdb make cmake bison
!apt install -y autoconf libsass-dev libtool libxrandr-dev libxi-dev
!apt install -y libxcursor-dev libxinerama-dev
!git clone https://github.com/microsoft/vcpkg
!./vcpkg/bootstrap-vcpkg.sh
%cd /content/vcpkg
!./vcpkg install opencv3[contrib]:x64-linux

# cuda-nlmeans build and test
%cd /content
!git clone https://github.com/zixgo/cuda-nlmeans.git
%cd /content/cuda-nlmeans
!cmake -DCMAKE_BUILD_TYPE=Release -S. -Bout "-DCMAKE_TOOLCHAIN_FILE=/content/vcpkg/scripts/buildsystems/vcpkg.cmake"
!cmake --build out
!./cuda-nlmeans
```

## ����

����й��ڴ�������ʣ���ӭ�� issue��If any questions, an issue is welcomed.
