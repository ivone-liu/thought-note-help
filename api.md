## API

方寸笔迹提供对有开发能力开发者的公共调用API，可以通过API的形式来实现方寸笔迹数据内容的交互。

基于对安全性的考量，目前仅提供对笔记的录入功能，每位用户每日调用上限为1000次，即可通过API每日写入1000条笔记。

其中笔记的格式与内容，跟直接写笔记的方式和语法一致，没有针对API进行额外的笔记负担。



### 使用方法

API可以在主界面获取，拿到API后，可以通过POST方式调用。

```shell
curl -X POST 
	-d '{"note": "Hello,#note this note was sended via API"}' 
	"https://api.fang-cun.net/api/open/note/...."
```

**参数**

| 参数 | 类型   | 说明     | 必传 |
| ---- | ------ | -------- | ---- |
| note | string | 笔记内容 | √    |



### 示例

- 微信读书导入方寸笔迹 [Github](https://github.com/ivone-liu/ThoughtNote-Weread-Sync) / [码云](https://gitee.com/ivonee/ThoughtNote-Weread-Sync)