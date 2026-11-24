# data

机器可读数据。`index.html` 为了单文件可离线打开，仍内联了同一份 `WORKS / PAIRS`；这里的 JSON 是给脚本、Notebook、静态站点生成器复用的镜像。

## works.json

231 部作品，814 个 spot。顶层数组，每项：

- `id` / `title` / `year` / `form` / `typeName` / `region` / `source`
- `spots[]`

spot 关键字段：

- `id` / `name` / `city` / `province` / `lat` / `lng`
- `basis`：实拍地、剧情地、建筑原型
- `still` / `real`：作品截图、实景图 URL
- `stillSrc` / `realSrc`：来源页
- `imageMatch`：同机位 / 同建筑 / 同街区 / 原型 / 官方对照 / 待核 / 空
- `pairNote`：对照说明

## pairs.json

官方/媒体对照图的组合关系。`imgs` 里的 key 指向 `images.json`。

## images.json

对照图 URL 注册表。图片版权归原作者，仓库只存链接。

## 注意

- 坐标是地点中心点，不是拍摄机位；
- `待核` 不是已确认；
- 图片不要下载进仓库，遵守 `../sources.md`。
