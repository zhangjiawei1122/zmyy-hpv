# 知苗易约抢购

## 严正声明

1. 严禁使用此项目的代码及其衍生品程序进行任何的交易行为
2. 此项目仅供学习交流以及非盈利使用
3. 所有使用此项目所造成的法律后果均由使用者承担，与原作者无关
4. 本人未对微信以及知苗的服务器和客户端进行任何形式的攻击或者修改，完成本项目所需所有资料均来自互联网搜索
5. 如果你使用此项目，代表你接受上述条款
6. 希望所有适龄女孩子都能打上hpv，大家都有一个美好的未来，共勉

## 环境准备

1. python 3.8，需要安装
2. wechat 3.4.0.38，需要安装
3. mitmproxy，需要配置受信任的根证书

## 本项目优势

1. 无需抓包
2. 傻瓜式使用
3. **真的能抢到，这点很重要**

## 使用方法

1. 下载代码
2. 安装依赖
   ```
   pip install -r requirements.txt
    ```
3. 修改配置
   ```
   修改 main.py 470行
   config = {
        # 知苗配置
        "zhimiao": {
            # 省
            "province": "重庆市",
            # 市
            "city": "重庆市",
            # 县/区 可留空
            "county": "",
            # 城市代码
            "cityCode": "500000",
            # 疫苗名称
            "vaccines": "九价人乳头瘤病毒疫苗",
            # 医院名称
            "cname": "重庆市荣昌区昌州街道社区卫生服务中心",
            # 抢购开始时间
            "startTime": "2022-06-24 09:15:00.000",
            # 接种日期，如果公告有接种日期可以提前配置，没有时会自动获取
            # "dates": ["2022-06-15"],
            # 第几针
            "Ftime": 1
        }
    }
   ```
4. 执行代码（**注意：执行代码之前需要先登陆微信，建议在抢购开始前15分钟左右执行程序**）
   ```
   python main.py
   ```
5. 操作小程序
   ```
   打开知苗易约小程序->点击右下角我的
   ```
6. 等待程序自动抢购
7. 查看日志

## 其他

1. 如果断网，请手动执行`close_proxy.bat`
2. 建议同步一下知苗服务器的时间
3. 如果遇到一些奇奇怪怪的问题，建议重启微信，并重启脚本，重试
