# aesFA_giraud Fault Attack

## purpose of the code : 
Perfom a DFA (differential Fault analysis) attack on AES 128 bits using 3 faults

## To find a key you need to follow two steps : 
    # 1 - Find the Xvalue (this value is the common value for all your three deltas)
    # 2 - Calculate the key with the non faulted cyphertext and the Xvalue 

    
## To find the Xvalue 
solve the following equation : 

    delta = non-faulted-cypher XOR faulted-cypher


## Then check 
    delta = sbox[i] ^ (sbox[i ^ epsilon[j]]) 
    (where epsilon are all the height values possible)

## To find the key you need to solve the following equation : 
    correctCypher^sbox[xResult[0]]


## Usage
Input your deltas + plainText in hex
