All about ZAMA's [Concrete](https://github.com/zama-ai/concrete) program

Docs : https://docs.zama.ai/concrete/

### So how does this work ?

1. Using the concrete framework, one can write ``FHE circuits``
2. Compile those ``FHE circuits`` & host the compilation artifact on a server
3. Send an encrypted payload (inputs to the function) to the server 
4. The result of the computation is returned in encrypted form
5. Decrypt the result

### What are the drawbacks ?

1. Probability of Error : 1 in 100000 computation might result in incorrect value. This can be configured to a lower value, which in turn would affect performance.
2. Only selected `numpy` & arithmetic operations are allowed inside these `FHE circuits`, refer to the documentation [here](https://docs.zama.ai/concrete/getting-started/compatibility).


## Concrete - ML

https://docs.zama.ai/concrete-ml

- A model is trained using plaintext, non-encrypted, training data.
- The model is converted into an integer equivalent using quantization
- Do Simulation : Execute a model that was quantized, to measure the accuracy it would have in FHE
- Compiled using FHE's compiler
- The compiled model can then be executed on encrypted data, once the proper keys have been generated

Supported models : https://docs.zama.ai/concrete-ml/built-in-models/linear

### Drawbacks
- Limited precision (16-bit integers supported)
- Loss of accuracy versus the original model, which operates on plaintext
- No support for pre-processing model inputs and post-processing model outputs
- Not all models are compatible with FHE constraints out of the box
