# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:

Stability analysis using a Bode plot in MATLAB evaluates a system’s frequency response to determine its gain margin and phase margin. A system is stable when these margins are positive, indicating adequate separation from the instability point.
![WhatsApp Image 2025-11-18 at 11 52 55_d67cb7f5](https://github.com/user-attachments/assets/d9b8be15-241c-466f-81b0-0050f83db830)

![WhatsApp Image 2025-11-18 at 14 45 50_0ce8ce2d](https://github.com/user-attachments/assets/8cdf8e56-6ddc-4722-8ad8-ec7f6c578ad2)


![WhatsApp Image 2025-11-18 at 11 59 04_ca82f8f3](https://github.com/user-attachments/assets/9deab8f0-9d2e-4982-b332-e61202fdc52b)





## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```
## Output:

<img width="1771" height="881" alt="image" src="https://github.com/user-attachments/assets/bcd4982a-7c0c-46f0-a33b-238e531e013e" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12<br>
Phase Margin = 60.4231<br>
Gain crossover frequency = 0.9070<br>
Phase crossover frequency = 4.4721<br>
The system is stable
