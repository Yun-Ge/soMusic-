# soMusic-
在线搜索网易云，QQ音乐，酷狗，酷我，百度音乐

调用示例：
网站名字格式：网易->netease  QQ音乐->qqmusic   酷狗音乐->kugou  酷我音乐->kuwo  百度音乐->baidu
搜索：btn_play(“搜索关键字” “网站名字”);
返回正在播放音乐的链接：getSrc()
返回正在播放音乐的名字：getTitle()
返回正在播放音乐的封面图片：getPic()
返回正在播放音乐的作者名字：getAuthor()

1、需要放置jquery.js APlayer.min.js APlayer.min.css musci.js
2、放置
    <div id="aplayer"></div>

还不会，请看Demo示例

    <script src="/jquery-1.10.2.min.js" type="text/javascript"></script>
    <script src="/APlayer.min.js" type="text/javascript"></script>
    <script src="/music.js" type="text/javascript"></script>
    <link href="/APlayer.min.css"  rel="stylesheet" />

     <div>
      <input type="text" id="name" required>
      <button type="button" id="soMusic">搜索</button><br/>

      <input type="radio" name="musicWebsite" value="netease" checked /> 网易云
      <input type="radio" name="musicWebsite" value="qqmusic">QQ
      <input type="radio" name="musicWebsite" value="kugou" /> 酷狗
      <input type="radio" name="musicWebsite" value="kuwo" /> 酷我
      <input type="radio" name="musicWebsite" value="baidu" />百度
    </div>

    <div id="aplayer"></div>
    <button onclick="getSrc()">获取播放链接</button>
    <button onclick="getTitle()">获取音乐名</button>
    <button onclick="getPic()">获取封面图片链接</button>
    <button onclick="getAuthor()">获取作者名</button>
    <script>
      $("#soMusic").click(function(){
        var namevalue = $('input:radio[name="musicWebsite"]:checked').val();
        btn_play($("#name").val(), namevalue);
      })
    </script>
