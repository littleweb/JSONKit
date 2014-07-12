#使用方法

引入`JSONkit.h`

新建一个方法

```
-(NSDictionary *)JSONparse:(NSString *)json
{
    NSData  *jsonData = [json dataUsingEncoding:NSUTF8StringEncoding];
    
    NSDictionary *_result = [jsonData objectFromJSONData];
    
    return _result;
}
```

#注意

jsonkit不支持ARC，在使用时，需要做如下设置；

依次展开：Build Phases -> Complie Sorce -> 双击 JSONKit.m -> 输入`-fno-objc-arc`