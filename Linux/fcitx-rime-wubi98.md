参考链接：

[原文](https://arzx.org/posts/2019-12-27-rime-%E4%BA%94%E7%AC%94-98-%E9%85%8D%E7%BD%AE%E6%8C%87%E5%8D%97.html)

[第一个 repo](https://github.com/arzyu/rime-wubi98)

[第二个 repo](https://github.com/rime/rime-pinyin-simp)

[符号输入](https://github.com/rime/rime-prelude)

在 rime 的配置文件夹里面创建 `default.custom.yaml`，内容如下：

```yaml
patch:
  schema_list:
    - schema: wubi98 # 我们只用 wubi98 这一个输入方案

  switcher/caption: 〔方案选单〕
  switcher/hotkeys: # 默认配置占用了较多的热键，这里只用一个
    - Control+Shift+space

  ascii_composer/switch_key:
    Shift_L: commit_code # 按左 shift 直接上屏已输入内容

  # 按键绑定
  key_binder:
    bindings:
      - { when: always, toggle: full_shape, accept: "Shift+space" } # [shift+空格] 切换全半角
      - { when: always, toggle: ascii_punct, accept: "Control+period" } # [ctrl+.] 切换中英文标点
      - { when: composing, send: Shift+Delete, accept: "Control+d" } # [ctrl+d] 删除自造词
      - { when: composing, send: Page_Up, accept: "Control+p" } # 翻页
      - { when: composing, send: Page_Down, accept: "Control+n" }
      - { when: composing, send: Up, accept: "Control+k" } # 切换选中候选词
      - { when: composing, send: Down, accept: "Control+j" }
```

再添加 `wubi98.custom.yaml` 来输入各种特殊字符，内容如下：

```yaml
patch:
  "punctuator/import_preset": symbols
  "recognizer/patterns/punct": "^/([A-Z|a-z]*|[0-9]|10)$"
```
