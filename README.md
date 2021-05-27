# 哈尔滨工业大学（深圳）中期答辩 LaTex 模板

本模板根据 [2019 级中期答辩通知](http://www.hitsz.edu.cn/article/view/id-112449.html) 制作, 由 [hithesis v3](https://github.com/dustincys/hithesis) 改进而来, 以适应新的格式要求, 感谢原作者的贡献. 理论上本模板也适用于开题报告, 但是没有严格核对开题格式, 如需用于开题, 请自行确认格式, 如有问题欢迎提 issue.

## 使用方法

编译流程已经写到 `latexmk` 文件中, 使用时只需要 使用 `latexmk` 命令便可自动编译. 编译文件生成在 `build` 文件夹中, `build` 文件夹里边需要保持和外面有 `.tex` 文件的文件夹相同的结构. 既需要类似于如下的文件结构:

``` text
.\中期检查\中期报告TEX
├─.vscode
├─back # 正文后面的部分
├─body # 正文部分
├─build # 编译输出文件夹
│  ├─back
│  ├─body
│  └─front
├─figures # 插图
├─front # 正文前面的部分
└─logos # 学校的logo
```

以下提供 TexStudio 和 VsCode 的配置方式, 其他 IDE 或编辑器同理.

### TexStudio 配置

TexStudio 配置如下图, 请将原本的配置截图保持, 以免编译其他文件是需要改回设置.
![Alt text](github_images/texstudio设置.png?raw=true "Title")

### VsCode 配置

Vscode需要在工作目录下创建 .vscode/setting.json 文件, 填入以下工作区设置, 而后使用 `latexmk` 编译文档.

``` Json
{
    "latex-workshop.latex.recipes": [
        {
            "name": "latexmk",
            "tools": [
                "latexmk"
            ]
        },
    ],
    "latex-workshop.latex.tools": [
        {
            "name": "latexmk",
            "command": "latexmk",
            "args": [
                "%DOCFILE%"
            ]
        },
    ],
    "latex-workshop.latex.outDir": "%DIR%/build",
}
```

## 模板预览

![Alt text](github_images/report_页面_1.png?raw=true "Title")
![Alt text](github_images/report_页面_2.png?raw=true "Title")
![Alt text](github_images/report_页面_3.png?raw=true "Title")
![Alt text](github_images/report_页面_4.png?raw=true "Title")
![Alt text](github_images/report_页面_5.png?raw=true "Title")
![Alt text](github_images/report_页面_6.png?raw=true "Title")
![Alt text](github_images/report_页面_7.png?raw=true "Title")
