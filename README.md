# signal


---------- Forwarded message ---------
From: SHUBH BAFNA <shubhbafna.ec21@rvce.edu.in>
Date: Mon, 2 Oct 2023, 22:37
Subject: All
To: SIDDHANT SINHA <siddhantsinha.ec21@rvce.edu.in>


def linear convolution(x, h):

M = len(x)

N = len(h) 
result = [0] * (M + N - 1)

for n in range (M + N - 1):

       for k in range(N):

            if n - k >= 0 and n - k < M:

                 result[n] += x[n - k] * h[k]

return result


def cross correlation(x, y):

N = len(x)
result = []

for k in range (N):
correlation sum = 0 
         for n in range (N):
               if n -k >= 0 and n -k < N:
                  correlation sum += x[n-k]* y[n]
            result.append(correlation_sum)
return result


def auto correlation(x):

N = len(x)
result = []

for k in range(N):
             correlation_sum = 0 
               for n in range(N):
                if n-k >= 0 and n - k < N:
               correlation sum += x[n] x[n - k] result.append(correlation_sum)

return result


import

numpy

as np

def circular correlation(x, y):

N = len(x)

result = []

for k in range(N):

correlation_sum 0

for n in range(N):

correlation_sum += x[n] * y[(n + k) % N]

result.append(correlation_sum)

return result



def circular convolution(x, h):

N = len(x) result = [0]*N

for n in range(N):

for k in range(N):

result[n] += x[(n - k) % N] * h[k]

return result

----------------------------------------------------@@@@@@@@@@@@@@@@@@@@@@@-------------------------

EXP - 1
clc; close all;
n=-2:1:2;
y=[zeros(1,2),ones(1,1),zeros(1,2)];
figure(1)
stem(n,y);
xlabel("Time ")
ylabel("Amplitude")
title('unit impulse');

clc; close all;
n=input('enter the n value');
t=0:1:n-1;
y=ones(1,n);
figure(2)
plot(t,y);
title('unit step');
xlabel("Time (sec)")
ylabel("Amplitude")

clc; close all;
n=input('enter the n value');
t=0:n;
y=t;
figure(3)
stem(y,t);
title('unit ramp');
xlabel("Time (sec)")
ylabel("Amplitude")

t1 = sym(linspace(-5,5));
y1 = sinc(t1);
plot(t1,y1)
xlabel("Time (sec)")
ylabel("Amplitude")
title("Sinc Function")

Fs = 60; % sampling freq
t = -.5:1/Fs:.5;
x = 1/(sqrt(2*pi*0.01))*(exp(-t.^2/(2*0.01)));
figure(1);
plot(t,x);
title('Gaussian Pulse Signal');
xlabel('Time (s)');
ylabel('Amplitude');

x = linspace(-2,2);
ranges = abs((1.5).*x.^2 + 5);
ranges(45:55) = 3.5;
angles = linspace(-pi/2,pi/2,numel(ranges));
scan = lidarScan(ranges,angles);
plot(scan)

% create black and white image
clc;% clear command window
close all;% clear all figures
w = ones(64,64);
b = zeros(64,64);
bin1= [w b w b
b w b w
w b w b
b w b w];
bin2 = [w b w b
w b w b
w b w b
w b w b];
subplot(2,2,1);imshow(bin1); title('binary image 1');
subplot(2,2,2);imshow(bin2); title('binary image 2');
imwrite(bin1,'bin_image1.tif');
imwrite(bin2,'bin_image2.tif');
i1 = not(bin1);
i2 = not(bin2);
% for block & white image use subimage
subplot(2,2,3);imshow(i1); title('inverted image 1');
subplot(2,2,4);imshow(i2); title('inverted image 2');
%rgb2gray
clc; % clear command window
close all;% clear all figures
I1=imread('C:\Users\musta\OneDrive\Pictures\1773953.jpg');
figure;
imshow(I1);
title('color image');
I2=rgb2gray(I1);
figure;
imshow(I2);
title('Gray image');

subplot(2,2,1);imshow(I1); title('Color Image');
subplot(2,2,2);imshow(I2); title('Gray Image');
% reading and displaying color image
clc;% clear command window
close all;
a = imread('C:\Users\musta\OneDrive\Pictures\1773953.jpg');
[row, col, dim] = size(a);
figure(1); imshow(a); title('original image');
red = a(:,:,1);% gray scale image of the red plane
green = a(:,:,2);% gray scale image of the green plane
blue = a(:,:,3);% gray scale image of the blue plane
plane = zeros(row,col);
RED = cat(3,red,plane,plane);
GREEN = cat(3,plane,green,plane);
BLUE = cat(3,plane,plane,blue);
figure(3);
subplot(1,3,1);imshow(RED),title('red image');
subplot(1,3,2);imshow(GREEN),title('green image');
subplot(1,3,3);imshow(BLUE),title('blue image');














