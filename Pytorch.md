## RuntimeError: Function 'LogSoftmaxBackward0' returned nan values in its 0th output.
## Reason:
I use apex for fp16, but I have a code use torch.zeros, so the grad may go to zero or nan.
Change the torch.zeros to torch.rand, solved.
