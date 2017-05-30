TP5_Splider
===============



基于Thinkphp5 和X 易新闻 完善整理的新闻API接口

 + 新闻分类接口
 + 视频分类接口
 + 图片接口
 + 段子笑话接口
 + 重构的模型和数据库类
·

> ThinkPHP5的运行环境要求PHP5.4以上。


## 1. 新闻模块

说明: 包括 新闻模块banner轮播图接口、新闻分类列表分类接口、新闻详情接口、本地新闻接口 如下详情：

### 1.1 新闻轮播图接口

   **必选参数:**
   无
   **接口地址:**
   `News/banner`

   **调用例子:**
   `http://localhost:8050/index.php/index/News/banner`

   返回数据(每次返回是10条数据,这里就不全部列出来了)如下图:

### 1.2 新闻分类列表分类接口

   **必选参数:**
   `type` int : 新闻类型

   <table>
   <tr>
    <td>type</td>
    <td>0</td>
    <td>1</td>
    <td>2</td>
    <td>3</td>
    <td>4</td>
     <td>5</td>
     <td>6</td>
     <td>7</td>
   </tr>
   <tr>
    <td>名称</td>
    <td>头条</td>
    <td>军事</td>
    <td>娱乐</td>
    <td>体育</td>
    <td>科技</td>
    <td>艺术</td>
     <td>教育</td>
     <td>要闻</td>
   </tr>
   </table>

  `page` int : 分页页数,每页返回10条

   **接口地址:**
   `/News/new_list?type=1&page=20`

   **调用例子:**
   `http://localhost:8050/index.php/index/News/new_list?type=1&page=20`

   返回数据(每次返回是10条数据,这里就不全部列出来了)如下图:


  

### 1.3 新闻详情接口

  **必选参数:**
    `postid` 新闻列表下的 postid

  **接口地址:**
  `/index.php/index/News/new_detail?postid=CLJN5K2M000181KT`

  **调用例子:**
  `http://localhost:8050/index.php/index/News/new_detail?postid=CLJN5K2M000181KT`

  返回数据(每次返回是10条数据,这里就不全部列出来了)如下图:
