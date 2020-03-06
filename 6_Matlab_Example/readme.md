# Matlab scripts examples

Following Matlab script is a simple Windows example showing how to communicate with IMU and to acquire ten data frames with Matlab.

```matlab 
% Clear workspace etc.
clear all, close all, clc;
% Open serial port and get handle to related object
% Replace 'COM6' with proper COM port on your computer
serialObject = serial('COM6', 'BaudRate',115200,'DataBits',8, 'Parity', 'none', 'StopBits', 1,...
                      'Terminator', 'LF', 'TimeOut', 10);
% Open port with handle to serial object
fopen(serialObject);
% Read ten frames
for n = 0:9
    % Get current frame and plot it in console
    fgets(serialObject)    
end
% Close serial port
fclose(serialObject);
```

This example is a bit more elaborate. It starts by closing any opened serial port in order to get rid of any connection problem when COM port is not properly closed. Then it accumulates all data frames into a matrix before writing it into a text file.

```matlab
%% Script to read streaming data comming from Sparkfun IMU 9 DOF

% Clear worksapce etc.
clear all, close all, clc;

% Close all possibly opened serial port
serials = instrfind();
for n=1:length(serials)
    fclose(serials(n));
end

% Create serial port
serialObject = serial('COM4', 'BaudRate', 115200, ...
                        'DataBits', 8, 'Parity', 'none', ...
                        'StopBits', 1, 'Terminator',  'LF', 'TimeOut', 10);

% Open serial port
fopen(serialObject);

% Loop to accumulate data
data = [];
for n = 0:9
    % Read data from serial port in string format
    stringValue = fgets(serialObject);
    % Convert string to double vector
    doubleVectorValue = eval(['[',stringValue,']']);
    % Accumulate data in double matrix
    data = [data; doubleVectorValue];
end

% Close serial port
fclose(serialObject);

% Write data in text file
dlmwrite('data.txt', data);
```
