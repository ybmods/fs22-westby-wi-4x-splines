# Westby, WI 4X Traffic Splines

These are replacement traffic and AI splines for integration into [Westby, WI 4X by MB Farms, Tired Iron Modding](https://mb-farms.itch.io/fs22-westby-wi-4x-map). They provide a default AutoDrive network covering all paved roads and improved base game AI driving support.

Tested with map version **1.0.0.5**.

Does not require a new save game.

## Files
- `splines.i3d` - Replacement for existing 'splines' node of the `map.i3d`.
- `splines.i3d.shapes` - Shapes for splines.i3d.
- `sellingStationGrainElevator.i3d` - Replacement I3D placeable used for Premier Co-op and Hilltop Grains to enable base game AI delivery. Replacement for  `placeablesa\sellingStationGeneric\sellingStationGrainElevator.i3d`.
- `sellingStationGrainElevator.i3d.shapes` - Shapes for sellingStationGrainElevator.i3d. Replacement for `placeablesa\sellingStationGeneric\sellingStationGrainElevator.i3d.shapes`.

# Installation
The splines and replacement i3d for two sell points need to be installed (or ideally integrated by the map makers) to enable base game AI and delivery.

## Prepare for Editing the Map
1. Download this repository from [here](https://github.com/ybmods/fs22-westby-wi-4x-splines/archive/refs/heads/master.zip) and unzip to a temporary location.
1. Save a backup of the Westby 4x map ZIP file before editing.
1. Unzip the Westby 4x map to a temporary directory for editing.

## Import and Install the Splines
1. Open the map in [Giants Editor](https://gdn.giants-software.com/downloads.php) (`maps\mapUS\map.i3d`).
1. Expand `gameplay` -> `splines`, select the existing `trafficSystem` group and press `Delete`.
1. Go to File menu, Import..., browse and select `splines.i3d` from this repository download.
1. Expand the newly imported `splines` group at the bottom, click and shift-select the three children `trafficSystem`, `pedestrianSystem`, `ai` and press `Ctrl-X`
1. Select the existing `gameplay` -> `splines` and press `Ctrl-V` to paste into the original group.
1. The original `splines` transform group should now have the imported `trafficSystem`, `pedestrianSystem` and `ai`.
1. Select the now empty imported `splines` group at the bottom and press Delete.
1. Save the map and exit Giants Editor.

## Replace Selling Station
1. Copy `sellingStationGrainElevator.i3d` and `sellingStationGrainElevator.i3d.shapes` from this repository and overwrite the files in the map directory `placeablesa\sellingStationGeneric`. This replacement will re-align the AI splines for Hilltop Grains and Premier Co-operative.

## Re-zip the Westby 4x Map
1. Zip up the modified map and place back in your mods folder. Make sure the `modDesc.xml` is in the root of the ZIP file. It should look the same as the backup copy of your Westby 4x ZIP file.
