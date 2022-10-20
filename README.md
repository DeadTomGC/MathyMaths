# MathyMaths

$$V=IR$$

$$ W=I^2 R $$

Typical Li-ion Voltage: $3.7V$ <br/>
Tpyical 18650 Li-ion Capacity: $3.5Ah$  <br/>
Total Energy Capacity: $3.5Ah*3.7V = 12.95Wh$  <br/>
Internal Resistance (IR): $75mOhm$

Lipo cell voltage $3.7V$ <br/>
Assuming the same lipo capacity: $3.5Ah$  <br/>
Total Energy Capacity: $3.5Ah*3.7V = 12.95Wh$  <br/>
Internal Resistance (IR): $3mOhm$

Let's assume a discharge rate of $1A$, giving a power loss of:
$$Wloss_{li-ion} = (1A)^2 * 0.075Ohm = 0.075W$$
$$Wloss_{li-po} = (1A)^2 * 0.003Ohm = 0.003W$$

Run time will be $12.95h$, therefore, total Energy loss is:
$$Eloss_{li-ion} = 12.95h * 0.075W = 0.975Wh$$
$$Eloss_{li-po} = 12.95h * 0.003W = 0.004Wh$$

This translates to a $7.5\\%$ loss for li-ion vs a $0.4\\%$ loss for lipo in total capacity.  Also, this doesn't account for increased resistance and lower efficiency due to heating. <br/>
If we double the current to $2A$, the percentages get worse.  For Li-ion it becomes a $15\\%$ loss and $0.8\\%$ for li-po, approximately. 

In the case of a 10A current pull on 40 (10S,4P) li-ion Cells, with 20Ah capacity, you'd be looking at 2h's of runtime, and those 10 cells in series have a total of 0.75Ohm resistance, but their individual current load is only 2.5A.  

Plugging this in gives us: $$Wloss_{li-ion} = (2.5A)^2 * 0.75Ohm = 4.7W$$ $$Eloss_{li-ion} = 2h * 4.7W = 9.375Wh$$
Multiply this by 4 to get your total lost power since there are 4 banks of cells.  You end up with about $37.5Wh$ lost.
Total capacity of the battery is: $$20Ah * 36V = 720Wh$$  $$\frac{37.5Wh}{720Wh} = 5.2\\%$$ 
So you'll lose at least 5% of that battery pack's capacity due to resistance. The resistance also generates heat, which makes the resistance go up even more. <br/>
If it were a Lipo pack, you'd lose more like 0.3%.  
