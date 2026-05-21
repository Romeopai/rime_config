# Used Projects

- [rime-ice](https://github.com/iDvel/rime-ice)
- [rime-japanese](https://github.com/gkovacs/rime-japanese)
- [rime-spanish](https://github.com/gkovacs/rime-spanish)
- [latex-symbols](https://github.com/wklchris/Rime-latex-symbols) # 修改适配rime-ice

# 中英文混合输入方案
- [rime-melt](https://github.com/tumuyan/rime-melt)

# Rime 定制方案
- [weasel_style.yaml](https://github.com/rime/weasel/wiki)

## 主要文件和作用

修改或添加内容对文件时，依照以下说明放置到对应文件：

- `cn_dicts/`：中文词库文件。
  - `8105`：常用汉字单字。
  - `41448`：大字表，默认不启用，主要收录生僻字。
  - `base`：核心词库，包含两字词和常用词，必须包含注音和词频。两字词必须放到这个文件中。
  - `ext`：扩展词库，必须包含注音和词频。含有多音字的词条必须放到这个文件中。
  - `tencent`：大词库。必须没有注音。词频可选。脚本会自动补充。禁止包含多音字。
- `en_dicts/*.yaml`：英文词库文件。
  - `en`：核心英文词库，收录英文词。
  - `en_ext`：扩展英文词库，收录在词典里面一般不会收录的英文词，例如网络用词，产品名称，特别缩写，标准名称。
- `en_dicts/*.txt`：中英混合词库文件，由 `others/cn_en.txt` 派生。
- `opencc/`：OpenCC 映射文件，控制 Emoji 和部分特殊词输出，由 `others/emoji-map.txt` 派生。
- `lua/`：Lua 扩展脚本，使用 `librime-lua` API。
- `others/script/`：构建、检查和测试脚本。
- `others/recipes/`：plum 配方文件。
- `*.schema.yaml`：输入方案文件，定义拼写、翻译器、过滤器和词库引用。
- `*.dict.yaml`：主词库文件，在文件头引用具体词库文件。此类文件的具体格式请参考既有文件的写法，和标准 yaml 有所不同。
- `recipe.yaml`：plum 默认配方。
- `symbols*`：控制 `v`/`V` 模式下的符号输入。
- `weasel.yaml`：小狼毫前端配置。
- `squirrel.yaml`：鼠须管前端配置。
- `default.yaml`：全局默认配置，控制启用方案和通用行为。
- `custom_phrase.txt`：全拼自定义短语。