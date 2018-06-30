# Be-There-Tomorrow
Source code and instructions to developp an autonomous hives monitoring system

The extinction of bees is a major problem for the planet. BeeThereTomorrow seeks a new approach in bee monitoring from actual open source project (more autonomous, costless and new sensors)

PROBLEM
The disappearance of bees is not a new phenomenon. However, it has accelerated drastically in recent years due to the massive use of certain pesticides such as neonicotinoids. Intervention on hives being complicated, how best to understand the state of health of hives? How to help beekeepers who cannot invest much money and time to monitor hives often isolated in nature? Projects are being put in place. But they often cannot be adapted to all complicated situations such as hives

PROPOSAL
The idea here is not to propose a prototype impossible to integrate in a real environment. It is necessary to design a device which can answer, at least, the primary needs of a beekeeper --- Cost --- Autonomy --- Isolation --- Easy to build --- Robustness--- We manufacture an IOT device using Lora communication technology, energy-saving sensors and small solar panels. This solution should allow us to hold with a 2 amp battery during the year (even in winter). The idea is that the installer doesn't have to worry about his devices... Only some informations is reported daily to verify that no sensor is raising an alert and the device is still operational. The sensors are mounted on wire probes that allow the device to be placed outside the hive while analysing the inside.

We assume that 
We can meet beekeepers who will allow us to test our solutions.

Constraint to overcome
Even if open source projects try to answer these problems, it is difficult to manufacture a device that can respond to communication problems in isolated areas while remaining low cost and autonomous. When I talk about low cost, it is necessary that a hive can be monitored for less than a few tens of dollars. Monitoring each hive in 3G will be much too expensive in component purchase and SIM subscription. That's the reasons we are looking at alternative solutions like Lora/Sigfox or using several hives with only one 3G gateway.

Current works
So many things on test! 
>>> test many different gaz sensors (carbon monoxyde, hydrogen, methane... anything possible!) to check reaction with commercial pesticide. 
>>> testing communication solutions. We already made the chip Lora Murata work on a CMWX1ZZABZ with a public gateway. But we need to be sure they are now enough ultra wide band gateway to cover most of the lands. 
>> we need more contacts with bee keepers as any advices can be priceless! 
>> we have to continue the embedded software implementation. We added a FreeRTOS on the STM32L4 to improve the compatibility, so adding new sensors shouldn’t be a problem. 
>> the box. We have to meet more beekeepers to decide the material we will use… When all this will work, it should be a good start for the 1.0 prototype! :-)

Current needs
We are going to need some electronic development board : 
>>>ST Murata for Lora testing 
>>>Solar Panel + energie controler
>>>Lipo battery 
>>>3G board
>>>STM32L4 dev board for energy saving test (sleeping mode are 10 times better than most Arduino board) 
>>>9DOF (degree of freedom) Invensense sensors for movement detection 
>>>Probably few FSR sensors 
>>>Chemical sensors testing to try to detect some néonicotinoids 
>>>Small distance communication (in case of star topology with 3G modem) (Enocean, Bluetooth Low Energie NORDIC) 
>>>3D printer access for the waterproof design 
>>>Buy some Lora Gateway datas (or SIM card if 3G is choosen) 
>>>Probably a "Dadant" hives (the most present in my area) for integration tests
>>>Possibly a Raspberry Pi camera or TOF sensors to monitor the hive inputs and outputs. But this would pose consumption problems





