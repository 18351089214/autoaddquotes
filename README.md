# autoaddquotes
###格式化请求头参数
在写爬虫程序时，一般会直接从网页源码中把请求头复制到代码里，直接复制的文本一般不是我们要的格式，所以
需要格式化一下，原始格式如下：

####输入文本：
'''
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3
Accept-Encoding: gzip, deflate, br
Accept-Language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7
Connection: keep-alive
Cookie: __mta=212211371.1562460994380.1562461111909.1562461116546.12; uuid_n_v=v1; uuid=10190B70A05211E9AF250DFC2B22F9F2130FB3172B8441F8B46D51CE00412021; _csrf=e1175ecb0e137164f270b9b3b9c9fc711f1dbf82e8eb2d39bfa22695c41fa183; _lxsdk_cuid=16bc9eebac7c8-0934d6c9528e1e-37677e02-fa000-16bc9eebac7c8; _lxsdk=10190B70A05211E9AF250DFC2B22F9F2130FB3172B8441F8B46D51CE00412021; _lx_utm=utm_source%3DBaidu%26utm_medium%3Dorganic; __mta=212211371.1562460994380.1562461085144.1562461094247.8; _lxsdk_s=16bc9eebac8-88d-d19-7b3%7C%7C35
Host: maoyan.com
Referer: https://maoyan.com/board/4?offset=10
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3770.100 Safari/537.36
'''

####输出结果：
"""
'Accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3',
'Accept-Encoding': 'gzip, deflate, br',
'Accept-Language': 'en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7',
'Connection': 'keep-alive',
'Cookie': '__mta=212211371.1562460994380.1562461111909.1562461116546.12; uuid_n_v=v1; uuid=10190B70A05211E9AF250DFC2B22F9F2130FB3172B8441F8B46D51CE00412021; _csrf=e1175ecb0e137164f270b9b3b9c9fc711f1dbf82e8eb2d39bfa22695c41fa183; _lxsdk_cuid=16bc9eebac7c8-0934d6c9528e1e-37677e02-fa000-16bc9eebac7c8; _lxsdk=10190B70A05211E9AF250DFC2B22F9F2130FB3172B8441F8B46D51CE00412021; _lx_utm=utm_source%3DBaidu%26utm_medium%3Dorganic; __mta=212211371.1562460994380.1562461085144.1562461094247.8; _lxsdk_s=16bc9eebac8-88d-d19-7b3%7C%7C35',
'Host': 'maoyan.com',
'Referer': 'https://maoyan.com/board/4?offset=10',
'Upgrade-Insecure-Requests': '1',
'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3770.100 Safari/537.36',
"""
