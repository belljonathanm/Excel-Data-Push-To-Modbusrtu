# Excel-Data-Push-To-Modbusrtu
This code will enable pushing modbus rtu commands over serial communications from an excel data set to update a controller on a regular basis

Many industrial processes use the Modbus RTU serial communication over an RS485 network to poll different devices, update settings, and
monitor processes.

This code is meant to facilitate changing the device setpoint to match historical setpoints (specifically temperature and humidity settings) from an excel file to the device(s) controlling the setpoints.

Items to do:
Create an excel sheet format that works smoothly with the code (this is essentially complete, but changes to how the data is arranged or entered
may be needed to facilitate the transfer)

Create code that will take the needed data (time sensitive) from the available data set and output the change over the serial port in the
correct format for the temperature and humidity controllers.

  Pull data from the spreadsheet
  
  Compile that data into a coherent string for sending through the serial connection
    Check Modbus communication data sheet from FDC to get correct format for the data
  
  Open the port and send the data
    Possibly check the returning data to ensure the message what sent and received correctly and if not resend the data/set an error
  
  Close the port and wait for the next time to send the update
  
