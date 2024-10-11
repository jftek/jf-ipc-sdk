
# jf-ipc-sdk

## Summary description

* The jf-ipc-sdk is a set of function interfaces, users call relevant interfaces, pass in video data and device information, generate executable program, and then run it on embedded devices with specific CPU and specific operating system, and finally users can remotely preview videos and modify configurations through tools such as JLINK APP, VMS, etc., you can also use our FunSDK to develop APP by yourself.
* The jf-ipc-sdk is aimed at such a company, which has camera audio and video function development capabilities, but is not good at cloud server deployment and function development, but wants to allow users to view camera video remotely on mobile phones or PCs.
* Our cloud servers support value-added functions such as cloud storage and intelligent analysis, and can share value-added benefits with equipment manufacturers using jf-ipc-sdk.

## Download SDK
We offer two types of SDKs：<br>
Latest Releases - We are constantly adding the latest features to make the product more feature-rich<br>
Stable version - Use more time and times, the function remains stable<br>

### For Linux
* **[Download](./Linux/download.md)**
* **[Release Note](./Linux/release_note.md)**

## Have a try
* Download the SDK package for your device (if there is no SDK package for the your device, please email to jf_ipc_sdk@jftech.com with the download path of the cross-compiler)
* Create Camera on the [Viot-product](https://viot.jftech.com/product#/product/index?lang=en&menuId=166), then get free licenses
* Read demo.c in SDK, replace uuid authkey pid
* Connect your camera to the Internet, Compile the demo and run the generated jf_ipc_sdk_demo on your camera. (The audio and video.h264 files need to be placed in the same folder as the jf_ipc_sdk_demo)
* Install the "JLINK" APP, make the uuid of the device into the form of a QR code, and then "JLINK" clicks the Add button, selects "Smart Camera", and selects "Wired Connection" to scan the front QR code to add
* After the addition is successful, preview the test video to learn the APP features

## Docking steps
* Modify the device parameters in demo.c, re-implement each callback function and audio and video data push process, and use the above effect verification process to test audio and video preview and other functions
* If it is a cable camera, you can use our DeviceManager software to configure the IP address of the camera and modify the real IP of the device in the callback function
* If it is a wifi camera, you need to realize the function of continuously collecting YUV images and then analyzing the QR code content in it, and call our jfviot_get_wifi_info_from_link_qrcode function to parse the QR code and obtain the SSID and password, and configure the wifi to connect wifi router
* Delete the previously added device in the JLINK app
* On the JLINK app, add devices with the "wired connection" method or "wireless connection" method according to the product function
* Make the device upgrade firmware, upload to [Viot-Firmware Management](https://viot.jftech.com/product#/firmware/index), create a upgrade schedule in [Viot-Firmware Update](https://viot.jftech.com/product#/upgrade/index), then test OTA on JLink App.
* Go to the [Viot-product](https://viot.jftech.com/product#/product/index?lang=en&menuId=166) to purchase the official authorization code
* Refer to the development document to understand the functions of the authorization code management server, write test tool, get the authorization code from the authorization code management server, and flash it to the camera's Flash

## Support
Technical documentation: [https://developer.en.jftech.com/](https://docs.jftech.com/docs?menusId=82518bf6b9a64411bb61d109bcdbb6fa&siderId=20d777495bd84b069917bfa7c5c4cfac&lang=en) <br>
Email: jf_ipc_sdk@jftech.com <br>

## License
[MIT License](./LICENSE)
