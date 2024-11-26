# TrafficLanguageDataSet
本仓库存储交通大语言模型数据集（Traffic large language model dataset）。使用json的方式存储对于视频中某个时间点发生的事件的描述。
# 描述视频中交通事件的json格式如下：
1，文件名与视频对应
2，以问答的形式标注数据
3，如需（建议都标明时间）标明发生时间，则使用<s*i*>标明开始时间，<e*i*>表明结束时间。
示例：
```
[
    {
        "id": "Mq57LwS2UtI",
        "conversations": [
            {
                "from": "human",
                "value": "<video>\nCould you provide a summary of the incidents that occurred at various timestamps in the video?"
            },
            {
                "from": "gpt",
                "value": "A crowd of people watching an asian news broadcast from <s0> to <e0>. An image of the news, showing people at a church from <s1> to <e1>."
            }
        ],
        "meta": {
            "split": [
                77.3,
                85.0
            ],
            "duration": 7.7,
            "token": {
                "<s0>": 0,
                "<e0>": 3.5,
                "<s1>": 3.5,
                "<e1>": 7.7
            }
        },
        "source": "internvid"
    },
    {
        "id": "3n3oCNerzV0",
        "conversations": [
            {
                "from": "human",
                "value": "<video>\nI'd appreciate it if you could provide a detailed account of the events that occurred at different timestamps in the video."
            },
            {
                "from": "gpt",
                "value": "From <s0> to <e0>, woman is counting money with a pen on a white table. From <s1> to <e1>, two people shaking hands in front of a desk."
            }
        ],
        "meta": {
            "split": [
                129.8,
                184.0
            ],
            "duration": 54.2,
            "token": {
                "<s0>": 0,
                "<e0>": 9.4,
                "<s1>": 49.4,
                "<e1>": 54.2
            }
        },
        "source": "internvid"
    }
]
```
