# stable-diffusion-webui-localization-zh

fork自[liggest/stable-diffusion-webui-localization](https://github.com/liggest/stable-diffusion-webui-localization)，添加了部分翻译（机翻），修改了小部分翻译。

与[官方翻译](https://github.com/dtlnor/stable-diffusion-webui-localization-zh_CN)稍有区别

特别感谢以上两个仓库的贡献者

### 用法

转到WebUI的 `Extensions` 标签页，选择`Install from URL`

在URL for extension's git repository里输入以下链接

```
https://github.com/xiaoxing1748/stable-diffusion-webui-localization-zh
```

点击**Install**

### 额外内容

在 [a1111-sd-webui-tagcomplete](https://github.com/DominikDoom/a1111-sd-webui-tagcomplete) 的加持下，WebUI 可以有 prompt 补全功能

它提供了一个 tag 众多的 `danbooru.csv` 文件，也可以为这个文件增加翻译

这里试着用网络上搜集来的 tag 翻译填补了极少一部分，还有大量 tag 是处于未翻译状态

要启用翻译，以扩展的形式安装好 tagcomplete 即可

可能有用的脚本：

- `get_untranslated.py` 
  
  找出目前尚未翻译的 tag，生成 `danbooru-untranslated.csv`
- `collect_tags.py` 
  
  通过提供 tag-翻译 对照文件，填充 `danbooru-zh.csv`
  
  （tag-翻译 对照文件即每行为 `tag分隔符翻译` 的文本文件）
- `merge_tags.py`
  
  合并提供的 tag-翻译 对照文件与 `danbooru-zh.csv` 中翻译不同的 tag，手动决定哪个翻译更好

- `merge_collect_tags.py`
  
  类似于同时做 `merge_tags.py` 和 `collect_tags.py`

> - [TagTable](https://github.com/zcyzcy88/TagTable)
> - [魔咒百科词典](https://aitag.top/)
> - [阿巧的 tag 翻译贴](https://ngabbs.com/read.php?tid=33869519)
