# PGD-Chaser

PGD-Chaser is a FiveM QBCore script that allows police officers to track vehicles using a tracking device. This script is inspired by the real-life StarChase system used by law enforcement agencies.

## Features

- Police officers can target and track vehicles using a special tracking device item.
- The tracked vehicle's location is displayed on the minimap with a blip that updates in real-time.
- The blip color changes after a configurable duration to indicate the age of the tracking data.
- Configurable settings for item names, blip sprites, colors, and durations.

## Installation

1. Download the latest release of the PGD-Chaser script from the [releases page](https://github.com/your-username/pgd-chaser/releases).
2. Extract the contents of the ZIP file into your FXServer resources folder (e.g., `resources/[qb]/pgd-chaser`).
3. Add the following line to your server.cfg file to ensure the script is started on server startup:
4. Add the tracking device item to the QBCore shared items file (`qb-core/shared/items.lua`). For example:
```
	police_tracker = { name = 'police_tracker', label = 'Police Tracker', weight = 1000, type = 'item', image = 'police_tracker.png', unique = true, useable = false, shouldClose = true, combinable = nil, description = 'A tracking device used by police officers' },
```


5. Place the item image (`police_tracker.png`) in the `qb-inventory/html/images/` folder.
6. (Optional) Customize the configuration settings in the `config.lua` file to match your server's requirements.

## Usage

1. Make sure you have the required item (`police_tracker`) by default in your inventory.
2. Target a vehicle within the configured distance.
3. Press the configured keybind (default: F9) to trigger the tracking system.
4. The target vehicle's location will be displayed on the minimap with a blip that updates in real-time.
5. After the initial duration (5 minutes by default), the blip color will change to indicate the age of the tracking data.
6. The blip will remain at the last known location for an additional duration (30 minutes by default) before disappearing.

## Configuration

The script's configuration settings can be found in the `config.lua` file. Here are the available options:

- `Config.StarChaseItem`: The name of the item representing the tracking device.
- `Config.Cooldown`: The cooldown time (in seconds) before the player can use the tracking system again.
- `Config.TargetDistance`: The maximum distance (in meters) from which the player can target a vehicle.
- `Config.Keybind`: The keybind that the player will use to trigger the tracking system.
- `Config.VehicleBlip`: Settings for the vehicle blip on the minimap, including initial and final sprites, colors, and durations.

## Credits

This script was created by PixelGraffix Designs and is inspired by the real-life StarChase system used by law enforcement agencies.

## License

This project is licensed under the [MIT License](LICENSE).

