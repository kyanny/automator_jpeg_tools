Automator JPEG Tools
====================

Automator JPEG convert tools

## Convert To JPEG

To convert any files to JPEG.

It's useful for convert screenshot PNG images to JPEG.

![Convert To JPEG.app](./convert_to_jpeg_1.gif)

![Convert To JPEG.workflow](./convert_to_jpeg_2.gif)

## Low Quality JPEG

To convert any files to JPEG with low quality.

It's useful for convert screenshot PNG images to JPEG with reduced size (expecially friendly with Qiita's upload size limit)

![Low Quality JPEG.app](./low_quality_jpeg_1.gif)

![Low Quality JPEG.workflow](./low_quality_jpeg_2.gif)

## Apps

Automator applications for drag & drop operation.

## Services

Automator services as right-click context menu in Finder.

## Scripting

Low quality convert job is by `sips` command.

```bash
for f in "$@"
do
	sips -s format jpeg -s formatOptions low --out "${f%.*}.jpg" "$f"
done
```
