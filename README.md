# ERC1155-Pausable
ERC1155 Pausable
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC1155/extensions/ERC1155Pausable.sol";

contract Pause1155 is ERC1155Pausable {
    constructor() ERC1155("ipfs://example/") {}

    function mint(uint256 id, uint256 amount) public {
        _mint(msg.sender, id, amount, "");
    }

    function pause() public { _pause(); }
    function unpause() public { _unpause(); }
}
