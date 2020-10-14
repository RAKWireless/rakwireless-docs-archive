---
type: page
title: Burning the Bootloader
listed: true
slug: burning-the-bootloader
---published

$plugin[{
    "type": "callout",
    "data": {
        "text": "Usually you don't need to burn the bootloader since there is a bootloader already in RAK7204 from V3.0.0.0 firmware and so on. If the firmware of your RAK7204 is V3.0.0.0 or a newer one, **Skip this section.**",
        "type": "info",
        "title": "Note:"
    }
}]$

You can burn the bootloader in your RAK7204 by following the steps below:

**1.** Download and Install the [**STM32CubeProgrammer**](https://www.st.com/content/st_com/en/products/development-tools/software-development-tools/stm32-software-development-tools/stm32-programmers/stm32cubeprog.html#overview) Software from STMicroelectronics on your Windows PC.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567313432\/18986\/y0zy3im6dd0ienfsyrsn.jpg",
        "mode": "responsive",
        "width": 1351,
        "height": 673,
        "caption": "**Figure 1:** STM32CubeProg Download Page"
    }
}]$

**2.** Insert the provided jumper on the Boot line pins ("BOOT" pin and "VDD"), shorting them . Also, make sure that the RX pin of J25 is connected to the RXCP pin.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567314723\/18986\/og57pakunpx8jvxp4ktc.jpg",
        "mode": "300",
        "width": 842,
        "height": 376,
        "caption": "**Figure 2:** Boot Line shorted using the Jumper Pins"
    }
}]$

**3.** Connect the RAK7204 on your Windows PC's USB Interface and press the RST Button or power it on again.  Open the STM32CubeProgrammer Software and Select UART type.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1590753791\/18986\/amu5gf5gsozhebos24qe.jpg",
        "mode": "responsive",
        "width": 10683,
        "height": 4990,
        "caption": "**Figure 3:** USB Interface"
    }
}]$

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567315144\/18986\/p1ntn9ii9d4ccu10gjzr.jpg",
        "mode": "responsive",
        "width": 1198,
        "height": 780,
        "caption": "**Figure 4:**  UART Settings in STM32CubeProgrammer"
    }
}]$

**4.**Choose the appropriate port number in the **COM Port** field.

**5.**Set the Baud Rate to 115200, and the Parity to Even as seen in Figure 3 then Press **Connect.**

If you didn't properly set your RAK7204 device to work in BOOT Mode, you will see the following information in the Log Section of the Software:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567315363\/18986\/wjjwvo0xfwwlbdabpwdr.jpg",
        "mode": "responsive",
        "width": 1196,
        "height": 779,
        "caption": "**Figure 5**: Errors Occurred During Connecting"
    }
}]$

- If this happens, Close the STM32CubeProgrammer and go back to the section above and set your RAK7204 device to work in **Boot Mode** again.
- If all works well, You will then see the following log:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567315445\/18986\/wgvzidnibvoiqdzjtkby.jpg",
        "mode": "responsive",
        "width": 1198,
        "height": 742,
        "caption": "**Figure 6**: Successful Connection Log to your Device"
    }
}]$

Now that you have successfully connected your RAK7204 to the STM32CubeProgrammer Tool, let's burn the Bootloader into the RAK7204.

**6.** Download the Bootloader for the RAK7204 Environmental Sensor **[here](https://downloads.rakwireless.com/en/LoRa/RAK7204/Firmware/)**.

**7.** In the STM32CubeProgrammer, Click the "Erase Chip" button to erase all the data on RAK7204:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567316036\/18986\/o5mjjpxf0ifix3vhanl9.jpg",
        "mode": "responsive",
        "width": 1204,
        "height": 777,
        "caption": "**Figure 7**: Erasing the Data in the Chip"
    }
}]$

**8.** Click "Open File" and select the correct Bootloader file that you have just downloaded.

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567316054\/18986\/ochgdykv7i7s8kffnt6o.jpg",
        "mode": "responsive",
        "width": 1198,
        "height": 779,
        "caption": "**Figure 8**: Opening the Bootloader file"
    }
}]$

**9.** Click the "Download" Button to start the burning process:

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567316146\/18986\/f4g4duloizbd9hmdodph.jpg",
        "mode": "responsive",
        "width": 1433,
        "height": 888,
        "caption": "**Figure 9**: Downloading of Bootloader to the device"
    }
}]$

**10.** After a couple of seconds, you will see the following window telling that you have successfully burned the Bootloader to your RAK7204!

$plugin[{
    "type": "image",
    "data": {
        "url": "https:\/\/res.cloudinary.com\/developerhub\/image\/upload\/v1567316176\/18986\/rr9dnhyyoixq3ljstalq.jpg",
        "mode": "responsive",
        "width": 1194,
        "height": 747,
        "caption": "**Figure 10**: Successfully Burned the Bootloader to the device"
    }
}]$

**11.**“Disconnect” and close the “STM32CubeProgrammer” tool.

$plugin[{
    "type": "callout",
    "data": {
        "text": "Disconnect your RAK7204 in your Windows PC and do not forget to remove the Jumper on the Boot Line Pins to work in Normal Mode.",
        "type": "warning",
        "title": "Warning"
    }
}]$

