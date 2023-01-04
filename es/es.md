


### 查询
#### 精确查询
`filters` 关键字搭配
`term ` 查询，处理数字(number)，布尔(bool)、日期(date)以及文本(text)

当需要查询一个精确值的时候，不需要对结果进行评分计算，只需要对文档进行包括或者排除的计算，可以使用 ``constant_score ``关键字进行非评分模式的查询
```sql

GET /bank/_search
{
  "query": {
    "constant_score": {
      "filter": {
        "term": {
          "age": "36"
        }
      }
    }
  }
}
```


#### 组合过滤器
- must 所有的语句必须和 must 匹配，类似 and
- should 至少由一个匹配，类似 or
- must not  所有的语句都不能匹配 类似 not

#### 范围

- range 查询某个范围内的文档,类似 between and


- gt 大于
- lt 小于
- gte 大于等于
- lte 小于等于

```sql

```


#### 处理 NULL值