#  一个学习 ffmpeg 命令行的例子
`An example of ffmpeg`

## 断点调试，ffmpeg 命令行直接编译进项目中

## 使用说明

想必大家都行学习一下大名鼎鼎的 ffmpeg 命令行工具，了解 ffmpeg 命令行是如何运行的，甚至想像调试 iOS 和 Android 程序那样调试 ffmpeg，增加断点等等，该项目为 macOS 的项目，通过 Xcode 进行 ffmpeg 命令行，随意调试

## 编译

### 方法一
`该例子没有直接从源码级别编译 ffmpeg`，需要先编译 ffmpeg 命令行的依赖库（该项目在 ffmpeg-5.1.1 测试通过）
brew install ffmpeg


### 方法二

也可以直接编译项目中的 ffmpeg-5.1.1，编译完成后需要修改Xcode 的 Other Link Flags, Header Search Paths, Library Search Paths，参考项目修改即可 

./configure --prefix=/usr/local
make -j8
make install


## RUN

直接修改 main.m 中的 command 命令行参数即可运行，开始你的学习和调试之旅吧

```c
    char command[] = "ffmpeg -i     input.mp4  -c  copy output.mp4";
```
