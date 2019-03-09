# Android Logger存储到本地-未生成日志文件



1、描述：

​	使用Logger

Logger日志地址

<https://github.com/orhanobut/logger>

2、解决方案：

​	动态申请权限，代码如下：

```java
private void requsetStoragePermission() {
    if (ActivityCompat.checkSelfPermission(this, 	        Manifest.permission.READ_EXTERNAL_STORAGE) != PackageManager.PERMISSION_GRANTED) {
        ActivityCompat.requestPermissions(this, new String[]{
           Manifest.permission.READ_EXTERNAL_STORAGE}, REQUEST_READ_EXTERNAL_STORAGE);
    }
}
```

查找原因：

1、分析Logger

 ![img](image/2019-3-9-1.jpg)

2、结论