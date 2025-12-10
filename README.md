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

<img width="603" height="357" alt="image" src="https://github.com/user-attachments/assets/2a8bb63b-d4a1-4792-8195-e74020644eeb" />


### ⚙️ 3. Logic Synthesis (Design Compiler)

The RTL was synthesized using Synopsys Design Compiler. Technology mapping, area optimization, and timing checks were performed. A gate-level netlist, reports, and SDC files were generated.

-------------------------

### 🧱 4. Floorplanning (ICC)

Core boundary, aspect ratio, and utilization were defined. IO placement and macro positioning (if any) were set. A clean layout structure was established for the physical flow.

 ----------------------------
 
### 🔌 5. Power Planning

Power rings and power rails were inserted across the chip. VDD/VSS stripes were generated to ensure uniform IR drop and stable power delivery.

-----------------------------------------

### 📍 6. Placement

Standard cells were placed using ICC optimization. Placement ensured minimal wirelength, low congestion, and improved timing quality.

-----------------------

### 🕒 7. Clock Tree Synthesis (CTS)

A balanced clock tree was inserted with buffers and inverters. Clock skew and insertion delay were optimized to meet timing constraints.

---------------------------
### 🔀 8. Routing

Global and detailed routing were performed. All nets were routed with minimum DRC violations. Routing optimization ensured clean timing and signal integrity.

-------------------

### 🧼 10. Physical Verification (DRC/LVS)

The routed layout underwent DRC and LVS checks. All rule violations were resolved to ensure the design matches the schematic and follows fabrication rules.

---------------------

### 🧾 11. Sign-Off Analysis

The final design was run through sign-off timing, power, antenna checks, and geometry verification. All reports passed the required criteria.

----------------------

### 🟦 12. GDSII Generation

A clean GDSII file was generated for tape-out. This represents the final manufacturable layout of the Full Adder.

-------------------

<img width="603" height="357" alt="image" src="https://github.com/user-attachments/assets/ef6d248d-e25f-4d7c-80eb-d8116c2371a9" />

<img width="687" height="423" alt="image" src="https://github.com/user-attachments/assets/0a655460-e29b-49ab-a31a-5b261e0eeca9" />

<img width="853" height="338" alt="image" src="https://github.com/user-attachments/assets/32a34051-6db3-4e84-b546-63169b57b057" />

<img width="830" height="323" alt="image" src="https://github.com/user-attachments/assets/cd7f4cea-8395-4410-af89-07ddec3c3c2d" />

### 🏁 Conclusion

This project successfully completed the entire RTL to GDSII ASIC flow for a 1-bit Full Adder.
The hands-on experience involved RTL coding, simulation, synthesis, floorplanning, power planning, placement, CTS, routing, physical verification, ECO fixes, and final GDSII export.
This flow gave deep insight into how digital logic transforms into an optimized physical chip layout suitable for fabrication.

------------

I’m sincerely thankful and grateful to  Kanika Mam and Srujan Sir from VLSI Expert for their continuous guidance, detailed explanations, and valuable support throughout this learning journey.
