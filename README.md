# xxl-job-admin-sdk
使用java代码控制xxl-job-admin。使用代码添加job的CRUD等功能
下面是自动配置类，默认配置如下
```
@Data
@ConfigurationProperties(prefix = "xxl.job.sdk")
public class XxlJobAdminProperties {
    private String adminUrl = "http://localhost:8080/xxl-job-admin";
    private String userName = "admin";
    private String password = "123456";
    private int connectionTimeOut = 5000;

    private boolean enable = false;
}
```
# 使用方法
1. 下载本项目install到本地maven仓库
2. 其它需要通过代码添加job的spring boot项目加入本项目的依赖
3. 配置参数如下
5. <img width="576" alt="image" src="https://user-images.githubusercontent.com/18614347/155741835-892c54a7-cdd0-4f5e-b414-98c34b9b43a8.png">
6. 接下来注入关键的类，使用XxlJobService来控制job的crud
7. <img width="337" alt="image" src="https://user-images.githubusercontent.com/18614347/155742249-49778cf5-b6e8-4317-9020-78df46b023fc.png">

使用方法就是这样，现在只接入了JOB的crud，后续看项目情况也许会接入其它接口。
如果大家有什么问题，欢迎大家提出来。这个项目写的很粗糙，大家有什么意见和建议，非常欢迎大家来交流。谢谢
