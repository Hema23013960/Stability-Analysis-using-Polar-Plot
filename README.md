# Stability-Analysis-using-Polar-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=10/(S(1+0.5S)(1+0.2S)) using polar plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![WhatsApp Image 2025-11-28 at 06 29 00_b50272e8](https://github.com/user-attachments/assets/e106c6d3-d056-4e7d-a236-e568d5c2f3f9)

![WhatsApp Image 2025-11-28 at 06 26 11_2f0ff8d7](https://github.com/user-attachments/assets/45bbc33c-5438-4c91-9fe0-2c7dea0e2fd7)
![WhatsApp Image 2025-11-28 at 06 27 13_68ea1fbf](https://github.com/user-attachments/assets/cd262d0f-2fe1-4903-bd37-5f73886b157b)
![WhatsApp Image 2025-11-28 at 06 26 58_778592b3](https://github.com/user-attachments/assets/fb7e9d4c-f7b9-4889-b5db-5ecccba3112f)





## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
num=[10]
den=[0.1 0.7 1 0]
sys=tf(num,den)
[mag,phase,W]=bode(sys)
mag=squeeze(mag)
phase=squeeze(phase)
phase1=deg2rad(phase)
polarplot(phase1,mag,'linewidth',1.5)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end

## Output:
<img width="713" height="640" alt="image" src="https://github.com/user-attachments/assets/553f46ab-e0c0-4a22-acdd-fb0a92db6049" />

## Result:
Thus the polar plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin =0.7 <br>
Phase Margin = -8.8865<br>
Gain crossover frequency = 3.7565<br>
Phase crossover frequency = 3.1623<br>
The system is unstable.
