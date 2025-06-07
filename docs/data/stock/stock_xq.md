## [AKShare](https://github.com/akfamily/akshare) 股票数据

### A 股

#### 个股信息查询-雪球

接口: stock_individual_basic_info_xq

目标地址: https://xueqiu.com/snowman/S/SH601127/detail#/GSJJ

描述: 雪球财经-个股-公司概况-公司简介

限量: 单次返回指定 symbol 的个股信息

输入参数

| 名称    | 类型  | 描述                             |
| ------- | ----- | -------------------------------- |
| symbol  | str   | symbol="SH601127"; 股票代码      |
| token   | str   | token=None;                      |
| timeout | float | timeout=None; 默认不设置超时参数 |

输出参数

| 名称  | 类型   | 描述 |
| ----- | ------ | ---- |
| item  | object | -    |
| value | object | -    |

接口示例

```python
import akshare as ak

stock_individual_basic_info_xq_df = ak.stock_individual_basic_info_xq(symbol="SH601127")
print(stock_individual_basic_info_xq_df)
```

数据示例

```
                            item                                              value
0                         org_id                                         T000071215
1                    org_name_cn                                        赛力斯集团股份有限公司
2              org_short_name_cn                                                赛力斯
3                    org_name_en                               Seres Group Co.,Ltd.
4              org_short_name_en                                              SERES
5        main_operation_business      新能源汽车及核心三电(电池、电驱、电控)、传统汽车及核心部件总成的研发、制造、销售及服务。
6                operating_scope  　　一般项目：制造、销售：汽车零部件、机动车辆零部件、普通机械、电器机械、电器、电子产品（不...
7                district_encode                                             500106
8            org_cn_introduction  赛力斯始创于1986年，是以新能源汽车为核心业务的技术科技型汽车企业。现有员工1.6万人，A...
9           legal_representative                                                张正萍
10               general_manager                                                张正萍
11                     secretary                                                 申薇
12              established_date                                      1178812800000
13                     reg_asset                                       1509782193.0
14                     staff_num                                              16102
15                     telephone                                     86-23-65179666
16                      postcode                                             401335
17                           fax                                     86-23-65179777
18                         email                                    601127@seres.cn
19                   org_website                                   www.seres.com.cn
20                reg_address_cn                                      重庆市沙坪坝区五云湖路7号
21                reg_address_en                                               None
22             office_address_cn                                      重庆市沙坪坝区五云湖路7号
23             office_address_en                                               None
24               currency_encode                                             019001
25                      currency                                                CNY
26                   listed_date                                      1465920000000
27               provincial_name                                                重庆市
28             actual_controller                                       张兴海 (13.79%)
29                   classi_name                                               民营企业
30                   pre_name_cn                                     重庆小康工业集团股份有限公司
31                      chairman                                                张正萍
32               executives_nums                                                 20
33              actual_issue_vol                                        142500000.0
34                   issue_price                                               5.81
35             actual_rc_net_amt                                        738451000.0
36              pe_after_issuing                                              18.19
37  online_success_rate_of_issue                                           0.110176
38            affiliate_industry         {'ind_code': 'BK0025', 'ind_name': '汽车整车'}
```

#### 实时行情数据

##### 实时行情数据-雪球

接口: stock_individual_spot_xq

目标地址: https://xueqiu.com/S/SH513520

描述: 雪球-行情中心-个股

限量: 单次获取指定 symbol 的最新行情数据

输入参数

| 名称    | 类型  | 描述                                                                                             |
| ------- | ----- | ------------------------------------------------------------------------------------------------ |
| symbol  | str   | symbol="SH600000"; 证券代码，可以是 A 股个股代码，A 股场内基金代码，A 股指数，美股代码, 美股指数 |
| token   | float | token=None; 默认不设置 token                                                                     |
| timeout | float | timeout=None; 默认不设置超时参数                                                                 |

输出参数

| 名称  | 类型   | 描述 |
| ----- | ------ | ---- |
| item  | object | -    |
| value | object | -    |

接口示例

```python
import akshare as ak

stock_individual_spot_xq_df = ak.stock_individual_spot_xq(symbol="SH600000")
print(stock_individual_spot_xq_df.dtypes)
```

数据示例

```
        item                value
0         代码             SH600000
1      52周最高                11.02
2        流通股          29352178996
3         跌停                 8.69
4         最高                10.29
5        流通值       299392225759.0
6     最小交易单位                  100
7         涨跌                 0.55
8       每股收益                 1.54
9         昨收                 9.65
10       成交量            149422915
11       周转率                 0.51
12     52周最低               6.8673
13        名称                 浦发银行
14       交易所                   SH
15    市盈率(动)                6.615
16  基金份额/总股本          29352178996
17   净资产中的商誉             0.726713
18        均价               10.048
19        涨幅                  5.7
20        振幅                  5.6
21        现价                 10.2
22    今年以来涨幅                -0.87
23      发行日期  1999-11-10 00:00:00
24        最低                 9.75
25  资产净值/总市值       299392225759.0
26   股息(TTM)                0.321
27  股息率(TTM)                3.147
28        货币                  CNY
29     每股净资产                22.36
30    市盈率(静)                6.615
31       成交额         1501459278.0
32       市净率                0.456
33        涨停                10.62
34  市盈率(TTM)                6.615
35        时间  2025-04-08 15:00:00
36        今开                 9.77
```


