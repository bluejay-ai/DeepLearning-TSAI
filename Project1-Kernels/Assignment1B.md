#Kernels

*Q : What are Channels and Kernels (according to EVA)?*
Imagine a abstract painting, full of different colors such as - blue, green, red ,yellow and etc.
If another painter wants to change the blue color to white color, he has to extract the location of blue color and then paint it to white.

The pattern / location of blue color is the channel, Blue color is feature and tool used to extract the blue color pattern from the painting is kernel.

In other words, 
Feature is a unique property of the object.
Channel is a unique container of the feature.
Kernel is a tool used to extract the feature.


*Q : Why should we only (well mostly) use 3x3 Kernels?*
We can use NxN kernels. There are combination of various factors, why 3x3 is extensively used.

1. Computational Exhaustive vs Accuracy
For NxN Kernels, the number of operations needed is N^2(N additions + N Multiplications)
Higher the N, It would be more accurate and computational exhaustive. Hence, we would need tradeoff b/w accuracy and computational power.  
Hence, lower N is preferred. Let's say N = 1,2,3

2. Axis of Symmetry
Odd Kernels have axis of symmetry across horizontal, vertical, diagonal and centre, where as even kernels don't have axis of symmetry. Hence, 2x2 Kernels are not widely used.

3. Neighbouring Information Retention
If we use 1x1 Kernels, no information from neighbouring pixels will be retained. Hence, 1x1 kernels are very local and not a popular choice.

4. Computational Power
Over a period of time, usage of 3x3 kernels has increased. Hence, all the accelators have been optimized to perform the 3x3 Convolution. Since, 3x3 Convolution is faster and optimized, 3x3 kernels are widely used.

*Q : How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations) ?*
z=199;
for (i = 0, z == 1, i++) {
   z = z -2;
   }
print ("Number of 3x3 convolution operations %d", i);
Answer is 99
