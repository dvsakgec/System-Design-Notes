## Basic steps to handle flash sale are following:

  1. Plan for flash sale in advance including the load prediction
  2. Test the systems for scale in advance, including when things could go wrong
  3. Monitoring systems to keep track of load and health of system


Core problems in Flash sale design:
------

1. Scaling the writes
2. Serialisation of customer checkout requests
3. In Flash sale, requests go through the roof in matter of minutes and then suddenly come down drastically so over provision and under provision of resources and provisioning it much earlier will cost a lot probably even costlier than gains in the sale
4. Blocking invalid requests, Hackers can attack your system to break it down during sale as it already under stress
5. Inventory updates when user checksout products at minimum 20K/sec ( Redis can help with that)
  
  
## Below are the links which could be useful

  0. [***Video:*** Flash Sale System design](https://www.youtube.com/watch?v=dlV7l_VqCXk)
  1. [shopify scale for flash sale](http://highscalability.com/blog/2015/11/2/how-shopify-scales-to-handle-flash-sales-from-kanye-west-and.html), [***Video:*** ](https://www.youtube.com/watch?v=-I4tIudkArY)
  2. [How Amazon planned for flash sale](https://images-na.ssl-images-amazon.com/images/I/B2NSQ66nKkS.pdf)
  3. [***CDN optimisation:*** research Paper for Flash Sales](https://www.akamai.com/us/en/multimedia/documents/white-paper/handling-flash-sales-devops-strategies-for-traffic-mitigation-whitepaper.pdf)
  4. **IMPT** [Hackernoon:design system for flash sale](https://hackernoon.com/developing-a-flash-sale-system-7481f6ede0a3)
  5. [Alibaba](https://www.alibabacloud.com/help/doc-detail/63920.htm) 
  6. [***Video:*** Use Redis for running flash sales]
