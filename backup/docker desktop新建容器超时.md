**报错：**
FROM python:3
python:3: failed to resolve source metadata for docker.io/library/python:3: unexpected status from HEAD request to https://docker.nju.edu.cn/v2/library/python/manifests/3?ns=docker.io: 403 Forbidden

解决方法：

1. 打开Docker Desktop 
2. 打开 "Settings" 

<img width="1270" height="720" alt="Image" src="https://github.com/user-attachments/assets/83f0ea9d-e5bf-48d8-af12-cc1d0465bad7" />

3. 进入 "Docker Engine" 选项卡

<img width="1238" height="595" alt="Image" src="https://github.com/user-attachments/assets/bcb41908-d1ee-4153-abd1-566ed3fe7b83" />

4. 在配置文件中添加以下内容：
  "registry-mirrors": [
    "https://docker.registry.cyou/",
    "https://docker-cf.registry.cyou/",
    "https://dockercf.jsdelivr.fyi/",
    "https://docker.jsdelivr.fyi/",
    "https://dockertest.jsdelivr.fyi/",
    "https://mirror.aliyuncs.com/",
    "https://dockerproxy.com/",
    "https://mirror.baidubce.com/",
    "https://docker.m.daocloud.io/",
    "https://docker.nju.edu.cn/",
    "https://docker.mirrors.sjtug.sjtu.edu.cn/",
    "https://docker.mirrors.ustc.edu.cn/",
    "https://mirror.iscas.ac.cn/",
    "https://docker.rainbond.cc/",
    "https://jq794zz5.mirror.aliyuncs.com"
  ]
5.点击 "Apply & Restart"