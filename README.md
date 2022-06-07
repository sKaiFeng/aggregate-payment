# aggregate-payment

With the prevalence of mobile payment, commercial banks, third-party payment companies, other clearing institutions, consumer finance companies and many other types of institutions are providing online (mobile) payment solutions for merchants. On the other hand, users have a wide range of payment needs, and the payment channels have been "fragmented", and the degree of "fragmentation" will gradually deepen. As the name suggests, aggregate payment is to integrate the current mainstream payment to form an aggregate channel for third-party payment, also known as "the fourth party payment".



### The following figure shows the industrial structure of aggregate payment:

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200807174552351.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDk1MDk4Nw==,size_16,color_FFFFFF,t_70)

Aggregate payment does not carry out fund clearing, so it does not need a payment license. It only completes the information flow in the payment process and the carrier of merchant operations. On the basis of collecting mainstream payment methods such as UnionPay, Alipay and wechat, it helps merchants reduce access costs and improve operation efficiency. It is neutral, flexible and convenient.



### The following figure shows the merchant completing the payment business through the aggregate payment platform:

![在这里插入图片描述](https://img-blog.csdnimg.cn/2020080717463898.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDk1MDk4Nw==,size_16,color_FFFFFF,t_70)

**Functional **

The functional module platform of the project mainly includes three modules: Official Website & open platform, merchant platform and operation platform. The detailed functions are as follows:

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200807174701961.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDk1MDk4Nw==,size_16,color_FFFFFF,t_70)



### What technical framework is adopted for the project?

The current popular front-end and back-end separation architecture is adopted for the development of flash mob payment, which is composed of user layer, UI layer, micro service layer, data layer and other parts to provide services for PC, H5 and other client users. The following figure shows the technical architecture of the system:

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200807175154998.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDk1MDk4Nw==,size_16,color_FFFFFF,t_70)



Business process example:

1. Users can access flash pay through PC, mobile phone and other clients.
2. The system uses CDN technology to schedule and access some pictures, CSS, videos and other resources from CDN.
3. All requests go through the load balancer.
4. First request the UI layer to render the user interface
5. The merchant registers and authenticates the enterprise through the platform. The UI layer requests the service layer through the gateway. After the service layer completes the business processing, the data is persisted to the data layer.
6. The platform operator reviews the merchant information, and the system execution process is consistent with the merchant registration process. The UI layer requests the service layer for business processing, and the service layer persistence the data to the database through the data layer.



### The project technology stack is as follows:

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200807180227983.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDk1MDk4Nw==,size_16,color_FFFFFF,t_70)

The payment service end of Shanju is built based on spring boot and adopts spring cloud Alibaba microservice architecture.

