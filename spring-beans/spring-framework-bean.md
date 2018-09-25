1. Qualifier
	* 直接@Qualifier("beanName")等价于@Resource(name="beanName")
	* @Qualifier直接注解在其他的注解上，然后在Bean定义上添加qualifier，也可以添加更多的属性，精确匹配
	* https://blog.csdn.net/lovin_fang/article/details/78537547
	* 实践: @Qulifier和@Bean一起使用是否可以?


git fetch
git checkout -b develop --track origin/develop