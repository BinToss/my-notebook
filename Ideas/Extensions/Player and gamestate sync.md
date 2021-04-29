Index array of instanced class object.
Each instance represents one player with each player also being represented as an integer in an index.

Gamestate and player deltas would be synced for bandwidth efficiency, but this can lead to desync over time. Find a balance of how frequently it should be resynced. Account for latency and dropped packets rate to determine how quickly the gamestate desyncs.

Run the network in 30, 60, et cetera ticks per second to combat desync-over-time. This would allow for sending smaller packets.

Deflate or otherwise compress packet contents? This would shrink delta values for sure if they're zeroed. Total of Compress and Decompress duration must be 6ms or less per packet to achieve 120tps networking.

Packet timestamp to account for changes since the packet was sent?