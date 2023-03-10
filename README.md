# stable-diffusion-webui-localization-zh

自用插件，fork自[liggest/stable-diffusion-webui-localization](https://github.com/liggest/stable-diffusion-webui-localization)，添加了[journey-ad的翻译](https://gist.github.com/journey-ad/d98ed173321658be6e51f752d6e6163c)到文本列表

~~删掉了自己写的机翻~~

特别感谢以上仓库的贡献者

### 用法

- 切换到WebUI的 `Extensions` 标签页，选择`Install from URL`


- 在`URL for extension's git repository`里输入以下链接：

  `https://github.com/xiaoxing1748/stable-diffusion-webui-localization-zh`

- 点击**Install**后刷新页面


- 切换到`setting(设置)-User interface(用户界面)`，在底部`Localization`栏选择`I18N_sd-webui-zh_CN.json`


- 滚动到上方点击`Apply settings`并点击`Reload UI`即可完成语言切换


### 小tips

在设置-用户界面-快捷设置列表里可以添加`sd_model_checkpoint,sd_vae`两个字段方便快捷切换模型和VAE

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
