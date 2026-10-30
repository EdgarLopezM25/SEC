Authors
MC. Edgar López Molina
Dr. Víctor Manuel Sámano Ortega
Dr. Juan José Martínez Nolasco

Software Requirements
LabVIEW 2019
  MyRIO Toolkit
  FPGA Toolkit
  Real-Time Module
  NI MAX
  NI Package Manager

SEC_LabVIEW
  This folder contain the proyect SEC.lvproj 
  The proyect uses all files and need 2 MyRIO 1900 devices with IPs 172.22.11.2 (micro-Grid) and 172.22.11.10 (Electric Vehicle)
  Inside micro-Grid device found URedRTP.vi (here we can modify properties of ESS and RPVS like Power of PV cells, f (Aging factor), n_p (efficiency of PV converter), Q, nCD (Charge/discharge efficiency of ESS), n(b) (efficiency of ESS PEC) in block diagram view)
  We will need to expand the Chassis, FPGA Target, and Build Specifications windows to Build FPGA target of micro-Grid
  Inside Electric Vehicle device found vehicle.vi (here we can modify nCD of BB in block diagram and NS and NP in front panel)
  We will need to expand the Chassis, FPGA Target, and Build Specifications windows to Build FPGA target of Electric Vehicle
  In MyComputer we will find uRedPC.vi this is the interfaz user-machine
    In front panel we can modify number of PV, number of batteries in ESS and initial SoC, MG voltage, initial SoC of EV BB, %C used to charging process and manage faults in RPVS, MG and Start/Stop charge process

To run the HIL platform is necesary have the two MyRIO 1900 connected, when uRedPC.vi starts an emergent window appear to request irradiance data in xlsx format after it other emergent window appear to request load data in xlsx format.
At present irradiance data is solicite as 235 values in column A starting on row 1 of Excel, because emulation takes irradiance values every 360 seconds
Load data is solicítate as 234 values in column C in column C of Excel
uRedPC.vi is configured to repeat data of irradiance and load when emulation has used all introduced data.
