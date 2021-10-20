---
id: vDTgZL9UHWqYtBFdtD3vK
title: Cfm
desc: ''
updated: 1634199185974
created: 1634199122481
---
installing cfm on server mapp

Thursday 14 October 2021

See instructions here https://bitbucket.org/wishartlab/cfm-id-code/src/master/cfm/INSTALL.md


tar -zxvf RDKit_2017_09_3.tgz
cd ../..
mkdir build
cd build
cmake .. \
    -DRDK_PGSQL_STATIC=OFF\ 
    -DRDK_BUILD_PYTHON_WRAPPERS=OFF\  
    -DRDK_BUILD_CPP_TESTS=OFF\  
    -DRDK_BUILD_DESCRIPTORS3D=OFF\
        -DRDK_INSTALL_STATIC_LIBS=OFF\    
        -DRDK_INSTALL_INTREE=ON \
    -DRDK_BUILD_INCHI_SUPPORT=ON\  
    -DRDK_OPTIMIZE_NATIVE=ON  \
    -DCMAKE_CXX_STANDARD=11 \ 
    -DCMAKE_BUILD_TYPE=Release
make install



cmake .. \
    -DRDK_PGSQL_STATIC=OFF\ 
    -DRDK_BUILD_PYTHON_WRAPPERS=OFF\  
    -DRDK_BUILD_CPP_TESTS=OFF\  
    -DRDK_BUILD_DESCRIPTORS3D=OFF\
        -DRDK_INSTALL_STATIC_LIBS=OFF\    
        -DRDK_INSTALL_INTREE=OFF \
    -DRDK_BUILD_INCHI_SUPPORT=ON\  
    -DRDK_OPTIMIZE_NATIVE=ON  \
    -DCMAKE_CXX_STANDARD=11 \ 
    -DCMAKE_BUILD_TYPE=Release