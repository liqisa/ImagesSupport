# Requirements
环境配置详情参考Dockerfile

# Models
models/sm_black_1.tronmodel  
models/sm_black_2.tronmodel  
models/sm_black_3.tronmodel  

# Images
测试图片从48类中抽取出了8类，每类1张，共计8张    
图片命名为index_class_name_number.jpg  
> 注：index 为类别序号，class_name 为类别名， number为每张图的编号

**例：**                                
images/2_bk_boom_smoke_0227_3370.jpg  


```shell
$ mkdir build   
   
$ cd build && cmake ..   
   
$ make   
   
$ ./test_hades ../models/sm_black_1.tronmodel   \  
               ../models/sm_black_2.tronmodel   \  
               ../models/sm_black_3.tronmodel   \  
               
```

| name | infer_time_avg | GPU | batch |
| --- | ---| --- | --- |
| sm_black_SDK | 9.99325ms | P4 | 8 |
