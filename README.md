# Split the Bill

This Split the Bill project is used for equally splitting multiple bills into individual person. The input is a CSV format of Cost,Description,Pipe-delimited list of names. The output is a list of names along with their corresponding share of the bills. All calculations are done locally by the browser. The server doesn't receive any information about the bill.

For example, supposed we have 2 bills:
* 1st bill is for $150.15 at a bar and the people involved are Joe, Donald, and Barack.
* 2nd bill is for $120.12 at a mexican restaurant and the people involved are Joe, Barack, and George.

The example above would have this input:
```
150.15,a bar,Joe|Donald|Barack
120.12,mexican restaurant,Joe|Barack|George
```

When the Split the bill button is clicked, the following output is expected:
|Name|Share|
|----|-----|
|Joe|$ 90.09|
|Donald|$ 50.05|
|Barack|$ 90.09|
|George|$ 40.04|

Here's the math:
* $150.15 is split evenly among Joe, Donald, and Barack at $50.05 each.
* $120.12 is split evenly among Joe, Barack, and George at $40.04 each.
* Joe's share of the bills is $50.05 + $40.04 = $90.09.
* Donald's share of the bills is $50.05.
* Barack's share of the bills is $50.05 + $40.04 = $90.09.
* George's share of the bills is $40.04.
