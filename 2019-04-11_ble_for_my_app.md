# Nordic talk about BLE (Bluetooth Low Energy)

Nordic sells lots of BLE.

* Use the dongle to do BLE from the dev SDK in eclipse
* nRF52-DK you can use a new Blue
    * Need to add drivers with the weird segger thing
* They did a lot of the work to get the Nordic stuff in place for the dealys

## Connect IQ

* The `Toybox.BluetoothLowEngery` is for sending stuff
* Has handlers for connectivity
* Use delgates for handling data send/recieve (like the recipe)
* For uuids replace only bytes 12 and 13
* Important stuff needs to be in the advertisement part of the BLE
* BLE is delayed by what the device (Garmin watch) wants to let you do
* Security is level 1, this means that you must do encryption yourself, it's not provided at the protocol level
* There are byte array helpers to make it easier to interact with
