# 韩沁彤 · 作品集导入包

这个文件夹已经整理成可直接部署的 GitHub Pages 结构。所有作品数据和四季建模都在里面。

## 一、完整网站（推荐）

把下面这些内容上传到 GitHub 仓库根目录：

```text
index.html
project/
web-project/
audio/
```

- `index.html`：整站单文件版（柜子 + 四季 3D + 项目弹窗，全部 r128 全局 CDN，没有 ES Module）
- `project/`：互动编程的视频、作品说明、代码、Word 原文件和文档图片
- `web-project/`：网络媒体设计的视频、封面、四张 UI 展板
- `audio/`：网站点击音效

**不需要**再上传 `styles.css`、`script.js` 或 `scene-gallery/`；这些已经内联在 `index.html` 中。

## 二、只要四季 3D 页面

把 `four-seasons-gallery-r128.html` 改名为 `index.html` 单独上传即可。

它包含：

- 四季展厅
- 春 · 桃花源
- 夏 · 荷风榭
- 秋 · 稻香渡
- 冬 · 上元雪
- 四个季节的完整 THREE r128 全局场景代码

## 三、四季完整建模源码

在 `source/four-seasons/`：

| 文件 | 说明 |
| --- | --- |
| `spring-scene.js` | 春季场景源码 |
| `summer-scene.js` | 夏季场景源码 |
| `autumn-scene.js` | 秋季场景源码 |
| `winter-scene.js` | 冬季场景源码 |
| `four-seasons-gallery.html` | 模块化展厅原始页面 |
| `four-seasons-gallery-standalone.html` | 内联 Three.js 的完整展厅 |
| `four-seasons-3d.bundle.js` | 四季共享运行时 bundle |
| `build-four-seasons-3d.mjs` | 构建脚本 |
| `build-gallery-standalone.mjs` | 展厅打包脚本 |
| `four-seasons-gallery-complete.zip` | 完整源码 + Three.js vendor + 预览图 |

如果后续要继续修改建模，优先解压 `four-seasons-gallery-complete.zip`，里面有 `taohuayuan-source/vendor/` 的完整 Three.js 依赖。

## 四、作品数据索引

`works-manifest.json` 是作品/资源的清单，方便你后续继续导入或改版；网页实际显示并不依赖它。

## 五、部署注意

1. GitHub Pages 默认读取根目录的 `index.html`。
2. `project/`、`web-project/`、`audio/` 必须和 `index.html` 在同一层。
3. 如果仓库里还保留旧的 `index.html`，要先用本包的 `index.html` 覆盖它。
4. 只用整站版时，`four-seasons-gallery-r128.html` 和 `source/` 可以不上传。
