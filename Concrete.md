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
