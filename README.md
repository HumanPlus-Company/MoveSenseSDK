# MoveSenseSDK

MoveSenseSDK可让开发者通过USB口获取图像及IMU信息，并进行二次开发。

## Windows版

Windows版以动态链接库方式发布。

### 结构
-	**ConfigFiles**: MoveSense不同系列相机的配置文件，一般无需修改
-	**Denpendencies**: OpenCV2.4.10的依赖文件，用于Samples
-	**Documentation**: 文档，含产品手册等
-	**include**: MoveSenseSDK头文件 
-	**lib**: Windows下的库文件
	- vs2012: 使用 Visual Studio 2012 32/64 bit 编译
-	**Samples**: MoveSense相机的简单示例程序    

### 使用
示例代码参考samples文件夹，其中包含了可直接编译运行的Visual Studio工程，使用时需将对应的dll文件复制到exe所在目录或Windows系统目录。

## Linux版

Linux版以源码方式发布。

### 结构
-	**Configfiles**: MoveSense不同系列相机的配置文件，一般无需修改
-	**Denpendencies**: OpenCV2.4.10的依赖文件，用于Samples
-	**Documentation**: 文档，含产品手册等
-	**MoveSenseCamera**: MoveSenseSDK源码
-	**Samples**: MoveSense相机的简单示例程序 

### 使用 

编译需要使用cmake，安装cmake

```
sudo apt-get install cmake
```

程序另外调用的库有： libudev-dev，安装libudev-dev

```
sudo apt-get install libudev-dev
```

以上安装完成后，在发布目录下运行以下命令

```
mkdir build
cd build
cmake ..
make

cd bin
./ImageCapture
```

执行以上操作后即可看到显示的图像。
