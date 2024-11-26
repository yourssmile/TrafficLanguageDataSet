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
                "value": "<video>\nCan you point out if anyone is making a right turn in the video??"
            },
            {
                "from": "gpt",
                "value": "Sure, someone just started a right turn at <s0> and ended a right turn at <e0>."
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
                "<e0>": 3.5
            }
        },
        "source": "internvid"
    },
    {
        "id": "3n3oCNerzV0",
        "conversations": [
            {
                "from": "human",
                "value": "<video>\nThis is a no-parking section. Help me see if anyone has parked here."
            },
            {
                "from": "gpt",
                "value": "At <s0> a car stopped, and at <s1> another car stopped nearby, but neither car left."
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
                "<s1>": 9.4
            }
        },
        "source": "internvid"
    }
]
```
