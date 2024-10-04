# deep_dream
An AI Model is ultimately characterized by its structure: the layers, the operations, and the number of parameters. Model is what is unchanging throughout training. Even most of the hyperparameters are not really a characteristic of the model. The parameter does not have an inherent relation to the model, for parameters can be any number. In this perspective, the input and the parameters are not different. They are both numbers. They both can change. The model cannot differentiate between input and parameters. We impose categorization among them by only changing the parameters. For example, take an intermediate layer; during backpropagation, the layer receives a gradient, which is then used to calculate the gradient w.r.t to the input and the parameters of that layer. The gradient calculated w.r.t to the input is passed to the layer before it. This fact is true for the first layer as well. The input backpropagated in the first layer is the gradient w.r.t to the input. Input may well be the output from an unknown layer. But these gradients are ignored. We change the parameters so that loss function may decrease w.r.t to the input. But, these input gradients are real and we may as well change the input to fit the parameters.

The deep dream algorithm is built on this idea. What if we alter the image w.r.t to the parameters? That is, we alter the image such that the output of an layer is maximized. We aim to maximize the input to that layer. What does this mean? The image is altered to fit what the layer searches in it. 
                
                
What I noticed during deep dreams, especially during w.r.t the initial layers, is a differentiation of colors. Red, Blue, and Green. At every group of pixels, a specific primary color is maximized. This is why the pattern is psychedelic. The fundamental colors (3 arrays) are being separated. At a specific pixel, a color is maximized (It is gradient ascent, after all). The more activated a pixel is more it is affected.
