# MEPs

MEPs repo contains the MXC Evolution Proposals for EVM compatible chains. The proposals define the interface for implementation of the MXC protocol for IoT data exchange, mining and data marketplace.

## Introduction

Different MEPs describe different parts of the system and influence different stages of the data exchange protocol.

### MEP-01

MEP-01 defines the interface to create tenants and applications. A partner (business owner) has the ability to create a root organization (tenant) under which he can create specific applications for different purposes.

### MEP-02

MEP-02 defines the contract layout for a provisioning contract. This contract serves the purpose of provisioning different devices (sensors) as NFTs. The business owner has the ability to provision a sensor NFT with the metadata describing the NFT and sensor specifics. The sensor owner has the ability to claim the NFT and collect rewards based on the data efficiency of the sensor.

### MEP-03

MEP-03 defines the device profile for a given set of devices. The device profile defines the LoRaWAN specification for a family of sensors, codec for decoding the LoRaWAN frames, as well as some parameters which are specific to the application.

### MEP-04

MEP-04 defines the interface for a reward token. It extends the classical ERC-20 specification with additions like transfering token from the sensor's address, fuel tank, rewarding pools and how the rewards are distribution in each cycle.