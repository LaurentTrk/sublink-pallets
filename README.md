# SubLink Pallets

These pallets have been developed for the [SubLink Project](https://github.com/LaurentTrk/sublink).

## SubLink XCM Pallet

This pallet manage the XCM communication between the SubLink parachain and the others parachains.  
It acts both as a sender and a receiver of these messages, and should be deployed on each [parachain runtime](https://github.com/LaurentTrk/sublink/blob/main/runtime/src/xcm_config.rs#L223).

## SubLink Parachain Oracle

This is an Oracle proxy that relies on the SubLink XCM Pallet to retrieve price feeds.  
It implements the same interface as the Chainlink Pricefeed interface, and should be implemented in the [price feeds client parachains runtime](https://github.com/LaurentTrk/sublink-defichain/blob/master/runtime/src/lib.rs#L496).

## SubLink ink! Extension

These 2 pallets are used for the ink! contract extension : the runtime pallet is used in the [price feed client parachain runtime](https://github.com/LaurentTrk/sublink-defichain/blob/master/runtime/src/lib.rs#L547), and the contract pallet is used in [ink! contract](https://github.com/LaurentTrk/sublink-defi-contract/blob/main/lib.rs#L6).
