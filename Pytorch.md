## 1.RuntimeError: Function 'LogSoftmaxBackward0' returned nan values in its 0th output.
### Reason:
I use apex for fp16, but I have a code use torch.zeros, so the grad may go to zero or nan.
Change the torch.zeros to torch.rand, solved.

## 2. ImportError: urllib3 v2.0 only supports OpenSSL 1.1.1+, currently the 'ssl' module is compiled with 'OpenSSL 1.0.2u  20 Dec 2019'. See: https://github.com/urllib3/urllib3/issues/2168
```
pip install urllib3==1.26.6
```

## 3. ImportError: cannot import name 'OrderedDict' from 'typing'
OrderedDict add into typing after python 3.7.x(I donnot know exactly what x is).
So
```
from collections import OrderedDict
```
