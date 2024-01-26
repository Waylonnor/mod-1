# Blood Donation 


This Solidity smart contract, named **BloodDonationCamp**, facilitates blood donation by allowing participants to contribute and track their donations. The contract includes functions for managing particle counts and donated blood quantities, ensuring eligibility and monitoring the contributions.

## Contract Details

- Particle Count: The contract keeps track of the number of particles in the blood. Participants can set their particle count through the `foreignParticles` function.

- Donated Blood Quantity: The contract records the amount of blood donated by participants. The `BloodQuantity` function is used to input the quantity of donated blood.

## Functions

### `foreignParticles(uint256 _particleCount) external`

Participants use this function to declare the number of particles in their blood. The function includes a `require` statement to ensure eligibility for blood donation. The requirement is that the particle count must be fewer than 5.

### `BloodQuantity(uint256 _bloodQuantity) external`

This function allows participants to specify the quantity of blood they are donating. It utilizes `assert` and `revert` statements for additional conditions:
- `assert`: Ensures that the donated blood quantity is greater than 200 milliliters.
- `revert`: If the donated blood quantity is exactly 750 milliliters, the transaction is reverted, and a congratulatory message is displayed, indicating a $100 payback.

## License

This smart contract is released under the MIT License. See the [LICENSE](LICENSE) file for details.

## Author 
Waylon
noronhawaylon@gmail.com



