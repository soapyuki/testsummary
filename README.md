# 一次面试(13k-18k已拿到Offer的人)过程记录

## 初面

## 基本介绍
> 您好，我是xx，做测试有两年/三年/x年的时间，主要的经验是电商和金融/银行/后台管理类系统，比较擅长的是质量保障/接口自动化/APP自动化 ，了解简单的自我介绍，这是我的一个简单的自我介绍，您看还有什么需要补充的吗？

## 面试初面问题
- 1. 白盒测试和黑盒测试有什么区别？
>白盒测试的话会关注代码方面的，然后黑盒测试的话，不会关注内部实现的逻辑

### 根据上述问题展开的接下来的面试问题
  + 1.1 那你一般是怎么编写这个测试用例？
  > 您指的是功能的测试用例还是接口自动化的？
  
  + 1.2 你先说功能的吧
  > 我主要是场景法用的比较多一些，然后回去分析一些业务的特性，还有一些异常的场景
  
  + 1.3 接口这块呢？
  > 接口自动化的话，我主要是去写一些覆盖一些核心的流程，比如说营销活动这一块，还有退款的审核，大概覆盖了核心业务的50%

- 2. 那你觉得Web测试和APP测试有哪些区别？
>APP测试的话可能会更多的关注一些比如说中断测试、弱网测试、流量测试、电量的一些测试这个都可以用adb命令来进行测试

	+ 根据上述问题展开的接下来的面试问题？
	+ 2.1 那iOS测试你没有做过吗？只做过Android的吗？
	>呃，都做过
	+ 2.2 那iOS测试和Android测试有什么区别？
	> Android的话，可能就是会在兼容性上面考虑的要多一些，因为Android的话，它的那个手机机型比较多；iOS的话，iOS主要是不同系统版本进行测试

- 根据1和2问题展开的接下来的题目
- 3. 那你之前的接口测试的流程说一下吧？
>接口测试流程主要是根据开发提供的那个接口文档，然后我用postman来进行测试。主要关注点一个是业务方面，比如开发那边新增加的数据库字段或者是删除的数据库字段，对相关联接口的影响；另外一个关注点是数据量比较大的时候，前端的表示层的表现
>再有就是一些性能测试

- 4.  那你个人觉得自动化测试和手工测试有什么本质上的区别？
>自动化测试的话，其实它主要是放在就是回归，回归测试这一步，但是它没有办法，就是说去发现一些异常的情况。
>因为可能手工测试有的时候发现一些bug,可能用例当中没有写到，属于探索性测试过程当中发生了一些异常的问题，所以自动化测试的话，我一般是放在回归的流程，使用JenKins做持续集成，然后自动化的话，主要是去写一些核心的一些流程，没有说去写一些很细节的东西

- 5. 那一般的话，你测试的时候，一些测试数据你是怎么去准备的？
>测试数据的话，我是自己有写过一个小工具，就是一个数据工厂，用来准备测试的一些数据。
>比如说，有的时候性能测试可能需要准备比较大量的一些数据，那我可以用数据工厂去完成。因为我们有一些业务，可能需要去统计一些用户的一些情况，比如这个用户在一个月内下的单有多少，近半年内下的单有多少，这样的一些数据。因为我们的测试环境可能之前是没有这样的数据的，这个时候可以用数据工厂去生成一些自己需要的数据。
>

- 6. 那你的压测相关的有没有接触过？
>有接触过，最近又一些性能测试，因为疫情等关系，最近性能测试做过一些 

	+ 6.1  压测报告你能出吗？
  	>可以出
	
	+ 6.2 那你说下压测的一些基本步骤？流程是怎么样的？你是怎么测的？
  	>首先的话，我会分析一下这个业务，还有一些用户相关的数据，比如说我们会进行一个线上的监控，可能我们的用户会有多少，然后大概并发的用户占百分之多少，这个时候我再去分析一下这个性能测试需要达到多少TPS的并发，然后用Jmeter进行测试，然后自己搭建一个监控用influxDB+grafana，主要是关注TPS响应时间，然后再配合运维这边CPU和DB的一些监控
	
	+ 6.3 那压测报告上的一些参数指标呢？哪些指标是需要体现出来的？作为一个性能指标的一个考核，你觉得有哪些参数？
	>我觉得最主要关注的是TPS和响应时间，这两块我是会结合监控的图去做一个分析，比如TPS是到了多少的时候会出现一个瓶颈不再上升，那这个时候可能是一个瓶颈的地方 ，或者是有的时候会控制库存超卖的情况，加入一些锁，可能这个时候会响应时间比较久一些，所以响应时间和TPS这两块是我比较注重的


