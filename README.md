# Hisense-AS-18TR4R5E-SmartIR-Bridge

**Creator:** HDz_designs

This repository provides a custom SmartIR implementation to control a non-smart Hisense AS-18TR4R5E air conditioner locally via Home Assistant. It is configured for an ESPHome-based transmitter utilizing the AZIOT IR Blaster.

### Technical Details
*   **Hardware:** AZIOT IR Blaster (ESP8266).
*   **Encoding:** Two-part raw encoding utilizing a 250ms (`250000` microseconds) software delay to reliably transmit large signal gaps.
*   **Mapped Modes:** Cool
*   **Fan Speeds:** Auto, High, Medium, Low
*   **Temperature Range:** 16°C – 30°C

### Installation
1. Flash your IR blaster using the configuration in `esphome/aziot_ir_blaster.yaml`.
2. Place `9000.json` into your Home Assistant directory under `custom_components/smartir/codes/air_conditioners/`.
3. Configure your SmartIR climate entity in Home Assistant to point to device code `9000`.
