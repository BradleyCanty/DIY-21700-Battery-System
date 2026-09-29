# Vehicle Adapter Integration Instructions
1. Use a CNC machine or drill press to cut out the vehicle adapter's mounting holes and wire pass-throughs in the material the vehicle adapter will be mounted on. The following table contains links to the vehicle adapter mounting hole and wire pass-through dimensions for each configuration.

   || 6s | 8s | 10s | 12s |
   | :--- | :--- | :--- | :--- | :--- |
   | 3p | [6s3p](Images/6s3p_vehicle_adapter_dimensions.png) | [8s3p](Images/8s3p_vehicle_adapter_dimensions.png) | [10s3p](Images/10s3p_vehicle_adapter_dimensions.png) | [12s3p](Images/12s3p_vehicle_adapter_dimensions.png) |
   | 4p | [6s4p](Images/6s4p_vehicle_adapter_dimensions.png) | [8s4p](Images/8s4p_vehicle_adapter_dimensions.png) | [10s4p](Images/10s4p_vehicle_adapter_dimensions.png) | [12s4p](Images/12s4p_vehicle_adapter_dimensions.png) |
   | 5p | [6s5p](Images/6s5p_vehicle_adapter_dimensions.png) | [8s5p](Images/8s5p_vehicle_adapter_dimensions.png) | [10s5p](Images/10s5p_vehicle_adapter_dimensions.png) | [12s5p](Images/12s5p_vehicle_adapter_dimensions.png) |
   | 6p | [6s6p](Images/6s6p_vehicle_adapter_dimensions.png) | [8s6p](Images/8s6p_vehicle_adapter_dimensions.png) | [10s6p](Images/10s6p_vehicle_adapter_dimensions.png) | [12s6p](Images/12s6p_vehicle_adapter_dimensions.png) |


   **Note that it is <ins>critically important to check that the battery will fit on your vehicle</ins>:** if the mount hole positions are wider/longer than your vehicle, then either
   
   * select a different battery configuration\
     or...
   * open the CAD file and reposition the mount holes, then 3D print the new vehicle adapter
   
2. Use M3 bolts and either M3 nylock nuts or M3 clinching rivet nuts to bolt down the vehicle adapter to the vehicle

3. Size the 8 AWG wires coming off the vehicle adapter board to the length required for connecting with the vehicle's power system, then solder on the XT90 connectors (female on battery side, male on vehicle side).
