# print(f) to Pay Respects

Category : Binary/Executable

Points : 100

## Description

Lulu recently began to collect rice granules, she needs so many! (like over 9999) Jake says it might be a cure to Lulu's disease. Go help her get enough by throwing rice at the portal, print(f) to pay respects.

## Hint

Careful not to throw rice in the wrong direction, just thow it close by (not into) the portal - Jake can pick it up later.

## Solving

This challenge, thanks to the beauty that is .net, the challenge's Portal.exe can't be executed. But that doesn't really matter, we should
do fine without it. We could use IDA as always to reverse engineering, but this time it will not bring us very far, so let's use a specialized tool.
We'll use dnSpy, that is specialized in .net executables and dlls.

So let's open up dnSpy and see what we got :

![image](https://user-images.githubusercontent.com/57148042/73195685-9443e500-412e-11ea-9733-d80782671534.png)

We could take some time looking at Portal.exe, but what we are interested in is in Portal.dll. We just need to explore it a little :

![image](https://user-images.githubusercontent.com/57148042/73195869-e5ec6f80-412e-11ea-9ddd-e33e6031a323.png)

flag : rtcp{s0m3t1m35_0n1y_s0m3tImEz_sn^k3z_ar3_u5EfuL}