```javascript
{
    "msg": "success",
    "code": 1,
    "data": {
        "body": "<!--IMG#0--><p>　　毛泽东同志在《论持久战》一文中指出，日本的军力在东方是一等的。抗战中，真实的侵华日军并非像某些影视作品中所描述的那样不堪一击，而是十分凶狠猖狂、具有很强战斗力。为了战胜这只军国主义怪兽，中国军民进行了长达14年的生死搏斗才赢得战争胜利。中国人民抗日战争可以说是异常惨烈，这是为什么呢？这又能给今天的我们以什么样启示呢？</p><p>　　<strong>为什么抗日战争异常惨烈？</strong></p><p>　　<strong>——侵华日军作战能力分析及启示</strong></p><p>　　■王晓辉 李雨樵</p><p>　　毛泽东同志在《论持久战》一文中指出，日本的军力在东方是一等的。抗战中，真实的侵华日军并非像某些影视作品中所描述的那样不堪一击，而是十分凶狠猖狂、具有很强战斗力。为了战胜这只军国主义怪兽，中国军民进行了长达14年的生死搏斗才赢得战争胜利。中国人民抗日战争可以说是异常惨烈，这是为什么呢？这又能给今天的我们以什么样启示呢？</p><p>　　<strong>部队结构合成，具备了协同作战能力</strong></p><p>　　日本发动侵华战争时已经完成了工业化，其军队在组织结构和武器装备上已经初步完成机械化。日本陆军是侵华的主力，师团是其具有确定编制的第一级作战单位，一般由步兵、炮兵、骑兵、工兵和辎重部队等混合编成。其中，除步兵外，炮兵、骑兵、工兵等兵种也属于直接作战力量，其数量几乎占了师团编成内联队数量的一半。因此，一支现代陆军所要求的火力、突击力、机动力与保障力等，日军师团一个也不缺。故日军的陆、海、空军既能联手打大战，单个陆军师团也敢孤军突入，与数倍于己的对手独立作战。如淞沪会战与武汉会战，是日军侵华的两次大规模陆、海、空三军联合作战。日军两度获胜，反映出其三军协同作战的能力，这是当时中国军队所不及的；也反映出当时中国军队的落后，是一种结构性的整体性的落后。</p><p>　　<strong>结构决定功能，体系决定战斗力。军队结构落后于时代、落后于战争形态和作战方式发展，必然丧失军事竞争主动权。可以说，在未来战场上，谁的结构更利于集聚潜能、释放效能，谁的结构更符合制胜机理、打赢要求，谁就能占据优势、赢得先机。</strong></p><p>　　<strong>武器装备精良，形成了联合火力杀伤</strong></p><p>　　抗战期间，中日两军在武器装备质量数量方面存在着很大的差距。以侵华日军一个常设师团（即甲种师团）与中国精锐的陆军第88师（德械师）相比，两军装备的各种枪炮在性能上互有优长，但在数量上却拉开了差距：日军步枪数量是中国军队的1.6倍多，轻重机枪是2倍多，野战重炮是4倍多。在密集火力与重火力杀伤等方面，日本陆军对中国陆军构成了成倍的数量优势。此外，日本陆军作战还可以得到相当数量的空中火力支援以及坦克装甲部队的加强，可构筑一张陆、海、空三军联合火力网。如淞沪会战，是抗战中中日两军精锐部队首次硬碰硬的较量，也是中国军队牺牲最大、战斗最为惨烈的一役。中国军队进攻时，就会陷入日军的立体火力网；防御时，又会饱受日军的火力轰击，兵员损失达到一天一个师的惨烈程度。因此，面对侵华日军的立体火力网，中国军队只能凭借数量优势，以人海填火海，极为悲壮。</p><p>　　<strong>武器装备是构成战斗力最直接的物质基础。武器装备落后，人的能动作用在战争中也很难最大限度地发挥出来，要打赢战争就会付出更大的代价。因此，要赢得胜利既要敢于亮剑，又要善于铸剑，加快构建适应未来战争和履行使命要求的武器装备体系。</strong></p><p>　　<strong>作战组织严密，使得攻防转换比较灵活</strong></p><p>　　侵华日军作战组织与实施严密，使其火力杀伤更加精准、高效，因此总能掌控战场主动权。比如日军在淞沪会战时，首先，通过观测气球侦察中国军队阵地，标定攻击目标，然后召唤飞机、野战重炮与海军舰炮进行狂轰滥炸，尽量摧毁中国军队阵地。其次，待其陆、海、空火力突击后，日军便出动坦克掩护步兵，向中国军队阵地发起猛攻；与此同时，其炮兵火力实施延伸射击，对中国军队后方增援部队进行火力拦阻，力求大量杀伤有生力量。再次，如遭遇中国军队强力还击，日军即再次召唤火力轰击，然后再进行新一波步、坦协同攻击。此外，日本战机以组、队形式，在战场上空巡视，发现中国军队目标即进行轰炸与扫射，或召唤野战重炮与舰炮进行远程轰击。由于侵华日军在作战组织与实施上的严密性，使其无论在大兵团联合作战中，还是小股部队攻防战斗中，都能够做到军种间行动联合，步、坦、炮间火力协同，左右邻间相互配合，发挥出整体战力来。而正面战场中国军队在指挥上鲜有灵活创举，基本上处于见招拆招的被动地位。</p><p>　　<strong>战争对抗不仅是力量的对抗，而是综合较量。作战指挥，不是简单照条文操作或单纯计算就能解决的，面对战争复杂性的增加，单纯的技术或者单纯的谋略，都不可能掌控战场的主动权。而是应该谋力并举，既要讲指导的艺术，又要注重实力，二者相互支撑、不可偏废。</strong></p><p>　　<strong>军事训练严苛，保证了人员较高作战素养</strong></p><p>　　日军严苛的军事训练是其作战素养较高的主要原因。日军的训练可分为军官和士兵两部分，具有训练层次科学、训练课目覆盖面大、训练要求严格的特点。通过陆军士官学校文理兼顾的各兵种专业课程训练和后期各类技术兵种军官学校再教育，使得日军能够培养出一支高质量的基层军官队伍，且便于各兵种间的沟通和配合。士兵依照《步兵操典》组织常规单兵综合素质训练和中队以上的协同作战训练以及两个月的大队、联队级作战协同训练。而且日军新兵在转入小队、中队级协同战术训练时，往往会被老兵们带着加练夜间100米精确射击、避弹奔跑及针对避弹奔跑的射击方法、狙击与反狙击术、突发情况下防守与反击的动作等额外的训练课目，这些都是在战场上非常实用的技术。相比之下，当时中国军队则面临着军官受教育层次低、训练体系不完整、训练经费欠缺、训练装备差等问题。因缺少科学系统的训练，中国军队手中少量精良武器装备在战场上常常不能充分发挥应有作用。</p><p>　　<strong>军事训练是未来战争的预演。坚持军事训练是和平时期军队战斗力生成的基本途径。打仗硬碰硬，训练必须实打实。军事训练水平上不去，部队战斗力也很难提高，战时必然吃大亏。所以，要想赢得未来战争，必须通过严酷的实战化训练这块“磨刀石”，把打赢本领锤炼得更过硬。</strong></p><p>　　<strong>情报工作缜密，获得了事半功倍的作战效果</strong></p><p>　　自明治维新以来，日军在对外扩张战争中，屡屡尝到情报工作带来的甜头，故其视情报侦察为战争制胜的捷径，始终高度重视情报侦察工作。日本发动侵华战争前的数十年间，在中国加紧了对未来预定战场的情报侦察。如据日本防卫厅战史研究所编写的《大本营陆军部》记载，1923年日军就制订了对中国的作战计划设想要点。根据此要点，1925年，日军参谋本部作战科长畑俊六率参谋本部、陆军省、海军军令部作战科等一行人员，乘军舰用一个月的时间，对上海至汉口的登陆点逐段进行侦察，这为以后日军进攻淞沪、武汉等要地，摸清兵要地志情况做好了准备。九一八事变后，日军更是通过各种途径、运用各种手段进行情报侦察，可以说无孔不入、用尽其力。比如当时中国军用地图的兵要地志却没有日军地图标注得清晰完备。</p><p>　　<strong>“知彼知己，百战不殆”。情报工作的优劣、得失与高下，对于战争决策、作战部署乃至最后的战争胜负，起到极为重要的作用。通过缜密细致长期的情报工作，找出对手要害，针对性地设计战法，就能达到“四两拨千斤”的作战效果。</strong></p><p>　　<strong>思想控制严密，部队具有畸形的战斗意志</strong></p><p>　　抗战初期，侵华日军士兵普遍表现“不怕死”，这与长期日本武士道的文化贻害有关，但是更大程度上还是因为受到了军国主义思想的毒害。日本在近代走上武力扩张的道路之后，非常重视向军人灌输“效忠天皇”的封建忠君思想，同时日本还开展反华灭华教育；将侵略战争说成是为了解决日本“人口过剩”问题，捍卫日本的“生命线”“主权线”等。日军士兵长期受到军国主义思想的毒害，形成畸形的死战不降的战斗意志。在战局陷入僵持后，日军往往会组织自杀式的死亡冲锋。二战末期，美国最终决定先向日本投掷原子弹，而不是直接登陆日本。一个很重要的原因，就是美国惮于日本在本土进行“玉碎”作战，将会给美军带来巨大人员伤亡。与日军不同，中国军民的抵抗意志和战斗精神是在民族危亡中激发出来的，具有自发性、深刻性和持久性、正义性，这也是我们最终取得抗战胜利的重要原因。</p><p>　　<strong>战斗意志是军队战斗力的重要构成。今天，培育军人的战斗意志，必须以过硬的军事技术和丰富的科技知识作基础。要把战斗意志培育融入军事训练内容体系，渗入各项军事实践活动，紧紧围绕担负的作战任务，练胆量、练意志、练作风、练技术战术，保证战斗意志和军事素质同步提升。</strong></p><p>　　<strong>编后感言：</strong></p><p>　　<strong>以敌为鉴是赢得胜利的重要方式</strong></p><p>　　面对侵华日军这部高效运转的战争机器，这头人类历史上武装到牙齿的法西斯主义怪兽，中国军民不屈不挠、奋起抵抗，使侵略者陷入人民战争的汪洋大海。侵华日军是“很难打”，但绝非“不可战胜”。特别是到了战争中后期，随着日本战争潜力的枯竭、士兵反战情绪的蔓延，侵华日军的战斗力迅速衰落，已难逃失败投降的结局。历史已经雄辩地证明，正义必胜、和平必胜、人民必胜。因此，作为战胜者，承认敌人的强悍不需要什么勇气，但需要秉持正确认知态度。以敌为鉴为我所用，是胜者恒强的重要手段，也是赢得胜利的方式。随意消费血与火的历史，是对历史的不尊重，更是对未来的不负责任。</p><p>原标题：为何抗日战争异常惨烈？日军并非神剧不堪一击</p>",
        "ydbaike": [],
        "replyCount": 86,
        "link": [],
        "img": [
            {
                "ref": "<!--IMG#0-->",
                "pixel": "600*399",
                "alt": "",
                "src": "http://cms-bucket.nosdn.127.net/catchpic/5/5a/5a67d106dd715cc465c97092d71b197b.jpg"
            }
        ],
        "votes": [],
        "shareLink": "https://c.m.163.com/news/a/CLJN5K2M000181KT.html?spss=newsapp&spsw=1",
        "digest": "",
        "topiclist_news": [
            {
                "hasCover": false,
                "subnum": "超过1000万",
                "alias": "Military",
                "tname": "军事",
                "ename": "junshi",
                "tid": "T1348648141035",
                "cid": "C1348647991705"
            }
        ],
        "dkeys": "日军,中国军队,侵华日军,淞沪会战",
        "ec": "李曦_NN2587",
        "topiclist": [
            {
                "hasCover": false,
                "subnum": "181.4万",
                "alias": "网易军事频道，关注军事新闻",
                "tname": "网易军事",
                "ename": "wangyijunshi",
                "tid": "T1401334013017",
                "cid": "C1378977941637"
            }
        ],
        "docid": "CLJN5K2M000181KT",
        "picnews": true,
        "title": "为何抗战异常惨烈？日军并非如神剧中不堪一击",
        "tid": "",
        "template": "recommend",
        "threadVote": 30,
        "threadAgainst": 3,
        "boboList": [],
        "category": "历史",
        "replyBoard": "news_junshi_bbs",
        "source": "中国军网",
        "hasNext": false,
        "voicecomment": "off",
        "relative_sys": [
            {
                "id": "CLBSS1EJ000187UE",
                "title": "抗战期间,中国哪里的军人最容易变节投敌?",
                "source": "大象公会",
                "imgsrc": "http://cms-bucket.nosdn.127.net/f636439c8a89400c8cb829bfba778b2820170526101336.jpeg",
                "docID": "CLBSS1EJ000187UE",
                "from": "HZ",
                "type": "doc",
                "ptime": "2017-05-26 10:13:36",
                "href": ""
            },
            {
                "id": "CL7JRHFB0523D46J",
                "title": "一寸山河一寸血，南京光华门血战，撤退时教导总队泪奔了",
                "source": "不二书说历史",
                "imgsrc": "http://dingyue.nosdn.127.net/Ewnq46iqIU4hDHPhr3V80sK30DcK384lkBe0hNvRFoP=V1495621093803compressflag.jpg",
                "docID": "CL7JRHFB0523D46J",
                "from": "HZ",
                "type": "doc",
                "ptime": "2017-05-24 18:19:07",
                "href": ""
            },
            {
                "id": "CLC2DNAH05239N17",
                "title": "淞沪会战中，日军对中国军队是这样记载的！",
                "source": "68讲台",
                "imgsrc": "http://dingyue.nosdn.127.net/ogdZAXPtO2q8OK06qjeDTz2tWJ6bdjQ6MnqxnptQHvanQ1495770638931compressflag.jpg",
                "docID": "CLC2DNAH05239N17",
                "from": "HZ",
                "type": "doc",
                "ptime": "2017-05-26 11:50:42",
                "href": ""
            }
        ],
        "book": [],
        "ptime": "2017-05-29 11:07:54"
    }
}
 
```


