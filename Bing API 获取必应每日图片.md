# Bing API 获取必应每日图片

> 此 API 收集自网络，时间久远，忘记出处了。

## 每日图片

![每日图片](https://www.bing.com/th?id=OHR.OldManWhiskers_ZH-CN9321160932_1920x1080.jpg&rf=LaDigue_1920x1080.jpg&pid=hp)

## API 接口

- 接口：[http://www.bing.com/HPImageArchive.aspx?format=js&idx=0&n=1&mkt=zh-CN](http://www.bing.com/HPImageArchive.aspx?format=js&idx=0&n=1&mkt=zh-EN)

**mkt 参数**

| 参数      | 含义         |
| --------- | ------------ |
| zh-CN | 返回中文数据 |
| en-US | 返回英文数据 |

## 使用说明

拼接 `https://www.bing.com` + `images[0].url` 为图片链接。

## 返回 Json 数据格式

```json
{
	"images": [{
		"startdate": "20200527",
		"fullstartdate": "202005271600",
		"enddate": "20200528",
		"url": "/th?id=OHR.OldManWhiskers_ZH-CN9321160932_1920x1080.jpg&rf=LaDigue_1920x1080.jpg&pid=hp",
		"urlbase": "/th?id=OHR.OldManWhiskers_ZH-CN9321160932",
		"copyright": "结籽时的三花锦葵的长羽 (© Sunshine Haven Photo/Shutterstock)",
		"copyrightlink": "https://www.bing.com/search?q=%E4%B8%89%E8%8A%B1%E9%94%A6%E8%91%B5&form=hpcapt&mkt=zh-cn",
		"title": "",
		"quiz": "/search?q=Bing+homepage+quiz&filters=WQOskey:%22HPQuiz_20200527_OldManWhiskers%22&FORM=HPQUIZ",
		"wp": true,
		"hsh": "ff2d060438b1a2b190d523db49725ec8",
		"drk": 1,
		"top": 1,
		"bot": 1,
		"hs": []
	}],
	"tooltips": {
		"loading": "正在加载...",
		"previous": "上一个图像",
		"next": "下一个图像",
		"walle": "此图片不能下载用作壁纸。",
		"walls": "下载今日美图。仅限用作桌面壁纸。"
	}
}
```


