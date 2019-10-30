
POM   Project Object Model 项目对象模型
dependency  依赖，依赖关系，相依性

@SpringBootApplication是Sprnig Boot项目的核心注解，主要目的是开启自动配置  
@RestController注解等价于@Controller+@ResponseBody的结合，使用这个注解的类里面的方法都以json格式输出  
@Configuration 代表这是一个Java配置文件



控制反转 Inversion of Control ，IoC
面向切面编程 Aspect Oriented Programming,AOP


Spring 中把每一个需要管理的对象称为Spring Bean(简称：Bean)

扫描装配Bean到IoC容器中，使用@Component 和@ComponentScan
@Component 是标明那个类被扫描进入Spring IoC容器中，
@ComponentScan 则是标明采用何种策略去扫描装配Bean.  

@Autowired 根据属性的类型（by type）找到对应的Bean进行注入（注入用户服务）

@Primary 当发现有多个同样类型的Bean时，请优先使用我进行注入，

@Qualifier 它的配置项value需要一个字符串去定义，它将与@Autowired组合在一起，通过类型和名称一起找到Bean  
	@Autowired
	@Qualifier("dog")
	private Animal animal = null;
Spring IoC将会以类型和名称去寻找对应的Bean进行注入。  


Bean生命周期  
*Spring通过我们的配置，如@ComponentScan定义的扫描路径去找到带有@Component的类，这个过程就是一个资源定位的过程  
*一旦找到了资源，那么它就开始解析,并且将定义的信息保存起来。注意，此时还没有初始化Bean,也就没有Bean的实例，它有的仅仅是Bean的定义。  
*然后就会把Bean定义发布到Spring IoC容器中。此时，IoC容器也只有Bean的定义，还是没有Bean的实例生成。  


@Profile

@Transcational  表明该方法需要事务运行

Spring AOP是一种基于方法的AOP,它只能应用于方法上。  



@Aspect  Spring是以@Aspect作为切面声明的，当以@Aspect作为注解时，Spring就会知道这是一个切面，然后我们就可以通过各类 
注解来定义各类的通知了。  

@RequestingMapping("...") 定义请求 代表请求路径和控制器(或其方法)的映射关系  
@ResponseBody  转换为JSON

@DeclareParents  引入新的类来增强服务，它有两个必须配置的属性value和defaultImpl.  
*value:指向你要增强的目标对象，  
*defaultImpl:引入增强功能的类  



织入  
织入是一个生成动态代理对象并且将切面和目标对象方法编织成为约定流程的过程  


POJO  Plain Ordinary Java Object

query 查询


JPA(Java Persistence API，Java持久化API),是定义了对象关系映射(ORM)以及实体对象持久化的标准接口。  


MyBatis 的官方定义为：MyBatis是支持定制化SQL\存储过程以及高级映射的优秀的持久层框架。  

MapperFactoryBean是针对一个接口配置，
MapperScannerConfiguer扫描装配，也就是提供扫描装配MyBatis的接口道Spring IoC容器中。  
@MapperScan 也能够将MyBatis所需的对应接口扫描装配到Spring IoC容器中  


Maven 项目对象模型(POM),可以通过一小段描述信息来管理项目的构建


[Druid](https://github.com/alibaba/druid)  
[Druid常见问题](https://github.com/alibaba/druid/wiki/%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98)  
Druid:Java语言中最好的数据库连接池。Druid能够提供强大的监控和扩展功能  






@Transcational 声明式事务(建议放在实现类上使用这个注解)




数据访问层 DAO
业务层 service
控制器 Controller


@PathVariable("id") long id
@RequestParam("id") long id
@RequestParam(value = "userName",required = false,defalutValue = "") String userName





&lt;<  小于号；
 
&gt;> 大于号； 
 
&amp; & 和 ；
 
&apos;  ‘’单引号； 
 
&quot; “”  双引号；  






















































