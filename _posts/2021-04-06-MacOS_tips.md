---
layout:     post                    # 使用的布局(不需要改)
title:      macOS小技巧             # 标题
subtitle:   我是一只被禁足的安小鸟 #副标题
date:       2020-04-06 00:00:00 GMT+0800             # 时间
author:     Zen                 # 作者
header-img: img/photo/birdAngle.webp    #这篇文章标题背景图片
catalog: False                     # 是否归档
tags:                               #标签
    - macOS
---

# 批量删除macOS读取外部驱动器产生的4k挂载点文件
`find ./ -size 4k -exec rm -f {} \;`
# 批量删除macOS自动建立的`.DS_Store`文件
`find ./ -name ".DS_Store" -depth -exec rm {} \;`
# 查找并显示文件
`find ./ -name '*.txt' -print`
# 查找指定范围文件
`find . -type f -mtime -1 -size +100k`
# 查找空文件
`find -type d -empty`