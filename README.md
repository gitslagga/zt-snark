# ZK-SNARK

## Dependency
* npm install -g circom
* npm install -g snarkjs
* npm install @web3-js/scrypt-shim@0.1.0 --ignore-scripts
* npm install web3@1.2.7 --ignore-scripts
* npm install circomlib

## USage
* cd src
* circom InRange.circom -r InRange.rlcs
* vim input.json
```
{"a": 3, "b": 11}
```
* circom InRange.circom --r1cs --wasm --sym
* ll
* snarkjs info -r InRange.r1cs 
* snarkjs setup -r InRange.r1cs 
* ll
* snarkjs calculatewitness --wasm InRange.wasm --input input.json --witness witness.json
* snarkjs proff
* verify
* snarkjs generateverifier
* snarkjs generatecall

## Reference
* [Zero Knowledge](https://github.com/fluree/example-zero-knowledge)
* [Circom Package](https://github.com/iden3/circom)
* [Circom Tutorial](https://github.com/iden3/circom/blob/master/TUTORIAL.md)
* [Circomlib Package](https://github.com/iden3/circomlib)