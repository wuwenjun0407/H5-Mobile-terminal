# H5移动端DPI

@(H5移动端知识)


>iPhone3手机分辨率是320*480
			iPhone4手机分辨率是640*940
			上面两款手机的宽都是320px,这就导致了屏幕大小不变，实际像素却多了一倍，这时，一个css像素就等于两个物理像素，这就是像素密度比
			window。devicePixelRatio来检测像素密度比
			为什么设计师给的设计稿一般都是640*960 750*1334

```
<style type="text/css">
				@media only screen and (device-pixel-ratio:1) {
					/*device-pixel-来检测像素密度比*/
				}
				@media only screen and (device-pixel-ratio:2) {
					/*device-pixel-来检测像素密度比*/
				}
				@media only screen and (device-pixel-ratio:3) {
					/*device-pixel-来检测像素密度比*/
				}
```