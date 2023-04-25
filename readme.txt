This is a smart contract written in Solidity. It is an implementation of an ERC721 non-fungible token with some additional functionality. 

The contract is named "CBAI" and it inherits from the "ERC721" contract from the OpenZeppelin library, which defines the ERC721 interface. It also inherits from the "Ownable" contract, which provides the contract owner with certain privileges. Finally, it inherits from the "ReentrancyGuard" contract, which is a security measure to prevent reentrancy attacks.

The contract has several state variables, including:

- `baseURI`: a string that represents the base URI of the NFT metadata.
- `baseExtension`: a string that represents the file extension of the NFT metadata.
- `totalSupply`: an unsigned integer that represents the total number of NFTs that can be minted.
- `currentSupply`: an unsigned integer that represents the current number of NFTs that have been minted.
- `NFTCost`: an unsigned integer that represents the cost of minting an NFT.
- `whitelist`: a mapping that maps an address to an unsigned integer, which is used to control who can mint NFTs.
- `blacklist`: a mapping that maps an address to an unsigned integer, which is used to prevent certain addresses from minting NFTs.
- `isSaleActive`: a boolean that represents whether the public sale is active or not.
- `isWhitelistEnabled`: a boolean that represents whether the whitelist is active or not.

The contract has several functions, including:

- `mint`: a function that allows a user to mint NFTs. It takes an unsigned integer as an argument that represents the number of NFTs to mint. The function checks that the user is not blacklisted, the sale is active, and there are enough NFTs left to mint. If the user is not the contract owner, they must also send enough ether to cover the cost of minting the NFTs. The function then mints the NFTs and increments the `currentSupply` variable.
- `whitelistMint`: a function that is similar to `mint`, but it requires the user to be on the whitelist in order to mint NFTs.
- `getTotalSupply`: a function that returns the total supply of NFTs that can be minted.
- `getCurrentSupply`: a function that returns the current supply of NFTs that have been minted.
- `setBaseURI`: a function that allows the contract owner to set the base URI of the NFT metadata.
- `setNFTCost`: a function that allows the contract owner to set the cost of minting an NFT.
- `getBaseURI`: a function that returns the current base URI of the NFT metadata.
- `getNFTCost`: a function that returns the current cost of minting an NFT.
- `getPublicSaleIsActive`: a function that returns whether the public sale is active or not.
- `batchAddToWhitelist`: a function that allows the contract owner to add multiple addresses to the whitelist.
- `singleAddToWhitelist`: a function that allows the contract owner to add a single address to the whitelist.
- `batchRemoveFromWhitelist`: a function that allows the contract owner to remove multiple addresses from the whitelist.
- `singleRemoveFromWhitelist`: a function that allows the contract owner to remove a single address from the whitelist.
- `batchAddToBlacklist`: a function that allows the contract owner to add multiple addresses to the blacklist.
- `singleAddToBlacklist`: a function that allows the contract owner to add a single address to the blacklist.
- `batchRemoveFromBlacklistfunction withdrawAll() external onlyOwner {
payable(msg.sender).transfer(address(this).balance);
}

function withdrawAmount(uint256 amount) external onlyOwner {
payable(msg.sender).transfer(amount);
}
}

This is a smart contract written in Solidity. It is an ERC721 standard contract that allows the minting of non-fungible tokens (NFTs).

The contract has the following features:

Whitelist and blacklist functionality for controlling who can or cannot mint tokens
A public sale that can be enabled or disabled by the contract owner
A whitelist-only sale that can be enabled or disabled by the contract owner
Batch and single add/remove functions for managing the whitelist and blacklist
A function for setting the base URI for the token metadata
A function for setting the cost of the NFT
Functions for getting the current and total supply of tokens
Functions for withdrawing funds from the contract
Overall, this contract provides a solid foundation for managing the minting and sale of NFTs, with several useful features for controlling access and managing the sale process.
