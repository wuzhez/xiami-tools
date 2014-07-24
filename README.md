虾米工具包
============

* `Xiami.get_stared_song(self, uid=None)` 返回某用户所有收藏曲目列表, uid不写默认为登录用户. (测试速度过快会被ban, 一页等待1s)
* `Xiami.get_stared_collection(self, uid=None)` 返回某用户所有收藏精选集列表, uid不写默认为登录用户.
* `Xiami.get_stared_collection(self, uid=None)` 返回某用户所有收藏专集列表, uid不写默认为登录用户.
* `Xiami.set_320k()` 设置当前用户默认下载曲目为高音质
* `Xiami.download_song(self, song_id)` 返回编号为 *song_id* 的曲目的相关信息和下载地址, 详细返回请看范例
* `Xiami.download_album(self, album_id)` 返回编号为 *album_id* 的专辑的相关信息和专辑内曲目下载地址, 详细返回请看范例
* `Xiami.download_playlist(self, col_id)` 同上
* `Xiami.star_song(self, songid)` 收藏曲目编号为 *songid* 的歌曲

#### 范例

```python
xiami = Xiami('username', 'password')
print xiami.download_song(1773330029)

{'url': u'http://m5.file.xiami.com/566/58566/1004526490/1773330029_15326599_l.mp3?auth_key=xxx', 'header': {'Referer': 'http://img.xiami.com/static/swf/seiya/player.swf?v=1394535902294', 'User-Agent': 'Mozilla/5.0'}, 'cookies': {'member_auth': 'xxx', '_unsign_token': 'xxx', '__XIAMI_SESSID': 'xxx', 'user': 'xxx', '_xiamitoken': '88c977565b6f57d85833b488a43ac31c'}, 'data': [{'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'260', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Decision', 'album_id': u'204202267', 'id': 1773330029}]}
```

```python
xiami = Xiami('username', 'password')
print xiami.download_song(1773330029)

{'url': u'http://m5.file.xiami.com/566/58566/204202267/1773320969_15316507_l.mp3?auth_key=89334aa199686bda6ac580a04fac93da-1406332800-0-null', 'header': {'Referer': 'http://img.xiami.com/static/swf/seiya/player.swf?v=1394535902294', 'User-Agent': 'Mozilla/5.0'}, 'cookies': {'member_auth': '2W6bT45I621jiqifSIhiIC0f5O3VGGCFlo4Fj7Ev5VFwcdtaYYX%2FkauSRAJO2iKWrmFDReHNgWo', '_unsign_token': 'ea28d2a560b6ea779595ac8ebff850d3', '__XIAMI_SESSID': '250f587a94044259f53faa1c82580294', 'user': '36962256%22lalala%22%222%22680%22%3Ca+href%3D%27%2Fwebsitehelp%23help9_3%27+%3Efa%3C%2Fa%3E%220%220%221597%223bba224459%221406222184', '_xiamitoken': 'fff5782f2874e8cd3fbcc6cd4ab913eb'}, 'data': [{'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'260', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Decision', 'album_id': u'204202267', 'id': u'1773330029'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'126', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Best Thing That Ever Happened', 'album_id': u'204202267', 'id': u'1773330030'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'306', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'I&#039;m an Autobot', 'album_id': u'204202267', 'id': u'1773330031'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'137', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Optimus Is Alive', 'album_id': u'204202267', 'id': u'1773330032'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'353', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Cemetery Wind', 'album_id': u'204202267', 'id': u'1773330033'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'317', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'His Name Is Shane and He Drives', 'album_id': u'204202267', 'id': u'1773330034'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'125', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Hacking the Drone', 'album_id': u'204202267', 'id': u'1773330035'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'204', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Transformium', 'album_id': u'204202267', 'id': u'1773330036'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'116', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Galvatron Is Online', 'album_id': u'204202267', 'id': u'1773330037'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'206', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Your Creators Want You Back', 'album_id': u'204202267', 'id': u'1773330038'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'247', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'The Final Knight', 'album_id': u'204202267', 'id': u'1773330039'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'132', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Punch Hold Slide Repeat', 'album_id': u'204202267', 'id': u'1773330040'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'171', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'The Presence of Megatron', 'album_id': u'204202267', 'id': u'1773330041'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'254', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Galvatron Is Active', 'album_id': u'204202267', 'id': u'1773330042'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'89', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Have Faith Prime', 'album_id': u'204202267', 'id': u'1773330043'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'103', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Hong Kong Chase', 'album_id': u'204202267', 'id': u'1773330044'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'76', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'The Legend Exists', 'album_id': u'204202267', 'id': u'1773330045'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'397', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Dinobot Charge', 'album_id': u'204202267', 'id': u'1773330046'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'171', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'That&#039;s a Big Magnet', 'album_id': u'204202267', 'id': u'1773330047'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'125', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Drive Backwards', 'album_id': u'204202267', 'id': u'1773330048'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'318', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': u'http://img.xiami.net/lyric/49/1773330049_14053219446364.txt', 'title': u'Honor to the End', 'album_id': u'204202267', 'id': u'1773330049'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'227', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'Leave Planet Earth Alone', 'album_id': u'204202267', 'id': u'1773330050'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'201', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': None, 'title': u'The Knight Ship', 'album_id': u'204202267', 'id': u'1773330051'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'357', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': u'http://img.xiami.net/lyric/66/1773320966_14044862092251.lrc', 'title': u'Hunted', 'album_id': u'204202267', 'id': u'1773320966'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'345', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': u'http://img.xiami.net/lyric/67/1773320967_14044862169970.lrc', 'title': u'Tessa', 'album_id': u'204202267', 'id': u'1773320967'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'177', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': u'http://img.xiami.net/lyric/68/1773320968_14044862276405.lrc', 'title': u'Autobots Reunite', 'album_id': u'204202267', 'id': u'1773320968'}, {'artist': u'Steve Jablonsky', 'album_pic': u'http://img.xiami.net/images/album/img66/58566/2042022671404550070.jpg', 'length': u'294', 'album_name': u'Transformers: Age of Extinction (Music from the Motion Picture)', 'lyric': u'http://img.xiami.net/lyric/69/1773320969_14044862358934.lrc', 'title': u'Lockdown', 'album_id': u'204202267', 'id': u'1773320969'}]}
```

一些其他好玩的组合
============
* 转移用户收藏数据
