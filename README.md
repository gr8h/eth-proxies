# Solidity Proxy

This project demonstrates a basic Proxy for learning purposes only.

**A proxy** is a smart contract that acts as an intermediary between a user and another smart contract. It allows users to interact with the underlying contract without having to know its address, and it can also be used to add additional functionality to the underlying contract.

As smart contract code can never be upgraded, a proxy can set between the EOA and the contract (the Logic), then if we need to upgrad our logic we can ask our proxy to point to the new logic.

It's important to note that the data storage is on the proxy level not in the contract (the Logic), otherwise, we would need to do a data migration everytime we need to change the logic.

In this example the StorageSlot Library in [EIP 1967: Proxy Storage Slots.](https://eips.ethereum.org/EIPS/eip-1967) is used, to allow us to determine the storage location, to avoid any collison between the proxy and contract(s) slot locations.

**Limitations!** This proxy it does not return the return value in the `fallback` function. 
