# AWS.SQS.NET
This repository demonstrates how to integrate Amazon SQS (Simple Queue Service) with .NET applications. It includes examples for sending, receiving, and deleting messages from queues

# Summary

- [AWS.SQS.NET](#awssqsnet)
- [SQS](#sqs)
  - [Types of Queues](#types-of-queues)
  - [Create Queue](#create-queue)
- [Application](#application)
  - [Producer](#producer)
  - [Consumer](#consumer)
- [Queue on AWS Console](#queu-on-aws-console)
- [References](#references)




# SQS

![image](https://github.com/user-attachments/assets/fc5838a7-c1fb-494e-8356-f30bbc5f103f)

-----

## Types of Queues
Amazon SQS provides two types of queues based on your requirements.

- **Standard Queues**
- **FIFO Queues**

**Standard Queues** are the first type that was released initially. In systems where the order of processing messages is not important, standard queues can be used. When there are multiple messages in the standard queue, it tries to push them out in order, but the maintenance of the order is not guaranteed. So when the published puts messages 1,2,3,4,5 into this queue, the consumer may get the messages in order 3,2,4,1,5. There is also another limitation that there can be duplicate messages within the queue. But the throughput of such queues is quite high, almost unlimited.

**First In First Out** queues ensures that the messages are processed in sequence. And it’s also guaranteed that each message appears only once in the queue. As a limitation, there is slightly reduced throughput. FIFO queues support up to 300 messages per second. You can chain this with batches. When you batch 10 messages per request, the queue will now support almost 300*10 messages per second, which is again quite massive.

## Create Queue
![image](https://github.com/user-attachments/assets/7bf830da-540f-44e2-9a74-0eabf09d534d)

----

![image](https://github.com/user-attachments/assets/1ea07d43-8504-491e-8972-bcfae70232a5)


------

# Application
![image](https://github.com/user-attachments/assets/13bdf05f-5071-4a32-93fe-f37ad1d28949)

----

## Producer
![image](https://github.com/user-attachments/assets/18f62cba-5e02-41c8-a581-3937fe8e150b)
----



### Queu on AWS Console
![image](https://github.com/user-attachments/assets/66dbf1da-e3d9-46f5-ab92-abae2f048510)

----

![image](https://github.com/user-attachments/assets/ba27f642-d90c-4c11-9db3-557f821c84ee)

----
![image](https://github.com/user-attachments/assets/86e6fbbf-bda1-4116-b031-5e0e3bec7058)


----

![image](https://github.com/user-attachments/assets/42c292ed-41ea-40b1-af6f-9de8bc7e6cfd)


-------

### Consumer
![image](https://github.com/user-attachments/assets/9eca2752-50ab-4a5b-b08d-117cf1a0eefa)



## References
https://codewithmukesh.com/blog/amazon-sqs-and-aspnet-core/
