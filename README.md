Always use the latest (stable) version!

# Deepslate Cracker
Minecraft Fabric mod that cracks the (Overworld) world seed using deepslate patterns.

## Installation
1. Install the [Fabric Loader](https://fabricmc.net/use/).
2. Download the [Fabric API](https://minecraft.curseforge.com/projects/fabric/) and move it to your mods folder:
    - Linux/Windows: `.minecraft/mods`.
    - Mac: `minecraft/mods`.
3. Download Deepslate Cracker from the [releases page](https://github.com/asedyymym3/DeepslateCracker/releases/download/7/DeepslateCracker.zip), unzip it and move it to your mods folder.

## Commands
The mod comes with two commands. The most important command is `/deepslatecracker:crack`.

### Crack command
Usage: `/deepslatecracker:crack [<threads>] [<deepslategeneration>]`.

The `threads` parameter controls how many threads are going to be used for the cracking. Using more threads will speed up the computation. By default, the number of available threads will be used.

The `deepslategeneration` parameter controls the type of deepslate generation. Two different types exist, because there used to be a bug in Paper that would cause wrong deepslate generation. The options are `NORMAL` and `PAPER1_18`. See [19MisterX98/Nether_Bedrock_Cracker](https://github.com/asedyymym3/DeepslateCracker/releases/download/7/DeepslateCracker.zip) for more information on which one to use. By default, `NORMAL` is used.

### Source command
Usage: `/deepslatecracker:source (run)|(as <entity>)|(positioned <position>)|(rotated <rotation>)|(in <dimension>)`.

This command is largely borrowed from [SeedMapper](https://github.com/asedyymym3/DeepslateCracker/releases/download/7/DeepslateCracker.zip). Basically, it allows you to modify the source from which the command is executed. A common use-case is changing the position from which the command is executed, or forcing the dimension when the server is using an unknown world name.

## Building from source
This mod uses the [Z3 Theorem Prover](https://github.com/Z3Prover/z3) to crack the world seed. Based on the deepslate patterns, a series of constraints is imposed on the to be found seed, which Z3 smartly uses to rule out possibilities.
   ```

