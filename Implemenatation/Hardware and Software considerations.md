## Hardware and Software considerations

### Hardware Considerations

### Raspberry Pi 5

Main Hardware that's going to be used is an 8GB [Raspberry Pi 5](https://www.raspberrypi.com/products/raspberry-pi-5/). Main advantages of it are its acceptable price, performance, small size and low power consumption. More powerful devices for similar price; such as [Zima Board](https://www.zimaspace.com/products/single-board-server?utm_source=head&utm_medium=menu) exist, however the software/overall support is not nearly as good as the one for Raspberry Pi projects.<br>
Supporting components - that are either necessary and/or quality of life features include: Raspberry Pi 5 specific charger, Raspberry Pi 5 fan (to prolong the lifetime of the device - heat kills), 32GB SSD (For OS booting)

#### Specifications;

*Base Price*: [Raspberry Pi 5](https://www.galagomarket.com//item/display/3746?src=raspberrypi) - 130€ <br>
*Supporting Components Price(s):* [32GB Micro SSD](https://www.galagomarket.com//item/display/1802/5197_sd-kartice_sandisk_32-gb-micro-sd-adapter,-sdhc--c10-u3-v30-a1-uhs-i,-sandisk-extreme-100-mb-s) - 18€, [Raspberry Charger EU](https://www.galagomarket.com/item/display/3748?src=raspberrypi) - 15€, [Raspberry Pi 5 Active Cooler](https://www.galagomarket.com//item/display/3751/12268_ohisja_raspberry-pi_active-cooler-for-raspberry-pi-5-raspberry-pi-sc1148.jpeg) - 7€;<br>
*Total Cost:* Base (130€) + Supporting Component  (50€)  = 180€ <br>
Main Memory: 8Gb RAM <br>
Onboard Storage: / <br>
CPU: 2.4GHz quad-core Arm Cortex-A76

### Portable SSD - Samsung T7 2Tb

For main storage device we chose [Samsung T7](https://www.bigbang.si/samsung-portable-ssd-t7-2-samsung-izdelek-20283424/?utm_source=hatch&utm_content=69a56cf71763dc4abb542bac&utm_campaign=Samsung+IT) portable SSD disk with 2Tb of storage. While on a higher price side, we deemed it worth it since it should outlive some cheaper devices out there. Furthermore its small side and usb C access port make it perfect for this project. Some of you might be wondering why we chose USB - USB c connection for data transfer since PCI express is available on raspberry pi and is faster. This decision was made purely to increase salvageability of project in case of failure (as this expensive component (Samsung T7) can be used as a portable SSD in the case of project failure).

#### Specs;

Price: [Samsung T7](https://www.bigbang.si/samsung-portable-ssd-t7-2-samsung-izdelek-20283424/?utm_source=hatch&utm_content=69a56cf71763dc4abb542bac&utm_campaign=Samsung+IT) - 270 € <br>
Capacity: 2 Tb

#### Overview of Hardware choices;

The hardware choices were driven by cost/quality optimisation in order to have the created server have the longest possible life period at the smallest possible cost.
Concluded Total Cost of All Hardware Components: 450 €

### Software Considerations

Only open source software will be used in this project. That being said there are not too many choices available that fit the given criteria. For now we will provide only a high level overview of software that we plan to use;

[CasaOs](https://casaos.zimaspace.com) - for server "home", SSH and file management. <br>
[Cloudflare](https://www.cloudflare.com) - to ease the Networking hustles and for DNS registration. <br>
[Immich](https://demo.immich.app/photos/19758e7a-e1e4-4aae-853b-186cde2dd196) - excellent tool for image storing and browsing that also has a battalion of cool features. <br>
[Visual Studio Code Server](https://code.visualstudio.com/docs/remote/vscode-server) - for code hosting
[MariaDb](https://mariadb.org) - for databases
[PhpMyAdmin](https://www.phpmyadmin.nets) - for database access/UI

### Quick (dirty) Maths regarding Maintenance

Electrical costs for Raspberry Pi 5 running for a year; at maximal output power charger can provide is 27W = 0.027 KW. For a year of operation this rounds up to 0.027×8760h = 236.52kWh per year. Given the assumed price of 0.25€ per kWh, total maximum price of running this device for a year is 236.52 * 0.25 = 59€. However the actually real cost is much much much lower as we can expect the server to be idle most of the time with some peak loads. At idle Raspberry Pi5 spends around 3W of energy, given normal loads one can average this to around 5W which would mean that the actual cost per year is closer to ~ 10€. <br>
Only additional maintenance cost to this is domain registration which can be assumed to be about 10€ per year (but can be lower given longer periods of registration). So total maintenance cost of the server would be around 20€ per year.
## Hardware and Software considerations

### Hardware Considerations

### Raspberry Pi 5

Main Hardware that's going to be used is an 8GB [Raspberry Pi 5](https://www.raspberrypi.com/products/raspberry-pi-5/). Main advantages of it are its acceptable price, performance, small size and low power consumption. More powerful devices for similar price; such as [Zima Board](https://www.zimaspace.com/products/single-board-server?utm_source=head&utm_medium=menu) exist, however the software/overall support is not nearly as good as the one for Raspberry Pi projects.<br>
Supporting components - that are either necessary and/or quality of life features include: Raspberry Pi 5 specific charger, Raspberry Pi 5 fan (to prolong the lifetime of the device - heat kills), 32GB SSD (For OS booting)

#### Specifications;

*Base Price*: [Raspberry Pi 5](https://www.galagomarket.com//item/display/3746?src=raspberrypi) - 130€ <br>
*Supporting Components Price(s):* [32GB Micro SSD](https://www.galagomarket.com//item/display/1802/5197_sd-kartice_sandisk_32-gb-micro-sd-adapter,-sdhc--c10-u3-v30-a1-uhs-i,-sandisk-extreme-100-mb-s) - 18€, [Raspberry Charger EU](https://www.galagomarket.com/item/display/3748?src=raspberrypi) - 15€, [Raspberry Pi 5 Active Cooler](https://www.galagomarket.com//item/display/3751/12268_ohisja_raspberry-pi_active-cooler-for-raspberry-pi-5-raspberry-pi-sc1148.jpeg) - 7€;<br>
*Total Cost:* Base (130€) + Supporting Component  (50€)  = 180€ <br>
Main Memory: 8Gb RAM <br>
Onboard Storage: / <br>
CPU: 2.4GHz quad-core Arm Cortex-A76

### Portable SSD - Samsung T7 2Tb

For main storage device we chose [Samsung T7](https://www.bigbang.si/samsung-portable-ssd-t7-2-samsung-izdelek-20283424/?utm_source=hatch&utm_content=69a56cf71763dc4abb542bac&utm_campaign=Samsung+IT) portable SSD disk with 2Tb of storage. While on a higher price side, we deemed it worth it since it should outlive some cheaper devices out there. Furthermore its small side and usb C access port make it perfect for this project. Some of you might be wondering why we chose USB - USB c connection for data transfer since PCI express is available on raspberry pi and is faster. This decision was made purely to increase salvageability of project in case of failure (as this expensive component (Samsung T7) can be used as a portable SSD in the case of project failure).

#### Specs;

Price: [Samsung T7](https://www.bigbang.si/samsung-portable-ssd-t7-2-samsung-izdelek-20283424/?utm_source=hatch&utm_content=69a56cf71763dc4abb542bac&utm_campaign=Samsung+IT) - 270 € <br>
Capacity: 2 Tb

### Overview of Hardware choices;

The hardware choices were driven by cost/quality optimisation in order to have the created server have the longest possible life period at the smallest possible cost.<br>
Concluded Total Cost of All Hardware Components: 450 €

### Software Considerations

Only open source software will be used in this project. That being said there are not too many choices available that fit the given criteria. For now we will provide only a high level overview of software that we plan to use;

[CasaOs](https://casaos.zimaspace.com) - for server "home", SSH and file management. <br>
[Cloudflare](https://www.cloudflare.com) - to ease the Networking hustles and for DNS registration. <br>
[Immich](https://demo.immich.app/photos/19758e7a-e1e4-4aae-853b-186cde2dd196) - excellent tool for image storing and browsing that also has a battalion of cool features. <br>
[Visual Studio Code Server](https://code.visualstudio.com/docs/remote/vscode-server) - for code hosting.<br>
[MariaDb](https://mariadb.org) - databases.<br>
[PhpMyAdmin](https://www.phpmyadmin.nets) - for database access/UI.

### Quick (dirty) Maths regarding Maintenance

Electrical costs for Raspberry Pi 5 running for a year; at maximal output power charger can provide is 27W = 0.027 KW. For a year of operation this rounds up to 0.027×8760h = 236.52kWh per year. Given the assumed price of 0.25€ per kWh, total maximum price of running this device for a year is 236.52 * 0.25 = 59€. However the actual real cost is much much much lower as we can expect the server to be idle most of the time with some peak loads. At idle Raspberry Pi 5 spends around 3W of energy, given normal loads one can average this to around 5W which would mean that the actual cost per year is closer to ~ 10€. <br>
Only additional maintenance cost to this is domain registration which can be assumed to be about 10€ per year (but can be lower given longer periods of registration).<br>
In total maintenance cost of the server would be around 20€ per year or 1.6€  per month. 

Lets compare this to the Google Cloud's prices whcih offers a 2Tb storage priced at 10€ per month. Since our server maintanance is 1.6€  per month, monthly we save 8.4€ per month (given moderate usage and electricity price). Given base investment cost of 450€, our server will "pay itself" in 450€/8.4€ = 53.57 months roughly 4.5 years.