### 1.3 本地新闻

**必选参数:**
  `name` 地名 如:广东省_深圳市，江西省_南昌市

  **接口地址:**
  `/News/local_news?name=广东省_深圳市`

  **调用例子:**
  `http://localhost:8050/index.php/index/News/local_news?name=广东省_深圳市`

  返回数据(每次返回是10条数据,这里就不全部列出来了)如下图:
  ```
   ```




## 2. 视频模块

说明: 包括 视频首页数据、视频分类列表 视频详情、如下详情：

### 2.1 视频首页数据

**必选参数:**
      `无`
      
  **接口地址:**
      `/index`
      
 **调用例子:**
      `http://localhost/index`
      返回数据(每次返回是10条数据,这里就不全部列出来了)如下图:
      ```
      ```

### 2.2 视频分类列表
**必选参数:**
`type` int : 新闻类型
<table>
       <tr>
        <td>type</td>
        <td>0</td>
        <td>1</td>
        <td>2</td>
        <td>3</td>
        <td>4</td>
       </tr>
       <tr>
        <td>名称</td>
        <td>精品视频</td>
        <td>搞笑视频</td>
        <td>美女视频</td>
        <td>体育视频</td>
        <td>新闻现场</td>
       </tr>
  </table>
  `page` int : 分页页数,每页返回10条
  **接口地址:**
  
  `/Video/video_type?type=2&page=10`
  **调用例子:** 
  
   `http://localhost:8050/index.php/index/Video/video_type?type=2&page=10`
   返回数据(每次返回是10条数据,这里就不全部列出来了)如下图:
