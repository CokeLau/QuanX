# Genshin
<img src="https://genshin-card.getloli.com/rand/287266572.png" width="800" height="400" >

#### 安装教程
1.  前提
使用iOS操作系统的手机或平板
下载[Scriptable](https://apps.apple.com/cn/app/scriptable/id1405459188)

打开后点击右上角的➕，新建一个Scripts

复制以下代码运行即可

```
llet iCloud = FileManager.iCloud()
let pathCode = iCloud.joinPath(iCloud.documentsDirectory(), "Genshin Daily.js")
let codeUrl = await new Request("https://gitee.com/peter7/genshin/raw/master/Genshin%20Daily.js").loadString()
iCloud.writeString(pathCode, codeUrl)
let n = new Notification()
n.title = "脚本下载"
n.body = "成功。"
n.sound = "default"
await n.schedule()
```

2.  获取Cookie
- PC获取
```
var cookie = document.cookie;
var Str_Num = cookie.indexOf('_MHYUUID=');
cookie = '添加 ' + cookie.substring(Str_Num);
var ask = confirm('Cookie:' + cookie);
if (ask == true) {
  copy(cookie);
  msg = cookie
} else {
  msg = 'Cancel'
}
```
复制上面全部代码，然后打开https://bbs.mihoyo.com/ys/

在页面上右键检查或者Ctrl+Shift+i

选择控制台（Console），粘贴，回车，在弹出的窗口点确认（点完自动复制）

- 手机获取

Alook、Thor、Stream
