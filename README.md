# CloudXNS_Python3_SDK
CloudXNS API Python3 Software Development Kit

![CloudXNS_LOGO](https://www.cloudxns.net/Public/Sun/images/common/logo3.png)

CloudXNS 官方提供的SDK是基于Pyton2提供的，本项目根据CloudXNS官方提供的API开发了Python3上可以正常使用的SDK

CloudXNS官方api文档，返回的错误代码请参考
>https://www.cloudxns.net/Public/Doc/CloudXNS_api2.0_doc_zh-cn.zip

如发现本SDK存在问题，请联系我进行改进。
Examples
--------
使用之前请先import CloudXNS_APISDK    
    
    import CloudXNS_APISDK   
    #设置API KEY
    api=CloudXNS_API(api_key='fffffffffffffffffffffffffffffffff',secret_key='ffffffffffffffff',debug_log=True)
    #返回域名列表 返回内容为json格式str
    print(api.domain_list())
    #向账户添加域名 test.org
    api.domain_add('test.org')
    #快速修改ddns记录的值
    api.domain_host_DDNS('ddns.test.org')
    #http dns请求www.test.net
    str=api.http_dns_get('www.test.net')
    #转换str到dict
    dict=api.json_strtodict(str)

***更多功能，使用说明请参考官方文档或SDK中的注释***

License
-------

MIT License

Copyright (c) 2016 wevsty

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
