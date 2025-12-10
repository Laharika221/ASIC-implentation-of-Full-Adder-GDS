📘 Complete Full Adder – RTL to GDSII Flow Report
-------------------------------------------
### 🧩 1. RTL Design

We began the flow by writing the Verilog RTL for a 1-bit Full Adder using basic logic equations. The design was kept simple and synthesizable for smooth downstream processing.

below is the code :

```
module full_adder (
    input a, b, cin,
    output sum, cout
);
    assign sum = a ^ b ^ cin;
    assign cout = (a & b) | (b & cin) | (cin & a);
endmodule
```
