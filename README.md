# Experiment-08- Encoders-and-decoders 
### AIM: To implement 8 to 3 Encoder and  3to8 Decoder using verilog and validate its outputs
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## Encoders
Binary code of N digits can be used to store 2N distinct elements of coded information. This is what encoders and decoders are used for. Encoders convert 2N lines of input into a code of N bits and Decoders decode the N bits into 2N lines.

1. Encoders –
An encoder is a combinational circuit that converts binary information in the form of a 2N input lines into N output lines, which represent N bit code for the input. For simple encoders, it is assumed that only one input line is active at a time.

As an example, let’s consider Octal to Binary encoder. As shown in the following figure, an octal-to-binary encoder takes 8 input lines and generates 3 output lines.

![image](https://user-images.githubusercontent.com/36288975/171543588-bc0746df-a173-4b35-989e-5fb7d385fe8a.png)
## Figure -01 3 to 8 Encoder 


Implementation –

X = D4 + D5 + D6 + D7
Y = D2 +D3 + D6 + D7
Z = D1 + D3 + D5 + D7 
Hence, the encoder can be realised with OR gates as follows:


![image](https://user-images.githubusercontent.com/36288975/171543740-68403b82-aa93-4c98-9343-f32b14885a2e.png)
## Figure -02 3 to 8 Encoder implenentation 

 ### Decoders 
A decoder does the opposite job of an encoder. It is a combinational circuit that converts n lines of input into 2n lines of output.

Let’s take an example of 3-to-8 line decoder.
Implementation –
D0 is high when X = 0, Y = 0 and Z = 0. Hence,

D0 = X’ Y’ Z’ 
Similarly,

D1 = X’ Y’ Z
D2 = X’ Y Z’
D3 = X’ Y Z
D4 = X Y’ Z’
D5 = X Y’ Z
D6 = X Y Z’
D7 = X Y Z 


![image](https://user-images.githubusercontent.com/36288975/171543978-ee2d0671-2846-40a1-8705-507fd6287a49.png)
## Figure -03 8 to 3 Decoder 



![image](https://user-images.githubusercontent.com/36288975/171543866-5a6eace6-8683-49d7-9c4f-a7cb30ec3035.png)
## Figure -04 8 to 3 Decoder implementation 

### Procedure




### PROGRAM 

Program for Endocers and Decoders  and verify its truth table in quartus using Verilog programming.

Developed by: YUVASRI.K

RegisterNumber:  212222050061

ENCODER

module EX8(a,b,c,d0,d1,d2d3,d4,d5,d6,d7);

output a,b,c; 

input d0,d1,d2,d3,d4,d5,d6,d7;

or(a,d4,d5,d6,d7);


or(b,d2,d3,d6,d7);

or(c,d1,d3,d5,d7);

endmodule

DECODER

module EX8(d0,d1,d2,d3,d4,d5,d6,d7,a,b,c);

input a,b,c;

output d0,d1,d2,d3,d4,d5,d6,d7;

assign d0 = (~a&~b&~c); 

assign d1 = (~a&~b&c);

assign d2 = (~a&b&~c);

assign d3 =(~a&b&c);

assign d4 = (a&~b&~c); 

assign d5 = (a&~b&c);

assign d6 = (a&b&~c); 

assign d7 = (a&b&c); 

endmodule








### RTL LOGIC  

ENCODER

![238169328-aca6fb80-f5c1-4804-b92a-d85bb364631f](https://github.com/yuvasri2005/Experiment-08-Encoders-and-decoders-/assets/129949620/410770e3-48ef-409b-8ed6-b8616545cf6e)


DECODER

![238169342-8ab1edd1-9e35-4ca3-badb-22d69a610f8b](https://github.com/yuvasri2005/Experiment-08-Encoders-and-decoders-/assets/129949620/42ab0b53-1632-4aea-bcad-a27fcc86243d)






### TIMING DIGRAMS  

ENCODER

![238169377-bc6f29a3-f066-44f8-93d2-58303534584f](https://github.com/yuvasri2005/Experiment-08-Encoders-and-decoders-/assets/129949620/8b4764e4-5b97-4598-9886-2e3efd34e037)

DECODER


![238169392-22db8d63-5ac5-46d9-a404-be4508d6aceb](https://github.com/yuvasri2005/Experiment-08-Encoders-and-decoders-/assets/129949620/016efb68-223d-4939-9c21-a26cbd85aa03)



### TRUTH TABLE 

ENCODER

![238169396-ab4d23b4-a160-4eb3-a657-afe368bf1bdb](https://github.com/yuvasri2005/Experiment-08-Encoders-and-decoders-/assets/129949620/ff9bf168-4584-4c97-8c68-c940318a1f06)




DECODER

![238169407-76129e95-ba7d-4402-ac33-ca97a3d84f2e](https://github.com/yuvasri2005/Experiment-08-Encoders-and-decoders-/assets/129949620/8204ee65-958a-4e50-8d66-6495826d0cfd)




### RESULTS 

Thus the program to design Encoder and Decoder are completed.
