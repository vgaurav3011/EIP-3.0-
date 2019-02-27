## Receptive Field

The region or the area of the input data to which a specific convolution neural network is pointing to or is processing currently is called the receptive field. <br/>

Mathematically, the receptive field refers to: <br/>

n(out) = (n(in) + 2xp - k)/s )+1

where n(in): number of input features <br/>

n(out):number of output features<br/>

k: size of the kernel <br/>

p: padding size <br/>

s: convolution stride size ie the number of times we move through the matrix <br/>

Also, we can define receptive field as the matrix which is used for matrix multiplication during the process of convolution.
<br/>
This generally is a concept of spatial connectivity of the neurons as it allows only a certain number of neurons to be active and is the basis for increased efficiency of convolution neural networks.

<img src="https://github.com/vgaurav3011/EIP-3.0-/blob/master/Week%201/Assignment%203/receptive_field.gif"/>