EXP - 2
t=0:0.01:0.1;
f=25;
t1=2*pi*f*t;
x1=sin(t1);
subplot(3,1,1)
plot(t,x1)
title('x1')
xlabel('Time')
ylabel('Amplitude')
grid on;
x2=cos(t1);
subplot(3,1,2)
plot(t,x2)
title('x2')
xlabel('Time')
ylabel('Amplitude')
y=x1+x2;
subplot(3,1,3)
plot(t,y)
title('Addition of 2 signals y= x1+x2')
xlabel('Time')
ylabel('Amplitude')

t=0:0.01:0.1;
f=25;
t1=2*pi*f*t;
x1=sin(t1);
subplot(3,1,1)
plot(t,x1)
title('x1')
xlabel('Time')
ylabel('Amplitude')
grid on;
x2=cos(t1);
subplot(3,1,2)
grid on;
plot(t,x2)
title('x2')
xlabel('Time')
ylabel('Amplitude')
grid on;
y=x1-x2; % Here the subtraction takes place
subplot(3,1,3)
grid on;
plot(t,y)
title('Subtraction of Signals:y= x1-x2')
xlabel('Time')
ylabel('Amplitude')

t=0:0.01:0.1;
f=25;
t1=2*pi*f*t;
x1=sin(t1);
subplot(3,1,1)
plot(t,x1)
title('x1')
xlabel('Time')
ylabel('Amplitude')
grid on;
x2=cos(t1);
subplot(3,1,2)
plot(t,x2)
title('x2')
xlabel('Time')
ylabel('Amplitude')
grid on;
y=x1.*x2; % Here the multiplication takes place
subplot(3,1,3)
plot(t,y)
title('Multiplication of signals: y= x1*x2')
xlabel('Time')
ylabel('Amplitude')
grid on;

t=0:10;
x=[0 1 2 1 0 1 2 0 1 2 1 ];
subplot(3,1,1)
plot(t,x)
title('Signal')
xlabel('Time')
ylabel('Amplitude')
grid on;
axis([-2 8 0 4]);
subplot(3,1,2)
plot(t+2,x)
title('Right Shift')
xlabel('Time')
ylabel('Amplitude')
grid on;
axis([-2 8 0 4]);
subplot(3,1,3)
plot(t-2,x)
title('Left Shift')
xlabel('Time')
ylabel('Amplitude')
grid on;
axis([-2 8 0 4]);

t=0:0.01:8*pi;
x=sin(t);
subplot(3,1,1)
plot(t,x)
title('Signal')
xlabel('Time')
ylabel('Amplitude')
grid on;
y=sin(t/2);
subplot(3,1,2)
plot(t,y)
title('Expanded Signal')
xlabel('Time')
ylabel('Amplitude')
grid on;
z=sin(t*2);
subplot(3,1,3)
plot(t,z)
title('Compressed Signal')
xlabel('Time')
ylabel('Amplitude')
grid on;

t=0:10;
x=[0 1 2 3 4 -5 -6 -7 -8 -9 -10];
subplot(2,1,1)
stem(t,x)
title('Simple Signal')
xlabel('Time')
ylabel('Amplitude')
grid on;
y=fliplr(x);
subplot(2,1,2)
stem(t,y)
title('Reflected Signal')
xlabel('Time')
ylabel('Amplitude')
grid on;














