## Receptive Field

The region or the area of the input data to which a specific convolution neural network is pointing to or is processing currently is called the receptive field. <br/>

Mathematically, the receptive field refers to: <br/>

n(out) = ()(n(in) + 2xp - k)/s )+1

where n(in): number of input features <br/>

n(out):number of output features<br/>

k: size of the kernel <br/>

p: padding size <br/>

s: convolution stride size ie the number of times we move through the matrix <br/>

Also, we can define receptive field as the matrix which is used for matrix multiplication during the process of convolution.

<img src="https://cdn-images-1.medium.com/max/1600/0*1PSMTM8Brk0hsJuF."/>