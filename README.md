## 自定义layer
1. 按下 SPC f j 打开 dired 目录
2. 按下按键 + , 创建 ~/.spacemacs.d 目录
3. 将光标移动到 .spacemacs 文件上, 按下 R, 将该文件移动到 .spacemacs.d 目录中
4. 进入 .spacemacs.d 目录, 将光标移动到 .spacemacs 文件上, 按下 R, 将该文件重命名为 init.el
5. 按下 qq 退出 dired
6. 重启spacemacs

## 从github下载自定义layer
```
mv ~/.spacemacs .spacemacs.bak
git clone https://github.com/stillwuyan/myspacemacs.git ~/.spacemacs.d
```