EXP - 3
Ts=0.01;
t = 0:Ts:1;
x = sin(2*pi*15*t);
subplot(2,2,1)
plot(t,x)
xlabel('Time (seconds)')
ylabel('Amplitude')
title('Sinusoidal signal')
% Fourier Transform of the signal
y = fft(x);
fs = 1/Ts;
f = (0:length(y)-1)*fs/length(y);
n = length(x);
fshift = (-n/2:n/2-1)*(fs/n);
z = fftshift(y);
subplot(2,2,2)
stem(fshift,abs(z))
xlabel('Frequency (Hz)')
ylabel('Magnitude')
title('Magnitude response')
theta = angle(z);
subplot(2,2,3)
stem(f,theta/pi)
xlabel("Frequency (Hz)")
ylabel("Phase /\pi")
title('phase response')
%%FT of rectangular pulse
close all
clc
%fs = 500;
T = 1;
t = -2.5 : 0.1 : 2.5;
x = rectpuls(t,T);
subplot(2,2,1)
plot(t,x,'r','Linewidth',3);
axis([-2.5 2.5 0 1.2])
title({'Rectangular Pulse'})
xlabel({'Time(s)'});
ylabel('Ampltude');
grid
y=fft(x);
subplot(2,2,2)
plot(fftshift(abs(y)))
xlabel('frequency')
ylabel('amplitude')
title('Magnitude response')
theta = angle(y);
subplot(2,2,3)
stem(theta)
xlabel("Frequency (Hz)")
ylabel("Phase / \pi")
title('phase response')
% FT of sawtooth waveform
T = 10*(1/50);
fs = 1000;
t = 0:1/fs:T-1/fs;
x = sawtooth(2*pi*50*t);
subplot(2,2,1)
plot(t,x)
y=fft(x);
subplot(2,2,2)
plot(fftshift(abs(y)))
xlabel('frequency')
ylabel('amplitude')
title('Magnitude response')
theta = angle(y);
subplot(2,2,3)
stem(theta)
xlabel("Frequency (Hz)")
ylabel("Phase / \pi")
title('phase response')















EXP - 4
n=0:1:99;
x=cos(0.48*pi*n)+cos(0.52*pi*n);
% Discrete time signal
% Taking only 10 samples
n1=0:1:9;
x1=x(1:1:10);
y1=fft(x1);
mag_y1=abs(y1);
phase_y1=angle(y1);
figure(1);
subplot(3,1,1);
stem(n1,x1);
xlabel('n--->');
title('Input samples');
subplot(3,1,2);
F=2*pi*n1/10;
stem(F/pi,mag_y1);
xlabel('Frequency in units of Pi');
title('Magnitude plot');
X1=ifft(y1);
subplot(3,1,3);
stem(F/pi,phase_y1);
xlabel('Frequency in units of Pi');
title('phase plot');
n2=0:1:99;
x2=[x(1:1:10) zeros(1,90)];
y2=fft(x2);
mag_y2=abs(y2);
phase_y2=angle(y2);
figure(2);
subplot(3,1,1);
stem(n2,x2);
xlabel('n--->');
title('Input samples');
subplot(3,1,2);
F=2*pi*n2/100;
stem(F/pi,mag_y2);
xlabel('Frequency in units of Pi');
title('Magnitude plot');
X2=ifft(y2);
subplot(3,1,3);
stem(F/pi,phase_y2);
xlabel('Frequency in units of Pi');
title('phase plot');
% 100 samples
n3=0:1:99;
x=cos(0.48*pi*n3)+cos(0.52*pi*n3);
x3=x(1:1:100);
y3=fft(x3);
mag_y3=abs(y3);
phase_y3=angle(y3);
figure(3);
subplot(3,1,1);
stem(n3,x3);
xlabel('n--->');
title('Input samples');
subplot(3,1,2);
F=2*pi*n3/100;
%F1=2*pi*[-50:1:49]/100;
stem(F/pi,mag_y3);
xlabel('Frequency in units of Pi');
title('Magnitude plot');
X3=ifft(y3);
subplot(3,1,3);
stem(F/pi,phase_y3);
xlabel('Frequency in units of Pi');
title('phase plot');















EXP - 5
import numpy as np
h = [1,2,3,3,2,1];
x = [1,2,3,4,5];
y = np.convolve(x,h,mode='full')
print('Linear convolution output y =\n',y)

import numpy as np
h = [1,2,3,4,5];
x = [1,2,1];
N = max(len(x), len(h))
x_padded = np.pad(x,(0, N-len(x)),mode='constant')
h_padded = np.pad(h,(0, N-len(h)),mode='constant')
X = np.fft.fft(x_padded)
H = np.fft.fft(h_padded)
Y = np.fft.ifft(X*H)
print("Circular Convolution Result:", np.real(Y))















EXP - 6
import numpy as np
import matplotlib.pyplot as plt
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]
cross_corr = np.correlate(x,y,mode='full')
print('cross correlation = ',cross_corr)
auto_corr = np.correlate(x, x, mode='full')
print('autocorrelation = ', auto_corr)
lags = np.arange(-len(x) + 1, len(x))
plt.stem(lags, cross_corr)
plt.xlabel('Lag')
plt.ylabel('Cross-Correlation')
plt.title('Cross-Correlation of x and y')
plt.grid(True)
plt.show()
plt.stem(lags, auto_corr)
plt.xlabel('Lag')
plt.ylabel('Auto-Correlation')
plt.title('Auto-Correlation of x')
plt.grid(True)
plt.show()














