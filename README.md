# Image Captioning

Automatic image captioning task includes defining a very short summary of the image with the help of computer. This task signifies the exceptional capabilities of modern AI algorithms. Here we are combining three different deep learning based architectures, `CNN`, `Attention` and `GRU` to automatically generate the captions for any image.

- `CNN`: For extracting features from the image in terms of numbers.
- `Attention`: Weighting the features based on previous predictions from GRU.
- `GRU`: Generates probability density of words from given vocabulary at each step.




Model Includes two components:

- `Encoder`: Encodes the features from `Inception` net into required size. It includes a dense layer.
- `Decoder`: Attention + GRU
  - `Attention`: It takes Encoder output and GRU hidden output (from previous time step) as input and gives context vector as output.
  - `GRU`: It takes GRU hidden and main outputs (from previous time step) and attention context vector as input and gives hidden and main outputs as result. 
