# ble-coc-tester
Test the implementation of BLE CoC(Connection Oriented Channel) in Android 7.0.

LE L2CAP connection oriented channel is implemented in Fluoride Bluetooth stack(https://android-review.googlesource.com/#/c/188152), but there is no exposed Android API in Framework. There is API public BluetoothServerSocket listenUsingL2capOn(int port, boolean mitm, boolean min16DigitPin) in BluetoothAdapter.java, but the API is marked with "@hide". So App can not call the API to create a sorket server on BLE CoC.

ble-coc-tester app calls listenUsingL2capOn() to test the implementation in Fluoride Bluetooth stack.
