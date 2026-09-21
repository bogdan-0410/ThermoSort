# ThermoSort Sensor Board

## Overview

The ThermoSort Sensor Board enables battery detection through two pairs of ultrasonic sensors and one thermal camera.

## Thermal System

If a battery is damaged or malfunctioning, it can become extremely hot, potentially damaging the surrounding plastic. The thermal camera embedded in the ThermoSort Sensor Board detects the temperature difference between the surrounding plastic and an overheating battery. This allows the recycling process to be stopped, the battery to be removed, and the process to continue without losing an otherwise recyclable plastic pallet.

The thermal system consists of:

- MLX90640ESF-BAA-000-SP - a thermal camera manufactured by Melexis.

## Ultrasonic System

If batteries are present in the plastic pallet but are not malfunctioning, the thermal system may not be effective. For this reason, an ultrasonic system has also been added.

The ultrasonic system sends sound waves through the pallet and analyzes the returning signal to detect abnormalities. Since plastic and metal have different acoustic properties, the presence of a battery can affect the strength and characteristics of the returning ultrasonic signal.

The ultrasonic system consists of:

- 2× CUSA-T80-120-2200-TH - ultrasonic transmitters manufactured by Same Sky.
- 2× CUSA-R80-120-2200-TH - ultrasonic receivers manufactered by Same Sky.

## Communication System

The Sensor Board does not process the sensor data by itself because it does not contain a microprocessor. It connects to the ThermoSort main board through an 8-pin connector that provides power and carries the signals for the thermal and ultrasonic systems.

The main board processes the sensor data and communicates with the rest of the system. The Sensor Board can be used with a suitable microprocessor, provided that it has sufficient processing capability and enough I/O interfaces to operate the sensors.