EXP - 7
import librosa
import librosa.display
import numpy as np
import IPython.display as ipd
import matplotlib.pyplot as plt
ipd.Audio('/content/drive/MyDrive/Colab Notebooks/SUIII.wav')
audio_path = '/content/drive/MyDrive/Colab Notebooks/SUIII.wav'
x,sr = librosa.load(audio_path)

y = len(x)
print(y)
y1 = sr
print(y1)
duration_of_sound = y/y1
print(duration_of_sound,"second")

plt.figure(figsize=(14, 5))
plt.grid(True)
librosa.display.waveshow(x)
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.title("Time Domain Anlysis of Audio file")

X = librosa.stft(x)
Xdb = librosa.amplitude_to_db(abs(X))
plt.figure(figsize=(20, 5))
librosa.display.specshow(Xdb, sr=sr, x_axis='time', y_axis='hz')
plt.colorbar()

mfccs = librosa.feature.mfcc(y=x, sr=sr, n_mfcc=40)
plt.figure(figsize=(10,4))
librosa.display.specshow(mfccs, x_axis="time")
plt.colorbar()
plt.title('MFCC')
plt.tight_layout()
plt.show()

hop_length = 512
S = np.abs(librosa.stft(x))
chroma = librosa.feature.chroma_stft(S=S,sr=sr)
plt.figure(figsize=(15, 5))
librosa.display.specshow(chroma, x_axis='time', y_axis='chroma', hop_length=hop_length, cmap='coolwarm')















EXP - 8
import scipy.io.wavfile as wavfile
import scipy
import scipy.fftpack as fftpk
import numpy as np
from matplotlib import pyplot as plt
s_rate, signal = wavfile.read('/content/drive/MyDrive/Colab Notebooks/SUIII.wav')
FFT = abs(fftpk.fft(signal))
freqs = fftpk.fftfreq(len(FFT), (1.0/s_rate))
plt.plot(freqs[range(len(FFT)//2)], FFT[range(len(FFT)//2)])
plt.xlabel('Frequency (Hz)')
plt.ylabel('Amplitude')
plt.show()

std = np.std(freqs)
mean = np.mean(freqs)
maxv = np.amax(freqs)
minv = np.amin(freqs)
median = np.median(freqs)

skew = scipy.stats.skew(freqs)
kurt = scipy.stats.kurtosis(freqs)
q1 = np.quantile(freqs, 0.25)
q3 = np.quantile(freqs, 0.75)
mode = scipy.stats.mode(freqs)[0][0]
iqr = scipy.stats.iqr(freqs)
print('mean as:', mean)
print('std as:',std)
print('shew as:',skew)
print('kurt as:',kurt)
print('q1 as:',q1)















EXP - 9
Conventional AM in Simulink

Procedure:

Type Simulink in the Matlab Command Window to open a Simulink Library Browser

Go to Signal Processing Blockset-> Signal Processing Sources

. Choose Sine wave as source. Right click on it and select add to untitled. File->save as give file name and save it with .mdl extension For ex: Std_AM.mdl In this experiment Simulink is used to generate a Conventional Amplitude Modulator (Transmitter and receiver). Construct the model as shown in the figure below by searching cach block in a Simulink Library Browser.

Input Parameters:

(a) Sine wave

Frequency: 4 Hz

Amplitude: 1 V Phase offset: 0 radians Computation method: Trigonometric fen

Sample mode: Discrete Output complexity: Real

Sample time: 1/500

Samples per frame: 1

(b) Constant Constant value: 1

(c) Sine wavel

Amplitude: 1 V

Frequency: 50 Hz

Phase offset: 0 radians

Sample mode: Discrete Output complexity: Real

Computation method: Trigonometric fen

Sample time: 1/5000

Samples per frame: 1

(d) Add

List of signs: ++

(e) Product and Product!

Number of inputs: 2

(f) Analog Filter Design

Design method: Butterworth

Filter type: Lowpass Passband edge frequency (rad/s): 2*3.142*8

Filter order: 20

(g) Analog Filter Designl

Design method: Butterworth

Filter type: Bandpass

Filter order: 20 Lower passband edge frequency (rad/s): 2*3.142*2

Upper passband edge frequency (rad/s): 2*3.142*8

(b) Scope

Go to Settings, then click on History and Uncheck the limit data points to last Run time: 4sec
