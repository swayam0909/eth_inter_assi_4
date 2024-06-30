// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract DegenToken {
    string public name = "Degen";
    string public symbol = "DGN";
    uint public totalSupply;
    address public owner;
    string public Redemption_Status;

    mapping(address => uint) public balanceOf;

    modifier onlyOwner() {
        require(msg.sender == owner, "Only the owner can call this function.");
        _;
    }

    constructor(uint initialSupply) {
        totalSupply = initialSupply;
        balanceOf[msg.sender] = totalSupply;
        owner = msg.sender;
    }


    function transfer(address to, uint Amount) external returns (bool) {
        require(to != address(0), "Invalid recipient address.");
        require(Amount <= balanceOf[msg.sender], "Insufficient balance.");

        balanceOf[msg.sender] -= Amount;
        balanceOf[to] += Amount;
        return true;
    }


    function mint(address to, uint Amount) external onlyOwner {
        require(to != address(0), "Invalid recipient address.");
        totalSupply += Amount;
        balanceOf[to] += Amount;
    }

    function burn(uint Amount) external {
        require(Amount <= balanceOf[msg.sender], "Insufficient balance.");

        balanceOf[msg.sender] -= Amount;
        totalSupply -= Amount;
    }

    function transferFrom(address from, address to, uint Amount) external returns (bool) {
        require(to != address(0), "Invalid recipient address.");
        require(Amount <= balanceOf[from], "Insufficient balance.");
        balanceOf[from] -= Amount;
        balanceOf[to] += Amount;
        return true;
    }

    function Redeem(uint prizeCost) external {
        require(balanceOf[msg.sender] >= prizeCost, "Insufficient balance for the prize.");
        balanceOf[msg.sender] -= prizeCost;
        Redemption_Status = "Redemption successful!";        
    }
}