``` javascript
{
    "msg": "success",
    "code": 1,
    "data": [
        {
            "sizeSHD": 22050,
            "replyCount": 0,
            "videosource": "新媒体",
            "mp4Hd_url": "http://flv2.bn.netease.com/videolib3/1705/30/aYNXb0812/HD/aYNXb0812-mobile.mp4",
            "title": "小清新美女爱跳舞，夜里房间优雅独舞",
            "cover": "http://vimg3.ws.126.net/image/snapshot/2017/5/J/F/VCKOETEJF.jpg",
            "videoTopic": {
                "alias": "多彩人生，你我共同编织",
                "tname": "韬哥学霸哥",
                "ename": "T1494085453258",
                "tid": "T1494085453258",
                "topic_icons": "http://dingyue.nosdn.127.net/tHYrjgCtrdmQP3Nvygaa75m3BMOxdY5ZJ8RVPGgMj9Njt1494085452329.jpg"
            },
            "description": "小清新美女爱跳舞，夜里房间优雅独舞",
            "replyid": "BKOD7PO4050835RB",
            "length": 147,
            "m3u8_url": "http://flv.bn.netease.com/videolib3/1705/30/aYNXb0812/SD/movie_index.m3u8",
            "vid": "VBKOD7PO4",
            "topicName": "韬哥学霸哥",
            "votecount": 0,
            "topicImg": "http://vimg3.ws.126.net/image/snapshot/2017/5/9/B/VCKI1SH9B.jpg",
            "topicDesc": "让生活慢下来，品味阅读，享受人生，活到老学到老，教育大家，心灵美好，我们一起携手共创美好世界。",
            "topicSid": "VCKI1SH8S",
            "replyBoard": "video_bbs",
            "playCount": 0,
            "sectiontitle": "",
            "mp4_url": "http://flv2.bn.netease.com/videolib3/1705/30/aYNXb0812/SD/aYNXb0812-mobile.mp4",
            "playersize": 1,
            "sizeSD": 11025,
            "sizeHD": 14700,
            "m3u8Hd_url": "http://flv.bn.netease.com/videolib3/1705/30/aYNXb0812/HD/movie_index.m3u8",
            "ptime": "2017-05-30 10:21:30"
        }
    ]
}
```

