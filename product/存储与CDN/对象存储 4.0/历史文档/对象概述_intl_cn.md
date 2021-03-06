## 对象
对象是腾讯云 COS 中存储的基本单元，对象必须存储在存储桶中。用户可以通过腾讯云控制台、API、SDK 等多种方式管理对象
用户可以通过控制台对对象进行相关配置，具体请参考以下内容：
- [搜索对象](/doc/product/436/6256)
- [查看对象信息](/doc/product/436/6257)
- [设置对象权限](/doc/product/436/6371)
- [设置 HTTP 头部](/doc/product/436/6258)

## 对象名称
腾讯云 COS 中的对象需具有合法的名称，对象名称是对象在存储桶中的唯一标识。在控制台，存储桶中可以遍历对象名称。
对象名称采用 Unicode 字符，虽然可以在名称中使用任何 UTF-8 字符，但是不同应用程序对特殊字符的分析方式可能不同。以下原则有助于最大程度符合 DNS、Web 安全字符、XML 分析器和其他 API 的要求。以下字符集通常可安全地用于对象名称：

| 类型     | 详细内容                 |
| ------ | -------------------- |
| 字母数字字符 | [0-9 , a-z , A-Z]    |
| 特殊字符   | `!`、`-`、`_`、`.`、`* ` |

> <font color="#0000cc">**注意：** </font>
对象名称中不支持下列 ASCII 控制字符：
- 字符上(↑)：CAN (24) 
- 字符下(↓)：EM (25)
- 字符右(→)：SUB (26)
- 字符左(←)：ESC (27) 

以下是合法的对象名称示例：
- my-organization
- my.great_photos-2016/01/me.jpg
- videos/2016/birthday/video1.wmv
 
为方便用户管理存储对象，控制台可以创建文件夹，存储和管理对象。具体请参阅 [创建文件夹](https://cloud.tencent.com/document/product/436/6263)。
## 访问地址
对象的访问地址都是基于存储桶的访问地址和对象名称的，腾讯云的对象访问地址构成为`[存储桶域名]/[对象名称]`。
例如：
APPID 为1234567890 的用户创建了名为 example，所属地域为广州（华南）的存储桶，并在根目录上传了名为 example.exe 的对象。example.exe 的访问地址如下：

```
JSON API：example-1234567890.cosgz.myqcloud.com/example.exe
XML API：example-1234567890.cos.ap-guangzhou.myqcloud.com/example.exe
```
有关存储桶的域名管理请参阅 [域名管理](https://cloud.tencent.com/document/product/436/6252)。
