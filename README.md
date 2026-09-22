# Square Era Dedicated Server - Room 3: Builder's Paradise

Automated 5-Hour GitHub Actions Room Server Daemon for Square Era 3D Voxel Sandbox Room 3.

## Room Details
- Room ID: 3
- Room Name: Builder's Paradise
- Game Mode: CREATIVE
- Persistence Database: [yasamarium/square-era-db-room3](https://github.com/yasamarium/square-era-db-room3)

## Supervisor Cycle
1. Boots inside GitHub Actions on schedule (`0 */5 * * *`) or workflow dispatch.
2. Restores persistent world modifications and state from `square-era-db-room3`.
3. Hosts real-time multiplayer session daemon for 4 hours 50 minutes.
4. Auto-commits and shifts all accumulated world voxel modifications and player statistics to `square-era-db-room3`.
5. Retriggers successor workflow run before graceful termination.
