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
### 🧪 2. Functional Simulation

The RTL was simulated using a testbench that verified all 8 input combinations. Waveform and print outputs confirmed correct Sum and Carry functionality.

----------------------

<img width="320" height="441" alt="image" src="https://github.com/user-attachments/assets/219ab179-ba32-4627-a142-d3a926323508" />

--------

<img width="603" height="357" alt="image" src="https://github.com/user-attachments/assets/2a8bb63b-d4a1-4792-8195-e74020644eeb" />


### ⚙️ 3. Logic Synthesis (Design Compiler)

The RTL was synthesized using Synopsys Design Compiler. Technology mapping, area optimization, and timing checks were performed. A gate-level netlist, reports, and SDC files were generated.

-------------------------

### 🧱 4. Floorplanning (ICC)

Core boundary, aspect ratio, and utilization were defined. IO placement and macro positioning (if any) were set. A clean layout structure was established for the physical flow.

 ----------------------------
 
