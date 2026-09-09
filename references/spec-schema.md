# Guide Specification Schema

Use `scripts/build_guide.py` when a guide can be represented as ordered blocks. The script requires `python-docx`.

## Root fields

```json
{
  "title": "Required document title",
  "subtitle": "Optional subtitle",
  "subject": "Optional document metadata",
  "version": "Optional version note",
  "blocks": []
}
```

The internal notice is inserted automatically. Do not add it to `blocks`.

## Supported blocks

```json
{"type": "h1", "text": "一 主要部分"}
{"type": "h2", "text": "操作顺序"}
{"type": "h3", "text": "注意事项"}
{"type": "p", "text": "Ordinary paragraph", "indent": true}
{"type": "note", "text": "Small gray note"}
{"type": "example", "text": "Copyable example or prompt"}
{"type": "bullets", "items": ["Item one", "Item two"]}
{"type": "numbers", "items": ["Step one", "Step two"]}
{"type": "page_break"}
```

Tables use widths in centimeters. Their total should normally fit within 15.7 cm:

```json
{
  "type": "table",
  "headers": ["阶段", "主要工作", "成果"],
  "rows": [["研究启动", "建立记录", "研究计划"]],
  "widths_cm": [3.0, 7.5, 5.2],
  "font_size": 10.2,
  "center_columns": [0]
}
```

Image paths may be absolute or relative to the JSON specification file:

```json
{
  "type": "image",
  "path": "assets/step-01.png",
  "width_cm": 15.0,
  "caption": "图1 订阅信息页面",
  "description": "点击复制订阅地址。复制完成后再打开客户端导入配置。"
}
```

Keep an image description to one or two sentences. The script validates table dimensions and required fields but cannot judge factual accuracy or visual quality. Always render and inspect the output.
