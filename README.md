# logback-slf4j-ttl
logback日志框架扩展，支持transmittable-thread-local跨线程传递上下文

# 使用方式
通过设置系统属性"slf4j.provider"，指定SLF4JServiceProvider为“com.github.xsg.TTLLogbackServiceProvider”
### 方式一
-Dslf4j.provider=com.github.xsg.TTLLogbackServiceProvider
越早指定越稳妥，避免被其他线程先触发了org.slf4j.LoggerFactory.bind()的绑定逻辑。
### 方式二
System.setProperty("slf4j.provider", "com.github.xsg.TTLLogbackServiceProvider");