### 美股


#### 个股信息查询-雪球

接口: stock_individual_basic_info_us_xq

目标地址: https://xueqiu.com/snowman/S/NVDA/detail#/GSJJ

描述: 雪球-个股-公司概况-公司简介

限量: 单次返回指定 symbol 的个股信息

输入参数

| 名称    | 类型  | 描述                             |
| ------- | ----- | -------------------------------- |
| symbol  | str   | symbol="NVDA"; 股票代码          |
| token   | str   | token=None;                      |
| timeout | float | timeout=None; 默认不设置超时参数 |

输出参数

| 名称  | 类型   | 描述 |
| ----- | ------ | ---- |
| item  | object | -    |
| value | object | -    |

接口示例

```python
import akshare as ak

stock_individual_basic_info_us_xq_df = ak.stock_individual_basic_info_us_xq(symbol="SH601127")
print(stock_individual_basic_info_us_xq_df)
```

数据示例

```
                             item                                              value
0                          org_id                                         T000040433
1                     org_name_cn                                              英伟达公司
2               org_short_name_cn                                                英伟达
3                     org_name_en                                 Nvidia Corporation
4               org_short_name_en                                             Nvidia
5         main_operation_business                                           图形和通信处理器
6                 operating_scope  公司的图形和通信处理器已被多种多样的计算平台采用，包括个人数字媒体PC、商用PC、专业工作站...
7                 district_encode                                             001008
8             org_cn_introduction  英伟达公司于1993年4月在加利福尼亚州注册成立，并于1998年4月在特拉华州重新注册成立。...
9            legal_representative                                               None
10                general_manager                                               None
11                      secretary                                               None
12               established_date                                               None
13                      reg_asset                                               None
14                      staff_num                                              36000
15                      telephone                                      1-408-4862000
16                       postcode                                              95051
17                            fax                                               None
18                          email                                               None
19                    org_website                                     www.nvidia.com
20                 reg_address_cn                                               特拉华州
21                 reg_address_en                                               特拉华州
22              office_address_cn                                               None
23              office_address_en  2788 San Tomas Expressway\r\nSanta Clara\r\nCa...
24                currency_encode                                               None
25                       currency
26                    listed_date                                       916981200000
27                         td_mkt                                      美国NASDAQ证券交易所
28                       chairman                                               None
29                executives_nums                                                  6
30  actual_issue_total_shares_num                                               None
31             actual_issue_price                                               None
32            total_raise_capital                                               None
33                     mainholder                                       领航集团 (8.30%)
```

### 港股


#### 个股信息查询-雪球

接口: stock_individual_basic_info_hk_xq

目标地址: https://xueqiu.com/S/00700

描述: 雪球-个股-公司概况-公司简介

限量: 单次返回指定 symbol 的个股信息

输入参数

| 名称    | 类型  | 描述                             |
| ------- | ----- | -------------------------------- |
| symbol  | str   | symbol="02097"; 股票代码         |
| token   | str   | token=None;                      |
| timeout | float | timeout=None; 默认不设置超时参数 |

输出参数

| 名称  | 类型   | 描述 |
| ----- | ------ | ---- |
| item  | object | -    |
| value | object | -    |

接口示例

```python
import akshare as ak

stock_individual_basic_info_hk_xq_df = ak.stock_individual_basic_info_hk_xq(symbol="02097")
print(stock_individual_basic_info_hk_xq_df)
```

数据示例

```
           item                                              value
0       comunic                                        231269720.0
1     comcnname                                         蜜雪冰城股份有限公司
2     comenname                                        MIXUE Group
3       incdate                                    1209484800000.0
4        rgiofc                 中国河南省郑州市金水区北三环南、文化路东瀚海北金商业中心16004室
5    hofclctmbu                 中国河南省郑州市金水区北三环南、文化路东瀚海北金商业中心16004室
6      chairman                                                张红超
7           mbu                                             现制饮品企业
8       comintr  我们是一家领先的现制饮品企业,聚焦为广大消费者提供单价约6元人民币(约1美元)的高质平价的现...
9     refccomty                                                1.0
10     numtissh                                         17059900.0
11         ispr                                              202.5
12         nrfd                                       3291000000.0
13  nation_name                                                 中国
14          tel                                      0371-89834090
15          fax                                      0371-89916887
16        email                                dongshihui@mxbc.com
17     web_site                                http://www.mxbc.com
18    lsdateipo                                    1740931200000.0
19   mainholder                                                张红超
```
