# iPhone Control

Experimental Windows software for viewing and controlling an iPhone from your PC, with optional MCP access for AI agents.

**This is a documentation-only project overview.** Application source code, installers and binaries are not hosted in this repository.

## What it does

- **Live phone view:** USB screen preview in the prepared 0.5.2 beta package.
- **Bluetooth input:** The PC acts as a Bluetooth Low Energy keyboard and mouse.
- **Manual controls:** Relative pointer movement, taps, held-pointer dragging, scrolling and basic US-layout typing.
- **Agent integration:** An opt-in local CLI and MCP bridge let compatible agents interact with the selected phone.
- **Separate permissions:** Input control and phone-image sharing are enabled separately. A Pause control stops input.

No jailbreak or extra hardware bridge is required.

## How the connection works

The display and input use different connections. USB provides the phone picture; Bluetooth carries keyboard and pointer input. The app must be running and connected to the intended phone before agent control is enabled.

The pointer is relative, not an absolute touchscreen coordinate. Wheel scrolling and held-pointer dragging are different operations.

## Requirements

- Windows 10 build 19041 or newer; Windows 11 recommended.
- A Bluetooth adapter and driver supporting the **BLE peripheral role**. A Bluetooth version number alone does not establish compatibility.
- An iPhone with AssistiveTouch enabled and Bluetooth available.
- For the USB preview path: a trusted, unlocked USB connection, Developer Mode, and prepared Apple developer display support. The project documents this path for iOS 27.x; broader compatibility is not established.

## Beta status and limitations

The prepared package is **0.5.2-beta.1**, experimental early-access software. Later development work should not be assumed to be included in that package.

- Live validation has been limited to one iPhone.
- Pixel-perfect pointer positioning, native touch gestures and full multitouch are not provided.
- Basic US-layout typing is supported; arbitrary Unicode clipboard injection is not.
- Bluetooth adapters, iOS versions, reconnection, rotation and gesture behavior need broader testing.
- Observed performance on one setup is not a guarantee for other devices.
- Compatibility with every MCP client or AI agent is not established.

## Privacy and responsible use

Use only devices you own or have permission to control. Agent image sharing can expose anything visible on the phone screen. Review your agent client's privacy settings before enabling it.

Do not post pairing codes, device identifiers, private phone screenshots or unredacted diagnostic logs in public issues. Reports should contain only a brief, non-sensitive description of the problem and the app version.

## Distribution and third-party components

This overview does not grant a license to application code or replace any component's license. Any separately distributed application package must retain its applicable third-party notices and licenses. Where GPL-covered binaries are distributed, their corresponding-source obligations must also be met. A documentation-only repository does not satisfy those obligations by itself.

This project is independent and is not affiliated with Apple or Microsoft.
