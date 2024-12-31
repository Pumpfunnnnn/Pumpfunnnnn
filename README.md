// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract PumpFunToken is ERC20, Ownable {
    constructor(uint256 initialSupply) ERC20("PumpFunToken", "PUMP") {
        _mint(msg.sender, initialSupply * (10 ** decimals()));