### 2.3 视频详情
**必选参数:**
`vid` 视频列表下的vid  VEKKO9TJP

**接口地址:**
`/Video/video_detail?vid=VEKKO9TJP`

**调用例子:**
 `http://localhost:8050/index.php/index/Video/video_detail?vid=VEKKO9TJP`
 返回数据(每次返回是10条数据,这里就不全部列出来了)如下图:
 
```javascript
{
    "msg": "success",
    "code": 1,
    "data": {
        "topicid": "1000",
        "replyCount": 0,
        "mp4Hd_url": "http://flv2.bn.netease.com/videolib3/1705/29/BWixL8250/HD/BWixL8250-mobile.mp4",
        "recommend": [],
        "title": "搞笑段子：老婆，咱们去旅游吧",
        "hits": 0,
        "cover": "http://vimg1.ws.126.net/image/snapshot/2017/5/S/Q/VCKMKITSQ.jpg",
        "replyBoard": "video_bbs",
        "replyid": "EKKO9TJP050835RB",
        "mp4_url": "http://flv2.bn.netease.com/videolib3/1705/29/BWixL8250/SD/BWixL8250-mobile.mp4",
        "length": 13,
        "videotype": "搞笑的小妖精",
        "playersize": 0,
        "vurl": "http://v.163.com/paike/VCH0LU18J/VEKKO9TJP.html",
        "m3u8Hd_url": "http://flv.bn.netease.com/videolib3/1705/29/BWixL8250/HD/movie_index.m3u8",
        "m3u8_url": "http://flv.bn.netease.com/videolib3/1705/29/BWixL8250/SD/movie_index.m3u8",
        "ptime": "2017-05-29 00:17:56",
        "vid": "VEKKO9TJP"
    }
}
 
```

