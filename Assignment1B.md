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

(3x3) on (199x199),(3x3) on (197x197),(3x3) on (195x195),(3x3) on (193x193),(3x3) on (191x191),
(3x3) on (189x189),(3x3) on (187x187),(3x3) on (185x185),(3x3) on (183x183),(3x3) on (181x181),
(3x3) on (179x179), (3x3) on (177x177), (3x3) on (175x175), (3x3) on (173x173),(3x3) on  (171x171),
(3x3) on (169x169), (3x3) on (167x167), (3x3) on (165x165),(3x3) on  (163x163), (3x3) on (161x161),
(3x3) on (159x159),(3x3) on  (157x157), (3x3) on (155x155),(3x3) on  (153x153), (3x3) on (151x151),
(3x3) on (149x149), (3x3) on (147x147), (3x3) on (145x145), (3x3) on (143x143), (3x3) on (141x141),
(3x3) on (139x139), (3x3) on (137x137),(3x3) on  (135x135), (3x3) on (133x133), (3x3) on (131x131),
(3x3) on (129x129), (3x3) on (127x127), (3x3) on (125x125), (3x3) on (123x123), (3x3) on (121x121),
(3x3) on (119x119),(3x3) on  (117x117), (3x3) on (115x115), (3x3) on (113x113), (3x3) on (111x111),
(3x3) on (109x109), (3x3) on (107x107), (3x3) on (105x105), (3x3) on (103x103), (3x3) on (101x101),
(3x3) on (99x99), (3x3) on (97x97), (3x3) on (95x95),(3x3) on  (93x93), (3x3) on (91x91),
(3x3) on (89x89), (3x3) on (87x87), (3x3) on (85x85),(3x3) on  (83x83),(3x3) on  (81x81),
(3x3) on (79x79), (3x3) on (77x77),(3x3) on  (75x75), (3x3) on (73x73), (3x3) on (71x71),
(3x3) on (69x69), (3x3) on (67x67), (3x3) on (65x65), (3x3) on (63x63),(3x3) on  (61x61),
(3x3) on (59x59), (3x3) on (57x57), (3x3) on (55x55), (3x3) on (53x53), (3x3) on (51x51),
(3x3) on (49x49), (3x3) on (47x47), (3x3) on (45x45), (3x3) on (43x43), (3x3) on (41x41),
(3x3) on (39x39), (3x3) on (37x37),(3x3) on  (35x35), (3x3) on (33x33),(3x3) on  (31x31),
(3x3) on (29x29), (3x3) on (27x27),(3x3) on  (25x25), (3x3) on (23x23), (3x3) on (21x21),
(3x3) on (19x19), (3x3) on (17x17), (3x3) on (15x15), (3x3) on (13x13),(3x3) on  (11x11),
(3x3) on (9x9),(3x3) on  (7x7), (3x3) on (5x5),(3x3) on  (3x3), (1x1)





