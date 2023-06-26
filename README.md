# binary to bcd
# binary to bcd
```
module pro(b0,b1,b2,b3,b1bar,b2bar,b3bar,d0,d1,d2,d3,d4);
input b0,b1,b2,b3;
output b1bar,b2bar,b3bar,d0,d1,d2,d3,d4;
wire a,b,c,d,e,f;
assign d0=b0;
not(b1bar,b1);
not(b2bar,b2);
not(b3bar,b3);
and(a,b3,b2);
and(b,b3,b1);
and(c,b3bar,b2);
and(d,b2,b1);
and(e,b3,b2,b1bar);
and(f,b3bar,b1);
and(d3,b3,b2bar,b1bar);
or(d1,e,f);
or(d2,c,d);
or(d4,a,b);
endmodule
```
![image](https://github.com/sarveshjustin/digital/assets/113497481/d63faf0a-f7f4-4611-85f7-f8dff0bb7b50)
