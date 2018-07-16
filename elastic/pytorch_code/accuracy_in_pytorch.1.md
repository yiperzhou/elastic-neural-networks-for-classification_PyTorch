# Accuracy in Pytorch  

# classification on **CIFAR-10**

model                                                                     | error (best)             
--------------------------------------------------------------------------| ------------------- 
ResNet-18-imagenet-include-pretrain                                       | 7.6900
ResNet-18-imagenet-No-include-pretrain                                    | 6.1000 
Elastic_ResNet-18-imagenet-include-pretrain-skip-last-interCLF            | 12.0300
Elastic_ResNet-18-imagenet-include-pretrain-No-skip-last-interCLF         | 10.8900 [1] 
Elastic_ResNet-18-imagenet-No-include-pretrain-No-skip-last-interCLF      | 8.4800 
                    ----------------                                      | --------------------  
ResNet-34-imagenet-No-include-pretrain                                    | 4.9100
Elastic_ResNet-34-imagenet-No-include-pretrain                            | 11.0700 
                    ----------------                                      | --------------------  
ResNet-50-No-include-pretrain                                             | 5.0700  
Elastic_ResNet-50-No-include-pretrain                                     | 9.1000  

ResNet-101-include-pretrain-skip-last-interCLF                            | 8.5900
Elastic_ResNet-101-include-pretrain-skip-last-interCLF                    | 10.4900

reference  
**pretrain** means using 10 epochs to train classifier first
*[1] second to last classifier gets better result than the last classifier

暂时的结论：
在ResNet18-No-include-pretrain 中，精确度会比 ResNet18-include-pretrain 中会高 1%, 这个在
Elastic_ResNet-18-include-pretrain-No-skip-last-interCLF 和 Elastic_ResNet-18-No-include-pretrain-No-skip-last-interCLF 也发生了，即高 2%


# classification on **CIFAR-100**

model                                                                     | error (best)              
--------------------------------------------------------------------------| ------------------- 
ResNet-18-No-include-pretrain                                             | 25.1800  
Elastic_ResNet-18-No-include-pretrain                                     | 30.9500 

ResNet-34-imagenet-No-include-pretrain                                    | 22.4600 
Elastic_ResNet-34-imagenet-No-include-pretrain                            | 33.1300  
ResNet-34-imagenet-include-pretrain                                       | 23.2600 
Elastic_ResNet-34-imagenet-include-pretrain                               | 34.6900   

ResNet-50-No-include-pretrain                                             | 23.6600   
Elastic_ResNet-50-No-include-pretrain                                     | 29.1100 

ResNet-101-include-pretrain                                               | 22.3300   
Elastic_ResNet-101-include-pretrain                                       | 38.1000  

