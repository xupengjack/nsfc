# 国家自然科学基金查询
---
## 相关查询网站
### * http://www.letpub.com.cn/?page=grant
> 本爬虫使用，速度较快，但没有摘要等详细信息

### http://output.nsfc.gov.cn
> API接口较好，但资助项目检索需要验证码
> - 资助项目检索：http://output.nsfc.gov.cn/fundingQuery
> - 结题项目检索：http://output.nsfc.gov.cn/projectQuery
> - 结题项目详情：http://output.nsfc.gov.cn/conclusionProject/30360042
> - 申请代码：http://output.nsfc.gov.cn/common/data/fieldCode
> - 资助类别：http://output.nsfc.gov.cn/common/data/supportTypeData

### http://fund.sciencenet.cn/
> 查询方式不好：当 负责人/项目批准号/依托单位 都不存在时，项目名称不能为空

### https://isisn.nsfc.gov.cn/egrantindex/funcindex/prjsearch-list
> 官网，超难用。

### https://www.medsci.cn/sci/nsfc.do
> 查询不好用


## 使用
```bash
git clone https://github.com/suqingdong/nsfc.git
cd nsfc

mkdir test
cd test

# eg.: 爬取2019年C,H学科数据
scrapy crawl nsfc_spider \
  -a code=C,H \
  -a startTime=2019 \
  -a endTime=2019 \
  -o nsfc.2019.jl \
  -L INFO \
  --logfile nsfc.2019.log
```

## TODO
- 结题项目摘要信息补充
