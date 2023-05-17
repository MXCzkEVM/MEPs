# MEPs

MEPs repo contains the MXC Evolution Proposals for EVM compatible chains. The proposals define the interface for implementation of the MXC protocol for IoT data exchange, mining and data marketplace.

## Introduction

Different MEPs describe different parts of the system and influence different stages of the data exchange protocol.

## Contributing

1. Review [MEP-1](./MEP-1.md).
2. Fork the repository by clicking "Fork" in the top right.
3. Add your MEP to your fork of the repository. There is a [template MEP here](./eip-template.md).
4. Submit a Pull Request to MXC's [MEPs repository](https://github.com/MXCzkEVM/MEPs).

Your first PR should be a first draft of the final MEP. It must meet the formatting criteria enforced by the build (largely, correct metadata in the header). An editor will manually review the first PR for a new MEP and assign it a number before merging it. Make sure you include a `discussions-to` header with the URL to a discussion forum or open GitHub issue where people can discuss the MEP as a whole.

If your MEP requires images, the image files should be included in a subdirectory of the `assets` folder for that MEP as follows: `assets/mep-X` (for MEP X). When linking to an image in the MEP, use relative links such as `../assets/mep-X/image.png`.

## MEPs

| MEP Number | Title                                                    | Type      | Status |
| ---------- | -------------------------------------------------------- | --------- | ------ |
| MEP-1      | Purpose and Guidelines                                   | Process   | Living |
| MEP-20     | Tokens on MXC zkEVM Chain                                | Standards | Draft  |
| MEP-721    | Non-Fungible Token Standard on MXC zkEVM Chain           | Standards | Draft  |
| MEP-801    | ISO Application Contract                                 | Standards | Draft  |
| MEP-802    | Provisioning Contract                                    | Standards | Draft  |
| MEP-803    | Sensor Data Contract                                     | Standards | Draft  |
| MEP-804    | Reward Token Contract                                    | Standards | Draft  |
| MEP-1002   | Nestable Non-Fungible Tokens Tied to IoT Geolocations    | Standards | Draft  |
| MEP-1004   | Non-Fungible Tokens Tied to IoT Radio Base Station Miner | Standards | Draft  |
