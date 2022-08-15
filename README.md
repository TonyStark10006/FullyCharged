# FullyCharged

requirement: >= macOS 11

a simple client to display battery quantity for hackintosh(seems macintosh never need this), which based on CurrentCapacity & MaxCapacity from IOReg.

this app equals to result below (result = CurrentCapacity / MaxCapacity)

```
ioreg -l | awk '$3~/Capacity/{c[$3]=$5}END{OFMT="%.3f";max=c["\"MaxCapacity\""];print(max>0?100*c["\"CurrentCapacity\""]/max:"?")}'
```

screenshot:

![image](https://github.com/TonyStark10006/FullyCharged/raw/master/screenshot.jpg)
