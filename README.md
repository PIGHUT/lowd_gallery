# 深水城领主卡牌图鉴

这是一个静态版《深水城领主》卡牌图鉴，面向 Vercel 部署整理。

## 内容

- `index.html`：可直接打开的静态图鉴页面
- `assets/`：界面与资源图标、卡图素材
- `waterdeep_cards_gallery.json`：部署可用的卡牌数据快照
- `waterdeep_cards_gallery.csv`：表格数据快照

## 本地预览

```bash
python3 -m http.server 4173
```

然后打开 `http://127.0.0.1:4173/`。

## 重新构建

在本目录的上级工作目录运行：

```bash
python3 tools/export_waterdeep_gallery.py
python3 tools/build_lowd_gallery_static.py
```

`build_lowd_gallery_static.py` 会把本地解包卡图复制成 `assets/cards/` 下的相对路径，保证 Vercel 部署后可以正常显示。