## 3. 笑话段子轻松一刻

说明: 包括 视频首页数据、视频分类列表 视频详情、如下详情：

### 3.1 笑话段子

**必选参数:**
      `page`   分页数 10  20  30
      
 **接口地址:**
      `/Joke/index?page=10`
      
 **调用例子:**
      `http://localhost:8050/index.php/index/joke/index?page=10`
      返回数据(每次返回是10条数据,这里就不全部列出来了)如下图:
```javascript
{
    "msg": "success",
    "code": 1,
    "data": [
        {
            "adtype": 0,
            "boardid": "comment_bbs",
            "clkNum": 0,
            "danmu": 1,
            "digest": "上语文课时，老师提问：“小明，请你用文明礼貌的‘礼’字造个句子。”小明思索了一会说：“爸爸提着包出门托人办事。”老师说：“没‘礼’字呀？”小明认真的说：“咋没‘礼’呀？礼在包里呢，爸爸说没礼人家不办事。”",
            "docid": "CEJIS0I69001S0I7",
            "downTimes": 208,
            "imgType": 0,
            "imgsum": 0,
            "picCount": 0,
            "program": "HY",
            "recNews": 0,
            "recType": 0,
            "refreshPrompt": 0,
            "replyCount": 4,
            "replyid": "CEJIS0I69001S0I7",
            "source": "ZOL笑话大全",
            "title": "幽默的孩子和家长,不只是好笑。",
            "upTimes": 309
        }
    ]
}
```


