Contributors: [Majeed Thaika](https://github.com/majeedthaika), [Anshu Aviral](https://github.com/cyclotronian)

Homepage: [https://majeedthaika.github.io/THOMAS/](https://majeedthaika.github.io/THOMAS/) 

So far, we have implemented and compared the performance of TransferCL and Tensorflow Lite on our android device. Both these libraries were limited to performing inference on a pretrained neural network. We found that both codebases result in comparable performance in terms of processing time for running an inference on the same architecture (Mobilenet) and similar trained checkpoint. We found that using Tensorflow Lite API was more straightforward than TransferCL, but the TransferCL code base is easier to understand and modify (for our purpose to write fine-tuning, training code) than it was for Tensorflow Lite.

### Goals and Deliverables

As described before, we are on-track with respect to our proposed schedule. We believe that we would be able to fulfil our 100% goal of fine tuning all the layers of the network, initialized with pre-trained weights. For the next steps, we will start with a crude implementation of training a neural network and then explore the possibility of efficiently running it using a compressed form of the network. We would finally parallelize the training code. If the compression works, we would also try training the network from scratch.

For the poster session, we plan to demonstrate running inference for image classification on an android device and compare the performance before and after fine tuning a trained neural network on the android device and speedup due to parallelization. If we are able to hit the 120% goal, we would also compare the performance of a model trained from scratch with the fine tuned model and networks trained on desktop.

### Revised Schedule

Time | Plan |
--- | --- | 
Nov 5 | Familiarize ourselves with TensorFlow Lite and TransferCL and start modifying the code to work with Android devices.
Nov 12 | Finish deploying the serial code and start parallelizing inference for different kinds of layers.
Nov 19 | Finish parallelizing inference on different kinds of layers of the neural network (60% goal).
Nov 26 | Start working on the serial implementation of the fine tuning construct for the last layer of the network.
Dec 3 | Write code that utilizes the GPU for parallelizing the fine tuning of the last layer of the network (100%). 
Dec 10 | Extend the implementation to perform retraining of the whole network. 
Dec 15 | Analyze and compare the performance metrics for each stage of the implementation. 
