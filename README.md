# fhe-research

- [Concrete](./Concrete.md)

### The idea
-  The goal is to allow traders to write python programs like these & encrypt those strategies
```
def swap_matic():
  # Swap 10 Matic Tokens for 12 DAI tokens

def swap_dai():
  # Swap 12 DAI tokens for 15 Matic Tokens (Profit of 3 Matic tokens)
```
- The encrypted strategies are uploaded to a bot on our L3. The bot carries out the trades specified in the encrypted strategies.

### Issues

- Using concrete framework, we cannot encrypt programs like the above one as the contract calls in swaps are done in python using web3.py library & external library functions cannot be encrypted in Concrete programs.

### Questions 
- Does the bot carry out those trades without decrypting those strategies ?
- If the bot decrypts the strategies to carry out the trades, aren't the strategies exposed ?
