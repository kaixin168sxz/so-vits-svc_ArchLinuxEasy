# ArchLinux下使用So-VITS
> 2024.11.17

[bilibili视频](https://www.bilibili.com/video/BV1H24y187Ko)

## 获取音频
> 准备一段要训练的音频素材（最好1小时~2小时）
### 使用[UVR5](https://github.com/leebufan/Ultimate-Vocal-Remover?tab=readme-ov-file)移除杂音
#### 下载UVR5

1. 安装依赖

```sh
sudo pacman -Syu
sudo pacman -Sy
sudo pacman -S python-pip
sudo pacman -S --noconfirm tk
sudo pacman -S ffmpeg

sudo rm /usr/lib/python3.xx/EXTERNALLY-MANAGED
```

2. （可选，如果下一步报错使用。非常建议，防止环境混乱）使用虚拟环境

```sh
python3 -m venv .venv
source ./.venv/bin/activate
```

3. 安装依赖环境,在UVR5项目文件夹下运行

```sh
chmod +x install_packages.sh
./install_packages.sh
```

4. 启动UVR5,在UVR5项目文件夹下运行

```sh
python3 UVR.py
```

5. 将 ```UVR5模型.zip``` 解压，把三个文件夹复制到 ```UVR5文件夹\models\``` 下


#### 使用UVR5

