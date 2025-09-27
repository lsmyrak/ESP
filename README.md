### ESPHome Node00 – Smart Blinds Controller

This project contains an **ESPHome configuration** for an **ESP8266 (NodeMCU v2)** device that acts as a smart blinds controller. It is designed to be integrated into a smart home system via **MQTT** and/or the **ESPHome native API**, making it accessible through Home Assistant or any other MQTT-compatible platform.

#### Features

*   **Blinds Control**
    
    *   Two independent servo-driven blinds (Small Blind & Large Blind).
        
    *   Supports open, close, and stop commands.
        
    *   Manual control mode with adjustable servo position via MQTT.
        
    *   Configurable movement time (21s for small blind, 20s for large blind).
        
*   **MQTT Integration**
    
    *   Custom command topic (node00/command) with status reporting (node00/status).
        
    *   Full Home Assistant MQTT discovery support.
        
    *   Custom topics for blinds control and manual servo adjustments.
        
*   **API & OTA**
    
    *   Secure ESPHome API with encryption.
        
    *   OTA firmware updates protected by password.
        
*   **Wi-Fi Recovery Mode**
    
    *   Automatic fallback AP (EspRecoveryNode00) in case of Wi-Fi connection failure.
        
*   **Time Synchronization**
    
    *   SNTP integration for accurate time reporting.
        
*   **Remote Control via IR**
    
    *   NEC-based infrared receiver for physical remote control.
        
    *   Mapped buttons for open/close/stop and manual servo adjustments.
        
*   **Diagnostics**
    
    *   IP address exposed as a text sensor for debugging.
        
    *   MQTT status payload includes current time and device IP.
        

#### Use Cases

*   Example device for **device gateway integration** – shows how to:
    
    *   Bridge between MQTT topics and physical actuators (servos).
        
    *   Combine multiple control methods (MQTT, API, IR remote).
        
    *   Expose device state and status in a standardized format.
        
    *   Can be adapted to other servo-driven actuators such as curtains, valves, or custom mechanisms.
  
    
#### Hardware Requirements

*   ESP8266 NodeMCU v2 (or compatible).
    
*   2x Servo motors.
    
*   NEC-compatible IR receiver.
    
*   Wi-Fi network with MQTT broker.
