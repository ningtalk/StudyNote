**1、spring bean生命周期**  
1、Instantiate：spring IOC容器根据配置文件（基于xml配置元数据）bean定义的顺序来实例化Bean；  
2、Populate properties:设置属性值；  
3、BeanNameAware：Bean若实现了BeanNameAware接口，则调用其方法setBeanName；  
4、BeanFactoryAware：Bean若实现了BeanFactoryAware接口，则调用其方法setBeanFactory；  
5、ApplicationContextAware  
4、BeanPostProcessor:调用BeanPostProcessor的预初始化方法postProcessBeforeInitialization；  
5、InitializingBean：Bean若实现了InitializingBean接口，则调用其方法afterPropertiesSet；  
6、init-method：调用设置的初始化方法；  
7、BeanPostProcessor:调用BeanPostProcessor的后初始化方法postProcessAfterInitialization；  
8、Bean可以被使用了；  
9、DisposableBean:Bean若实现了DisposableBean接口，则执行其方法destroy;  
10、destroy-method:调用设置的初始化方法   
  
  
**2、后置处理器BeanPostProcessor**  
作用：在spring容器完成bean实例化、配置以及其他初始化方法前后要添加一些自己的逻辑处理。  