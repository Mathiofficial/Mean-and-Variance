#  Mean and variance of a discrete  distribution


# Aim : 

To find mean and variance of arrival of objects from the feeder using probability distribution


# Software required :  

Python and Visual components tool

# Theory:

The expectation or the mean of a discrete random variable is a weighted average of all possible
values of the random variable. The weights are the probabilities associated with the corresponding values. 
It is calculated as,

![image](https://user-images.githubusercontent.com/103921593/192938463-e34177f4-f188-48a0-bda2-8f6d1d660ed2.png)

The variance of a random variable shows the variability or the scatterings of the random variables.
It shows the distance of a random variable from its mean. It is calcualted as

![image](https://user-images.githubusercontent.com/103921593/192938695-99fedc01-34d5-4d36-84df-5880e766ed0c.png)


# Procedure :

1. Construct frequency distribution for the data

2. Find the  probability distribution from frequency distribution.

3. Calculate mean using 
   
   ![image](https://user-images.githubusercontent.com/103921593/192940431-03b81777-c54d-4286-b4f4-82dfe7666b4c.png)

4. Find  
   
      ![image](https://user-images.githubusercontent.com/103921593/192940255-2d9dd746-6875-4a6d-877b-6da6cdb96ab1.png)

5.  Calculate variance using 
  
      ![image](https://user-images.githubusercontent.com/103921593/192942852-913550a9-fabe-4a55-b956-0487b18bbd97.png)


# Experiment :

![204071203-75e5396f-7b27-4d10-8d94-29501c6c2839](https://user-images.githubusercontent.com/118787327/229995892-fe138204-bd38-4fec-b1d5-c3736eafa208.png)


# Program :
```
import numpy as np
L=[int(i) for i in input().split()]
N=len(L);M=max(L)
x=list();f=list()
for i in range(M+1):
  c=0
  for j in range(N):
    if L[j]==i:
      c=c+1
  f.append(c)
  x.append(i)
sf=np.sum(f)
p=list()
for i in range(M+1):
  p.append(f[i]/sf)
mean = np.inner(x,p)
EX2=np.inner(np.square(x),p)
var=EX2-mean**2
SD=np.sqrt(var)
print("The Mean arrival rate is %.3f"%mean)
print("The Variance of arrival from feeder is %.3f"%var)
print("The Standard deviation of arrival from feeder is %.3f"%SD)

```
# Output : 
![f3cde1e5-18bc-40f7-b043-e051aacf71a5](https://user-images.githubusercontent.com/118787327/230277869-03bc88c2-f9f5-4825-af15-1618aa18d07f.jpg)

# Results :
The mean and variance of arrivals of objects from feeder using probability distribution is calculated.

