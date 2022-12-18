### 5 Topics from Secureum 201

#### EVM Storage

In the Ethereum Virtual Machine (EVM), storage refers to the place where data is stored on the Ethereum blockchain. Every smart contract has its own storage, which is persistent and can only be modified by executing the contract's code.

In the EVM, storage is implemented as a key-value store, where each contract has a mapping from 256-bit words (keys) to 256-bit words (values). This allows contract developers to store data such as integers, strings, and arrays in the contract's storage.

The EVM uses a modified version of the Merkle Patricia tree to store the data in a tree-like structure, which allows for efficient updates and verification of the data. The root hash of the tree is stored in the contract's storage root, which is stored in the contract's storage slot in the blockchain's state trie.

It is important to note that storage is a limited resource in the EVM, as it is stored on the blockchain and each transaction that modifies the contract's storage incurs a cost in gas. As a result, it is important for contract developers to be mindful of the amount of data they store and to design their contracts efficiently to minimize the use of storage

#### EVM Storage Layout

In the Ethereum Virtual Machine (EVM), storage refers to the place where data is stored on the Ethereum blockchain. Every smart contract has its own storage, which is persistent and can only be modified by executing the contract's code.

In the EVM, storage is implemented as a key-value store, where each contract has a mapping from 256-bit words (keys) to 256-bit words (values). This allows contract developers to store data such as integers, strings, and arrays in the contract's storage.

The EVM uses a modified version of the Merkle Patricia tree to store the data in a tree-like structure, which allows for efficient updates and verification of the data. The root hash of the tree is stored in the contract's storage root, which is stored in the contract's storage slot in the blockchain's state trie.

It is important to note that storage is a limited resource in the EVM, as it is stored on the blockchain and each transaction that modifies the contract's storage incurs a cost in gas. As a result, it is important for contract developers to be mindful of the amount of data they store and to design their contracts efficiently to minimize the use of storage

#### EVM Memory

In the Ethereum Virtual Machine (EVM), memory refers to a temporary, volatile storage area that is used to hold data while a contract is being executed. It is a linear array of bytes that is dynamically sized, meaning that the size of the memory can be increased as needed during contract execution.

Memory is used to store variables and data structures that are used during the execution of a contract, but are not needed to be stored persistently on the blockchain. For example, a contract might use memory to store the result of an intermediate calculation that is needed for further processing, but is not needed to be stored permanently in the contract's storage.

Memory is implemented as a byte array and can be accessed using a byte array index. It is important to note that the EVM uses a word-based addressing system, where each word is 32 bytes (256 bits) in size. This means that when accessing memory, the index must be a multiple of 32.

#### EVM Free Memory Pointer

n the Ethereum Virtual Machine (EVM), the free memory pointer is a pointer that points to the next available byte in memory. It is used to keep track of the available space in memory and to allocate new memory as needed during contract execution.

The free memory pointer is implemented as a variable that stores the index of the next available byte in memory. It is initialized to point to the first byte of memory when the contract is deployed, and is updated as new memory is allocated during contract execution.

To allocate new memory, the contract can use the malloc instruction, which takes the number of bytes to allocate as an argument and returns the index of the first byte of the allocated memory. The free memory pointer is then updated to point to the next available byte after the allocated memory.

#### Name Collision Error

In the Solidity programming language, a name collision error occurs when a variable, function, or other identifier in a contract has the same name as a reserved keyword or built-in function in Solidity. This can lead to confusion and can cause issues when compiling and deploying the contract.

For example, if a contract defines a variable named function, it would cause a name collision error, as function is a reserved keyword in Solidity. Similarly, if a contract defines a function named send, it would cause a name collision error, as send is the name of a built-in function in Solidity that is used to send Ether to a specified address.

To avoid name collision errors, it is important for contract developers to choose descriptive and unique names for their variables, functions, and other identifiers. It is also a good idea to familiarize oneself with the list of reserved keywords and built-in functions in Solidity to avoid using them as identifier names.

If a name collision error is encountered when compiling a contract, it can typically be resolved by modifying the identifier name to be unique and not a reserved keyword or built-in function.
