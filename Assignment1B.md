# Project-1
# Question 1: What are Channels and Kernels (according to EVA)?
# Answer 1: 
A filter and/or a kernel is a feature detector in the context of a  Convolutional Neural Network. 
In CNN dictionary, Kernel = filters = feature detector.
The weight of the filter determines the specific feature extracted. 
Filters in a Convoluntional network are shared across the entire image. 
To be more precise,the input is convolved with the filter. 
In Image Processing, kernel is a small matrix used for various operations such as blurring,sharpening,embossing,edge detection,etc. 
This is achieved by convoluting an image and a kernel.
Let us consider a Music Band group which consists of various instrument players and vocalists. 
Each instrument by himself is a unique channel.
Also,if there is a Guitarist who is also singing, the Guitarist part of him is a separate channel and the Singer part is another.
If there is a text input,each character is a separate channel.
The first task in DNN is to create a simple channel list.
Basically,
Every Kernel=Feature_Extractor,
Channels=Similar_Feature_Bags


# Question 2:Why should we only (well mostly) use 3x3 Kernels?
# Answer 2:
The reason for using 3x3 kernels over 5x5 is that with smaller kernel size, we get lower number of weights and more number of layers.
A 3x3 kernel reduces the number of parameters.
A 3x3 kernel is computationally efficient due to lower number of weights whereas a 5x5 or 7x7 would be computationally expensive.
As the number of layers are more, it learns complex and more non-linear features.
If a question arises as to why not 2x2 instead of 3x3, then we prefer odd sized over even sized kernels because if we were to consider the final output pixel (of next layer) that was obtained by convolving on the previous layer pixels, all the previous layer pixels would be symmetrically around the output pixel.
Without this symmetry, we will have to account for distortions across the layers. 
This will happen due to the usage of an even sized kernel. Therefore, even sized kernel filters aren’t preferred.


# Question 3: How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)
# Answer 3:
We need to perform 100 3*3 convolution operations to reach 1*1 from 199*199

(199*199),(197*197),(195*195),(193*193),(191*191),
(189*189),(187*187),(185*185),(183*183),(181*181),
(179*179), (177*177), (175*175), (173*173), (171*171),
(169*169), (167*167), (165*165), (163*163), (161*161),
(159*159), (157*157), (155*155), (153*153), (151*151),
(149*149), (147*147), (145*145), (143*143), (141*141),
(139*139), (137*137 135*135, 133*133, 131*131,
129*129, 127*127, 125*125, 123*123, 121*121,
119*119, 117*117, 115*115, 113*113, 111*111,
109*109, 107*107, 105*105, 103*103, 101*101,
99*99, 97*97, 95*95, 93*93, 91*91,
89*89, 87*87, 85*85, 83*83, 81*81,
79*79, 77*77, 75*75, 73*73, 71*71,
69*69, 67*67, 65*65, 63*63, 61*61,
59*59, 57*57, 55*55, 53*53, 51*51,
49*49, 47*47, 45*45, 43*43, 41*41,
39*39, 37*37, 35*35, 33*33, 31*31,
29*29, 27*27, 25*25, 23*23, 21*21,
19*19, 17*17, 15*15, 13*13, 11*11,
9*9, 7*7, 5*5, 3*3, 1*1





