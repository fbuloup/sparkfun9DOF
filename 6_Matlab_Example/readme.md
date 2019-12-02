# Un exemple de script sous Matlab

Le script Matlab ci-dessous est un exemple simple, sous Windows, qui montre comment communiquer avec le module et lire dix trames de données.

```matlab 
% Clear workspace etc.
clear all, close all, clc;
% Open serial port and get handle to related object
% Replace 'COM6' with proper COM port on your computer (Cf. "Gestionnaire de Périphériques")
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
