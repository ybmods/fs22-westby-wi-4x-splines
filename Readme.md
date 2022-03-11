# Westby, WI 4X Traffic Splines

These are replacement traffic and AI splines for integration into [Westby, WI 4X by MB Farms, Tired Iron Modding](https://mb-farms.itch.io/fs22-westby-wi-4x-map).

Created for map version **1.0.0.0**.


## Files
- `splines.i3d` - Complete replacement for existing 'splines' node of the `map.i3d`.
- `splines.i3d.shapes` - Shapes for splines.i3d.
- `sellingStationGrainElevator.i3d` - Replacement I3D placeable used for Premier Co-op and Hilltop Grains to enable base game AI delivery. Replacement for  `\placeablesa\sellingStationGeneric\sellingStationGrainElevator.i3d`.
- `sellingStationGrainElevator.i3d.shapes` - Shapes for sellingStationGrainElevator.i3d. Replacement for `\placeablesa\sellingStationGeneric\sellingStationGrainElevator.i3d.shapes`.

## Notes
- The AI and traffic splines cover all paved roads on the map plus Premier Co-op, Hilltop Grains, additional triggers at Hilltop area and the indoor trigger at Cherokee Feeds.
- If used together with the replacement `sellingStationGrainElevator.i3d`, base game AI _Deliver_ and _Load and Deliver_ will work with at least three locations: Premier Co-op, Hilltop Grains and the Cherokee Feed indoor trigger (FeedStoreSales).
- The replacement `sellingStationGrainElevator.i3d` has been done in such a way that it does not require moving the placeable which would cause the need for a new save game. If a new save game will be required anyway, it is recommended to make some small adjustments to more closely match the alignment of the triggers.

## AutoDrive
- When first loaded, the AutoDrive mod will offer to create a full set of routes for all paved roads.
- Additional splines have been added to the hammermill and some of the other sell and buy points.
- Players will still need to makes new routes for their own farms and set location markers.

## Spline Notes
- In Giants Editor, rotation of the `aiNodeGrain` node in the placeable is important. If the AI trigger node is not rotated correctly, it will be unreachable even if it is on the spline.
- It is recommended to freeze the rotation transformation for all splines so their rotation is the same, otherwise the traffic will slow down at junctions between splines.
- Shortcuts for spline editing:
    - Shift select multiple splines and use `Ctrl-H` to hide or `Shift-H` to toggle visibility for editing.
    - Select the end or start node of a spline and press `Insert` to add a node and `Ctrl-B` to place it down. Repeat for the whole spline and make adjustments along the way.
    - For two way splines, press `Ctrl-D` to duplicate and `r` to reverse the duplicate.
- Launch the game with `-cheats` command line to use console commands such as `gsAISplinesShow` and `gsAISplinesCheckInterference` to view the AI splines and interference.
- The original traffic spline has been split up to allow for more junctions needed for a complete AutoDrive network and potential expansion to include farms if needed.
- Placeables have their own splines, but these have been duplicated under `ai` splines for supported sell points so that AutoDrive can use them.
- AutoDrive route generation can be added and removed with console commands `adParseSplines` and `adRemoveSplines` respectively.