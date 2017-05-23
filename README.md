# VBAcmd
FSM-based control software for Virtual Burrow Assay

Runs on Windows 7 Professional, Python 2.7.5 (WinPython distribution)

Instructions:
  - Rename VBAconfig.py.template to VBAconfig.py 
  - If necessary correct DAQ and scaling parameters in the new VBAconfig.py file (git pull will not overwrite your local VBAconfig.py file)
  - Run VBAcmd3.pyw

Requires:
  - Virtual Burrow Assay (see [CAD](https://github.com/goatsofnaxos/VBAcmd/tree/master/CAD) folder for frictionless rail design; requisite electronics parts listed below)
  - National Instruments card with analog and digital in/out (e.g.  [USB-6008](http://sine.ni.com/nips/cds/view/p/lang/en/nid/201986)). Default configuration in VBAconfig.py.template:
    - dev5:ai0 laser sensor   (scaling for MICRO-EPSILON ILD1302-50)
    - dev5:ai1 force sensor   (scaling for FUTEK FSH02664 load cell with FUTEK QSH00602 signal conditioner, +/-5 VDC output range)
    - dev5:ai2 servo position (scaling for FIRGELLI L12-50-50-12-I)
    - dev5:ai3 optional analog in (no scaling)
    - dev5:ao0 servo control  (scaling for FIRGELLI L12-50-50-12-I)
    - dev5/port0/line0 logical in to disable closed loop mode during trial / enable closed loop mode during ITI
    - dev5/port1/line0 logical out to indicate conditions satisfied for trial initiation
  - NI-DAQmx available at http://www.ni.com/getting-started/install-software/data-acquisition
  - PyDAQmx available at https://pythonhosted.org/PyDAQmx/
  - PyQt4 available at https://www.riverbankcomputing.com/software/pyqt/download
  - transitions available at https://github.com/tyarkoni/transitions
  - ParamLoad and Scaling available at https://github.com/goatsofnaxos/lib  

We are not software engineers. This is likely to be buggy, inefficient and recalcitrant to distribution across different platforms--and so welcome any assistance.

![alt tag](https://raw.githubusercontent.com/goatsofnaxos/VBAcmd/master/screengrab.png)
![alt tag](https://raw.githubusercontent.com/goatsofnaxos/VBAcmd/master/FSM.png)


![alt tag](https://raw.githubusercontent.com/goatsofnaxos/VBAcmd/master/ezgif-3-2a09ccfc0f.gif)
