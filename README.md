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

## 使用国内ELPA镜像
[ELPA 镜像](http://elpa.emacs-china.org/)

## Emacs在Linux终端下BACKSPACE键被改成了C-h
[解决办法](https://www.cnblogs.com/arielyuan/p/9230185.html)
在`~/.spacemacs`文件的`dotspacemacs/user-config`中添加：
```
(global-set-key "\C-h" 'backward-delete-char-untabify)
```

## Windows下重定向emacs home路径
1. 创建`C:\Users\Username\AppData\Roaming\emacs.d\init.el`文件
2. 在文件中添加如下内容：
   ```
   ;; Place this file in C:\Users\Username\AppData\Roaming\emacs.d\init.el and point to the appropriate files
   (setq user-init-file "<user defined home path>/emacs.d/init.el")
   (setq user-emacs-directory "<user defined home path>/emacs.d/")
   (setq default-directory "<user defined workspace path>")
   (setenv "HOME" "<user defined path>")
   (load user-init-file)
   ```
