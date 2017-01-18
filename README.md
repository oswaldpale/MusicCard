# MusicCard
tutorial basico para crear un aplicacion con react native


Configurar Dispotivo Movil Usb para depurar en Modo Intranet por Wifi.

Connect Android device and adb host computer to a common Wi-Fi network accessible to both. We have found that not all access points are suitable; you may need to use an access point whose firewall is configured properly to support adb.
    Connect the device with USB cable to host.

    Make sure adb is running in USB mode on host.

    $ adb usb
    restarting in USB mode

    Connect to the device over USB.

     $ adb devices
     List of devices attached
     ######## device

    Restart host adb in tcpip mode.

    $ adb tcpip 5555
    restarting in TCP mode port: 5555

    Find out the IP address of the Android device: Settings -> About tablet -> Status -> IP address. Remember the IP address, of the form #.#.#.#. sometimes its not possible to find the IP-address of the android device, as in my case. so u can get it using adb as the following: $ adb shell netcfg and the should be in the last line of the result.

    Connect adb host to device:

    $ adb connect #.#.#.#
    connected to #.#.#.#:5555

    Remove USB cable from device, and confirm you can still access device:

    $ adb devices
    List of devices attached
    #.#.#.#:5555 device