## 4. 图片相册接口

说明: 包括 视频首页数据、视频分类列表 视频详情、如下详情：

### 4.1 cosplay 相册

**必选参数:**
      `page`   分页数 10  20  30 
      
 **接口地址:**
      `/Picture/index?page=20` 
      
  **调用例子:**
      `http://localhost:8050/index.php/index/picture/index?page=20`
      
返回数据(每次返回是10条数据,这里就不全部列出来了)如下图:
```javascript
{
    "msg": "success",
    "code": 1,
    "data": [
        {
            "desc": "喜欢神奇宝贝的人一定都知道鲤鱼王。这个特别的精灵没有特别强大的能力，除了长相呆萌，好像没有其他优点。不过下面这名男子却对这个超弱的精灵情有独钟，他戴着鲤鱼王面具大玩Cosplay，照片被上传到网路后立刻成为网友们热议的话题。",
            "pvnum": "",
            "createdate": "2017-01-11 01:39:21",
            "scover": "http://img3.cache.netease.com/photo/0031/2017-01-11/s_CAFBLLL26LRK0031.jpg",
            "setname": "靠Cosplay鲤鱼王而走红的型男真面目",
            "cover": "http://img3.cache.netease.com/photo/0031/2017-01-11/CAFBLLL26LRK0031.jpg",
            "pics": [
                "http://img3.cache.netease.com/photo/0031/2017-01-11/CAFBLLL26LRK0031.jpg",
                "http://img4.cache.netease.com/photo/0031/2017-01-11/CAFBLLTT6LRK0031.jpg",
                "http://img4.cache.netease.com/photo/0031/2017-01-11/CAFBLM0J6LRK0031.jpg"
            ],
            "clientcover1": "",
            "replynum": "57",
            "topicname": "",
            "setid": "91744",
            "seturl": "http://play.163.com/photoview/6LRK0031/91744.html",
            "datetime": "2017-01-11 01:42:32",
            "clientcover": "",
            "imgsum": "7",
            "tcover": "http://img4.cache.netease.com/photo/0031/2017-01-11/t_CAFBLLL26LRK0031.jpg"
        },
        {
            "desc": "最后要推荐的一组图是台湾Coser：Mon小夢夢的最新作品——菲利克斯COS。在原作里，这位角色拥有着不属于女性的萌系着装以及言行举止，然而事实上却是个真·汉子......",
            "pvnum": "",
            "createdate": "2017-01-10 10:58:46",
            "scover": "http://img4.cache.netease.com/photo/0031/2017-01-10/s_CADP9L5P6LRK0031.jpg",
            "setname": "灵魂陷入危机之中 Re:0菲利克斯COS",
            "cover": "http://img3.cache.netease.com/photo/0031/2017-01-10/CADP9L5P6LRK0031.jpg",
            "pics": [
                "http://img3.cache.netease.com/photo/0031/2017-01-10/CADP9L5P6LRK0031.jpg",
                "http://img3.cache.netease.com/photo/0031/2017-01-10/CADP9JU36LRK0031.jpg",
                "http://img4.cache.netease.com/photo/0031/2017-01-10/CADP9K7J6LRK0031.jpg"
            ],
            "clientcover1": "",
            "replynum": "0",
            "topicname": "",
            "setid": "91731",
            "seturl": "http://play.163.com/photoview/6LRK0031/91731.html",
            "datetime": "2017-01-10 11:00:15",
            "clientcover": "",
            "imgsum": "5",
            "tcover": "http://img3.cache.netease.com/photo/0031/2017-01-10/t_CADP9L5P6LRK0031.jpg"
        }
    ]
}

```


