# Sylar154
Minecraft 1.12.2 crash-report
---- Minecraft Crash Report ----

WARNING: coremods are present:
  IELoadingPlugin (ImmersiveEngineering-core-0.12-98.jar)
  MekanismCoremod (Mekanism-1.12.2-9.8.3.390.jar)
  Uncrafting Blacklist Mixin Loading Plugin (uncrafting-blacklist-1.12.2-0.0.0.1.jar)
  CXLibraryCore (cxlibrary-1.12.1-1.6.1.jar)
  LittlePatchingLoader (LittleTiles_v1.5.72_mc1.12.2.jar)
  EnderCorePlugin (EnderCore-1.12.2-0.5.76-core.jar)
  SecurityCraftLoadingPlugin ([1.12.2] SecurityCraft v1.9.6.jar)
  PhosphorFMLLoadingPlugin (phosphor-1.12.2-0.2.6+build50-universal.jar)
  BlurPlugin (Blur-1.0.4-14.jar)
  LoadingPlugin (ResourceLoader-MC1.12.1-1.5.3.jar)
  Techguns Core (techguns-1.12.2-2.0.2.0_pre3.2.jar)
  LootrCore (lootr-1.12.2-0.6.1.jar)
  CoreMod (Aroma1997Core-1.12.2-2.0.0.2.jar)
  Inventory Tweaks Coremod (InventoryTweaks-1.64+dev.151.jar)
  XaeroWorldMapPlugin (XaerosWorldMap_1.30.3_Forge_1.12.jar)
  LoadingPlugin (RandomThings-MC1.12.2-4.2.7.4.jar)
  RandomPatches (randompatches-1.12.2-1.22.1.10.jar)
  RBLoadingPlugin (RealBench-1.12.2-1.3.3.jar)
  SSLoadingPlugin (SereneSeasons-1.12.2-1.2.18-universal.jar)
  TheBetweenlandsLoadingPlugin (TheBetweenlands-3.9.6-core.jar)
  FTBUltimineASM (ftb-ultimine-1202.3.5.jar)
  LogisticsPipesCoreLoader (logisticspipes-0.10.4.44.jar)
  ForgelinPlugin (Forgelin-1.8.4.jar)
  midnight (themidnight-0.3.5.jar)
  CreativePatchingLoader (CreativeCore_v1.10.70_mc1.12.2.jar)
  OpenModsCorePlugin (OpenModsLib-1.12.2-0.12.2.jar)
  XaeroMinimapPlugin (Xaeros_Minimap_23.4.4_Forge_1.12.jar)
  CTMCorePlugin (CTM-MC1.12.2-1.0.2.31.jar)
  AstralCore (astralsorcery-1.12.2-1.10.27.jar)
  HCASM (HammerLib-1.12.2-2.0.6.32.jar)
  Do not report to Forge! (If you haven't disabled the FoamFix coremod, try disabling it in the config! Note that this bit of text will still appear.) (foamfix-0.10.10-1.12.2.jar)
  MixinBooter (!mixinbooter-8.2.jar)
  MicdoodlePlugin (Galacticraft-1.12.2-4.0.5.jar)
  DLFMLCorePlugin (DynamicLights-1.12.2.jar)
  SteveKunGLibPlugin (SteveKunG's-Lib-mc1.12.2-v1.3.0.jar)
Contact their authors BEFORE contacting forge

// My bad.

Time: 6/3/23 7:06 AM
Description: Initializing game

java.lang.IllegalAccessError: tried to access class org.spongepowered.asm.mixin.transformer.MixinProcessor from class net.minecraftforge.fml.common.Loader
	at net.minecraftforge.fml.common.Loader.handler$zza000$uncrafting_blacklist_1_12_2_0_0_0_1$beforeConstructingMods(Loader.java:1147)
	at net.minecraftforge.fml.common.Loader.loadMods(Loader.java:594)
	at net.minecraftforge.fml.client.FMLClientHandler.beginMinecraftLoading(FMLClientHandler.java:232)
	at net.minecraft.client.Minecraft.func_71384_a(Minecraft.java:467)
	at net.minecraft.client.Minecraft.func_99999_d(Minecraft.java:378)
	at net.minecraft.client.main.Main.main(SourceFile:123)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(Unknown Source)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(Unknown Source)
	at java.lang.reflect.Method.invoke(Unknown Source)
	at net.minecraft.launchwrapper.Launch.launch(Launch.java:135)
	at net.minecraft.launchwrapper.Launch.main(Launch.java:28)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(Unknown Source)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(Unknown Source)
	at java.lang.reflect.Method.invoke(Unknown Source)
	at org.multimc.onesix.OneSixLauncher.launchWithMainClass(OneSixLauncher.java:243)
	at org.multimc.onesix.OneSixLauncher.launch(OneSixLauncher.java:278)
	at org.multimc.EntryPoint.listen(EntryPoint.java:143)
	at org.multimc.EntryPoint.main(EntryPoint.java:34)

(MixinBooter) Mixins in Stacktrace:
	net.minecraftforge.fml.common.Loader:
		doomanidus.mods.uncraftingblacklist.mixins.MixinLoader (mixins.loader.json) [uncrafting_blacklist_1_12_2_0_0_0_1]
	net.minecraft.client.Minecraft:
		net.geforcemods.securitycraft.mixin.camera.MinecraftMixin (securitycraft.mixins.json) [_5B1_12_2_5D_20SecurityCraft_20v1_9_6]
		de.maxhenkel.voicechat.mixin.MinecraftMixin (voicechat.mixins.json) [voicechat_forge_1_12_2_2_4_8]
		me.jellysquid.mods.phosphor.mixins.lighting.client.MixinMinecraft (mixins.phosphor.json) [phosphor_1_12_2_0_2_6_build50_universal]

A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Thread: Client thread
Stacktrace:
	at net.minecraftforge.fml.common.Loader.handler$zza000$uncrafting_blacklist_1_12_2_0_0_0_1$beforeConstructingMods(Loader.java:1147)
	at net.minecraftforge.fml.common.Loader.loadMods(Loader.java:594)
	at net.minecraftforge.fml.client.FMLClientHandler.beginMinecraftLoading(FMLClientHandler.java:232)
	at net.minecraft.client.Minecraft.func_71384_a(Minecraft.java:467)

-- Initialization --
Details:
Stacktrace:
	at net.minecraft.client.Minecraft.func_99999_d(Minecraft.java:378)
	at net.minecraft.client.main.Main.main(SourceFile:123)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(Unknown Source)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(Unknown Source)
	at java.lang.reflect.Method.invoke(Unknown Source)
	at net.minecraft.launchwrapper.Launch.launch(Launch.java:135)
	at net.minecraft.launchwrapper.Launch.main(Launch.java:28)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(Unknown Source)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(Unknown Source)
	at java.lang.reflect.Method.invoke(Unknown Source)
	at org.multimc.onesix.OneSixLauncher.launchWithMainClass(OneSixLauncher.java:243)
	at org.multimc.onesix.OneSixLauncher.launch(OneSixLauncher.java:278)
	at org.multimc.EntryPoint.listen(EntryPoint.java:143)
	at org.multimc.EntryPoint.main(EntryPoint.java:34)

-- System Details --
Details:
	Minecraft Version: 1.12.2
	Operating System: Windows 11 (amd64) version 10.0
	Java Version: 1.8.0_371, Oracle Corporation
	Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode), Oracle Corporation
	Memory: 8887197432 bytes (8475 MB) / 10963386368 bytes (10455 MB) up to 15271460864 bytes (14564 MB)
	JVM Flags: 3 total; -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -Xms8192m -Xmx16384m
	IntCache: cache: 0, tcache: 0, allocated: 0, tallocated: 0
	FML: MCP 9.42 Powered by Forge 14.23.5.2859 300 mods loaded, 300 mods active
	States: 'U' = Unloaded 'L' = Loaded 'C' = Constructed 'H' = Pre-initialized 'I' = Initialized 'J' = Post-initialized 'A' = Available 'D' = Disabled 'E' = Errored

	| State | ID                                | Version                                             | Source                                                  | Signature                                |
	|:----- |:--------------------------------- |:--------------------------------------------------- |:------------------------------------------------------- |:---------------------------------------- |
	| L     | minecraft                         | 1.12.2                                              | minecraft.jar                                           | None                                     |
	| L     | mcp                               | 9.42                                                | minecraft.jar                                           | None                                     |
	| L     | FML                               | 8.0.99.99                                           | forge-1.12.2-14.23.5.2859-universal.jar                 | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| L     | forge                             | 14.23.5.2859                                        | forge-1.12.2-14.23.5.2859-universal.jar                 | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| L     | creativecoredummy                 | 1.0.0                                               | minecraft.jar                                           | None                                     |
	| L     | micdoodlecore                     | 4.0.5                                               | minecraft.jar                                           | None                                     |
	| L     | littletilescore                   | 1.0.0                                               | minecraft.jar                                           | None                                     |
	| L     | xaerominimap_core                 | 1.12.2-1.0                                          | minecraft.jar                                           | None                                     |
	| L     | xaeroworldmap_core                | 1.12.2-1.0                                          | minecraft.jar                                           | None                                     |
	| L     | mixinbooter                       | 8.2                                                 | minecraft.jar                                           | None                                     |
	| L     | openmodscore                      | 0.12.2                                              | minecraft.jar                                           | None                                     |
	| L     | foamfixcore                       | 7.7.4                                               | minecraft.jar                                           | None                                     |
	| L     | randompatches                     | 1.12.2-1.22.1.10                                    | randompatches-1.12.2-1.22.1.10.jar                      | None                                     |
	| L     | techguns_core                     | 1.12.2-1.0                                          | minecraft.jar                                           | None                                     |
	| L     | securitycraft                     | v1.9.6                                              | [1.12.2] SecurityCraft v1.9.6.jar                       | None                                     |
	| L     | redstoneflux                      | 2.1.1                                               | RedstoneFlux-1.12-2.1.1.1-universal.jar                 | None                                     |
	| L     | cofhcore                          | 4.6.6                                               | CoFHCore-1.12.2-4.6.6.1-universal.jar                   | None                                     |
	| L     | ic2                               | 2.8.222-ex112                                       | industrialcraft-2-2.8.222-ex112.jar                     | None                                     |
	| L     | placebo                           | 1.6.0                                               | Placebo-1.12.2-1.6.0.jar                                | None                                     |
	| L     | industrialupgrade                 | 2.5.0.15                                            | IndustrialUpgrade-1.12.2-2.5.0.15.jar                   | None                                     |
	| L     | crafttweaker                      | 4.1.20                                              | CraftTweaker2-1.12-4.1.20.586.jar                       | None                                     |
	| L     | mtlib                             | 3.0.6                                               | MTLib-3.0.6.jar                                         | None                                     |
	| L     | modtweaker                        | 4.0.18                                              | modtweaker-4.0.18.jar                                   | None                                     |
	| L     | jei                               | 4.16.1.301                                          | jei_1.12.2-4.16.1.301.jar                               | None                                     |
	| L     | abyssalcraft                      | 1.10.4                                              | AbyssalCraft-1.12.2-1.10.4.jar                          | None                                     |
	| L     | fastbench                         | 1.7.4                                               | FastWorkbench-1.12.2-1.7.4.jar                          | None                                     |
	| L     | actuallyadditions                 | 1.12.2-r152                                         | ActuallyAdditions-1.12.2-r152.jar                       | None                                     |
	| L     | advancementplaques                | 1.4.10                                              | AdvancementPlaques-1.12.2-1.4.10.jar                    | None                                     |
	| L     | ctm                               | MC1.12.2-1.0.2.31                                   | CTM-MC1.12.2-1.0.2.31.jar                               | None                                     |
	| L     | appliedenergistics2               | rv6-stable-7                                        | appliedenergistics2-rv6-stable-7.jar                    | None                                     |
	| L     | baubles                           | 1.5.2                                               | Baubles-1.12-1.5.2.jar                                  | None                                     |
	| L     | roots                             | @VERSION@                                           | Roots-1.12.2-3.1.7.jar                                  | None                                     |
	| L     | mysticalworld                     | 1.12.2-1.11.0                                       | mysticalworld-1.12.2-1.11.0.jar                         | None                                     |
	| L     | endercore                         | 1.12.2-0.5.76                                       | EnderCore-1.12.2-0.5.76.jar                             | None                                     |
	| L     | thaumcraft                        | 6.1.BETA26                                          | Thaumcraft-1.12.2-6.1.BETA26.jar                        | None                                     |
	| L     | codechickenlib                    | 3.2.3.358                                           | CodeChickenLib-1.12.2-3.2.3.358-universal.jar           | None                                     |
	| L     | brandonscore                      | 2.4.20                                              | BrandonsCore-1.12.2-2.4.20.162-universal.jar            | None                                     |
	| L     | cofhworld                         | 1.4.0                                               | CoFHWorld-1.12.2-1.4.0.1-universal.jar                  | None                                     |
	| L     | thermalfoundation                 | 2.6.7                                               | ThermalFoundation-1.12.2-2.6.7.1-universal.jar          | None                                     |
	| L     | draconicevolution                 | 2.3.28                                              | Draconic-Evolution-1.12.2-2.3.28.354-universal.jar      | None                                     |
	| L     | thermalexpansion                  | 5.5.7                                               | ThermalExpansion-1.12.2-5.5.7.1-universal.jar           | None                                     |
	| L     | tombstone                         | 4.6.2                                               | tombstone-4.6.2-1.12.2.jar                              | None                                     |
	| L     | enderio                           | 5.3.70                                              | EnderIO-1.12.2-5.3.70.jar                               | None                                     |
	| L     | mantle                            | 1.12-1.3.3.55                                       | Mantle-1.12-1.3.3.55.jar                                | None                                     |
	| L     | projecte                          | 1.12.2-PE1.4.1                                      | ProjectE-1.12.2-PE1.4.1.jar                             | None                                     |
	| L     | chisel                            | MC1.12.2-1.0.2.45                                   | Chisel-MC1.12.2-1.0.2.45.jar                            | None                                     |
	| L     | enderiointegrationtic             | 5.3.70                                              | EnderIO-1.12.2-5.3.70.jar                               | None                                     |
	| L     | twilightforest                    | 3.11.1021                                           | twilightforest-1.12.2-3.11.1021-universal.jar           | None                                     |
	| L     | tconstruct                        | 1.12.2-2.13.0.183                                   | TConstruct-1.12.2-2.13.0.183.jar                        | None                                     |
	| L     | tesla                             | 1.0.63                                              | Tesla-1.12.2-1.0.63.jar                                 | None                                     |
	| L     | p455w0rdslib                      | 2.3.161                                             | p455w0rdslib-1.12.2-2.3.161.jar                         | None                                     |
	| L     | ae2wtlib                          | 1.0.34                                              | AE2WTLib-1.12.2-1.0.34.jar                              | None                                     |
	| L     | aether_legacy                     | 1.5.3.2                                             | aether-1.12.2-v1.5.3.2.jar                              | None                                     |
	| L     | akashictome                       | 1.2-12                                              | AkashicTome-1.2-12.jar                                  | None                                     |
	| L     | appleskin                         | 1.0.14                                              | AppleSkin-mc1.12-1.0.14.jar                             | None                                     |
	| L     | architecturecraft                 | @VERSION@                                           | architecturecraft-1.12-3.108.jar                        | None                                     |
	| L     | aroma1997core                     | 2.0.0.2                                             | Aroma1997Core-1.12.2-2.0.0.2.jar                        | None                                     |
	| L     | aroma1997sdimension               | 2.0.0.2.b89                                         | Aroma1997s-Dimensional-World-1.12.2-2.0.0.2.b89.jar     | None                                     |
	| L     | astralsorcery                     | 1.10.27                                             | astralsorcery-1.12.2-1.10.27.jar                        | None                                     |
	| L     | morphtool                         | 1.2-21                                              | Morph-o-Tool-1.2-21.jar                                 | None                                     |
	| L     | autoreglib                        | 1.3-32                                              | AutoRegLib-1.3-32.jar                                   | None                                     |
	| L     | avaritia                          | 3.3.0                                               | Avaritia-1.12.2-3.3.0.37-universal.jar                  | None                                     |
	| L     | avaritiafurnace                   | 1.0.0                                               | Avaritia_furnace-1.0.0-1.12.2.jar                       | None                                     |
	| L     | wanionlib                         | 1.12.2-2.9                                          | WanionLib-1.12.2-2.9.jar                                | None                                     |
	| L     | avaritiaddons                     | 1.12.2-1.8                                          | Avaritiaddons-1.12.2-1.8.jar                            | None                                     |
	| L     | avaritiaio                        | @VERSION@                                           | avaritiaio-1.4.jar                                      | None                                     |
	| L     | badwithernocookiereloaded         | 1.12.2-3.4.18                                       | badwithernocookiereloaded-1.12.2-3.4.18.jar             | None                                     |
	| L     | bdlib                             | 1.14.3.12                                           | bdlib-1.14.3.12-mc1.12.2.jar                            | None                                     |
	| L     | betteradvancements                | 0.1.0.77                                            | BetterAdvancements-1.12.2-0.1.0.77.jar                  | None                                     |
	| L     | betterpingdisplay                 | 1.0                                                 | BetterPingDisplay-1.12.2-1.0.jar                        | None                                     |
	| L     | bibliocraft                       | 2.4.6                                               | BiblioCraft[v2.4.6][MC1.12.2].jar                       | None                                     |
	| L     | biomesoplenty                     | 7.0.1.2444                                          | BiomesOPlenty-1.12.2-7.0.1.2444-universal.jar           | None                                     |
	| L     | blockcraftery                     | 1.12.2-1.3.1                                        | blockcraftery-1.12.2-1.3.1.jar                          | None                                     |
	| L     | blur                              | 1.0.4-14                                            | Blur-1.0.4-14.jar                                       | None                                     |
	| L     | bonsaitrees                       | 1.1.4                                               | bonsaitrees-1.1.4-b170.jar                              | None                                     |
	| L     | bookshelf                         | 2.3.590                                             | Bookshelf-1.12.2-2.3.590.jar                            | None                                     |
	| L     | botania                           | r1.10-364                                           | Botania r1.10-364.4.jar                                 | None                                     |
	| L     | buildcraftlib                     | 7.99.24.8                                           | buildcraft-all-7.99.24.8.jar                            | None                                     |
	| L     | buildcraftcore                    | 7.99.24.8                                           | buildcraft-all-7.99.24.8.jar                            | None                                     |
	| L     | buildcraftbuilders                | 7.99.24.8                                           | buildcraft-all-7.99.24.8.jar                            | None                                     |
	| L     | buildcrafttransport               | 7.99.24.8                                           | buildcraft-all-7.99.24.8.jar                            | None                                     |
	| L     | buildcraftsilicon                 | 7.99.24.8                                           | buildcraft-all-7.99.24.8.jar                            | None                                     |
	| L     | theoneprobe                       | 1.4.28                                              | theoneprobe-1.12-1.4.28.jar                             | None                                     |
	| L     | buildcraftcompat                  | 7.99.24.8                                           | buildcraft-all-7.99.24.8.jar                            | None                                     |
	| L     | buildcraftenergy                  | 7.99.24.8                                           | buildcraft-all-7.99.24.8.jar                            | None                                     |
	| L     | buildcraftfactory                 | 7.99.24.8                                           | buildcraft-all-7.99.24.8.jar                            | None                                     |
	| L     | buildcraftrobotics                | 7.99.24.8                                           | buildcraft-all-7.99.24.8.jar                            | None                                     |
	| L     | bbprojecte                        | 1.12.2                                              | buildersbag-projecte-1.12.2-1.1.0.8.jar                 | None                                     |
	| L     | buildinggadgets                   | 2.8.4                                               | BuildingGadgets-2.8.4.jar                               | None                                     |
	| L     | creativecore                      | 1.10.0                                              | CreativeCore_v1.10.70_mc1.12.2.jar                      | None                                     |
	| L     | littletiles                       | 1.5.0                                               | LittleTiles_v1.5.72_mc1.12.2.jar                        | None                                     |
	| L     | buildersbag                       | 1.12.2                                              | buildersbag-1.12.2-1.4.2.25.jar                         | None                                     |
	| L     | chameleon                         | 1.12-4.1.3                                          | Chameleon-1.12-4.1.3.jar                                | None                                     |
	| L     | chancecubes                       | 1.12.2-5.0.2.385                                    | ChanceCubes-1.12.2-5.0.2.385.jar                        | None                                     |
	| L     | chesttransporter                  | 2.8.8                                               | ChestTransporter-1.12.2-2.8.8.jar                       | None                                     |
	| L     | chickenchunks                     | 2.4.2.74                                            | ChickenChunks-1.12.2-2.4.2.74-universal.jar             | None                                     |
	| L     | clockworkphase                    | 1.0.8                                               | ClockworkPhase-1.12.2-1.0.8.jar                         | None                                     |
	| L     | clumps                            | 3.1.2                                               | Clumps-3.1.2.jar                                        | None                                     |
	| L     | cyclopscore                       | 1.6.6                                               | CyclopsCore-1.12.2-1.6.6.jar                            | None                                     |
	| L     | commoncapabilities                | 2.4.8                                               | CommonCapabilities-1.12.2-2.4.8.jar                     | None                                     |
	| L     | refinedstorage                    | 1.6.16                                              | refinedstorage-1.6.16.jar                               | None                                     |
	| L     | compactmachines3                  | 3.0.18                                              | compactmachines3-1.12.2-3.0.18-b278.jar                 | None                                     |
	| L     | compactsolars                     | 1.12.2-5.0.18.341                                   | CompactSolars-1.12.2-5.0.18.341-universal.jar           | None                                     |
	| L     | controlling                       | 3.0.10                                              | Controlling-3.0.12.2.jar                                | None                                     |
	| L     | cookingforblockheads              | 6.5.0                                               | CookingForBlockheads_1.12.2-6.5.0.jar                   | None                                     |
	| L     | ctgui                             | 1.0.0                                               | CraftTweaker2-1.12-4.1.20.586.jar                       | None                                     |
	| L     | crafttweakerjei                   | 2.0.3                                               | CraftTweaker2-1.12-4.1.20.586.jar                       | None                                     |
	| L     | cucumber                          | 1.1.3                                               | Cucumber-1.12.2-1.1.3.jar                               | None                                     |
	| L     | cxlibrary                         | 1.6.1                                               | cxlibrary-1.12.1-1.6.1.jar                              | None                                     |
	| L     | cyberware                         | 0.2.11.29                                           | cyberware-1.12.2-0.2.11.29.jar                          | None                                     |
	| L     | waila                             | 1.8.26                                              | Hwyla-1.8.26-B41_1.12.2.jar                             | None                                     |
	| L     | stg                               | 1.12.2-1.2.3                                        | stg-1.12.2-1.2.3.jar                                    | None                                     |
	| L     | mousetweaks                       | 2.10                                                | MouseTweaks-2.10-mc1.12.2.jar                           | None                                     |
	| L     | danknull                          | 1.7.91                                              | DankNull-1.12.2-1.7.91.jar                              | None                                     |
	| L     | ptrmodellib                       | 1.0.5                                               | PTRLib-1.0.5.jar                                        | None                                     |
	| L     | props                             | 2.6.3.7                                             | Decocraft-2.6.3.7_1.12.2.jar                            | None                                     |
	| L     | journeymap                        | 1.12.2-5.7.1                                        | journeymap-1.12.2-5.7.1.jar                             | None                                     |
	| L     | defaultoptions                    | 9.2.8                                               | DefaultOptions_1.12.2-9.2.8.jar                         | None                                     |
	| L     | diethopper                        | 1.1                                                 | diethopper-1.1.jar                                      | None                                     |
	| L     | dynamiclights                     | 1.4.9                                               | DynamicLights-1.12.2.jar                                | None                                     |
	| L     | dynamiclights_onfire              | 1.0.7                                               | DynamicLights-1.12.2.jar                                | None                                     |
	| L     | dynamiclights_creepers            | 1.0.6                                               | DynamicLights-1.12.2.jar                                | None                                     |
	| L     | dynamiclights_dropitems           | 1.1.0                                               | DynamicLights-1.12.2.jar                                | None                                     |
	| L     | dynamiclights_entityclasses       | 1.0.1                                               | DynamicLights-1.12.2.jar                                | None                                     |
	| L     | dynamiclights_mobequipment        | 1.1.0                                               | DynamicLights-1.12.2.jar                                | None                                     |
	| L     | dynamiclights_flamearrows         | 1.0.1                                               | DynamicLights-1.12.2.jar                                | None                                     |
	| L     | dynamiclights_floodlights         | 1.0.3                                               | DynamicLights-1.12.2.jar                                | None                                     |
	| L     | dynamiclights_otherplayers        | 1.0.9                                               | DynamicLights-1.12.2.jar                                | None                                     |
	| L     | dynamiclights_theplayer           | 1.1.3                                               | DynamicLights-1.12.2.jar                                | None                                     |
	| L     | eleccore                          | 1.9.453                                             | ElecCore-1.12.2-1.9.453.jar                             | None                                     |
	| L     | ebwizardry                        | 4.3.9                                               | ElectroblobsWizardry-4.3.9.jar                          | None                                     |
	| L     | enderiobase                       | 5.3.70                                              | EnderIO-1.12.2-5.3.70.jar                               | None                                     |
	| L     | enderioconduits                   | 5.3.70                                              | EnderIO-1.12.2-5.3.70.jar                               | None                                     |
	| L     | enderioconduitsappliedenergistics | 5.3.70                                              | EnderIO-1.12.2-5.3.70.jar                               | None                                     |
	| L     | enderioconduitsopencomputers      | 5.3.70                                              | EnderIO-1.12.2-5.3.70.jar                               | None                                     |
	| L     | enderioconduitsrefinedstorage     | 5.3.70                                              | EnderIO-1.12.2-5.3.70.jar                               | None                                     |
	| L     | enderiointegrationforestry        | 5.3.70                                              | EnderIO-1.12.2-5.3.70.jar                               | None                                     |
	| L     | enderiointegrationticlate         | 5.3.70                                              | EnderIO-1.12.2-5.3.70.jar                               | None                                     |
	| L     | enderioinvpanel                   | 5.3.70                                              | EnderIO-1.12.2-5.3.70.jar                               | None                                     |
	| L     | ftblib                            | 5.4.7.2                                             | FTBLib-5.4.7.2.jar                                      | None                                     |
	| L     | enderiomachines                   | 5.3.70                                              | EnderIO-1.12.2-5.3.70.jar                               | None                                     |
	| L     | enderiopowertools                 | 5.3.70                                              | EnderIO-1.12.2-5.3.70.jar                               | None                                     |
	| L     | enderstorage                      | 2.4.6.137                                           | EnderStorage-1.12.2-2.4.6.137-universal.jar             | None                                     |
	| L     | enderutilities                    | 0.7.15                                              | enderutilities-1.12.2-0.7.15.jar                        | None                                     |
	| L     | engineersdecor                    | 1.1.5                                               | engineersdecor-1.12.2-1.1.5.jar                         | None                                     |
	| L     | engineerstools                    | 1.0.5                                               | engineerstools-1.12.2-1.0.5.jar                         | None                                     |
	| L     | valkyrielib                       | 1.12.2-2.0.20.1                                     | valkyrielib-1.12.2-2.0.20.1.jar                         | None                                     |
	| L     | environmentaltech                 | 1.12.2-2.0.20.1                                     | environmentaltech-1.12.2-2.0.20.1.jar                   | None                                     |
	| L     | hammercore                        | 2.0.6.32                                            | HammerLib-1.12.2-2.0.6.32.jar                           | None                                     |
	| L     | equivadditions                    | 12.2.9                                              | EquivalentAdditions-1.12.2-12.2.9.jar                   | None                                     |
	| L     | gunpowderlib                      | 1.12.2-1.1                                          | GunpowderLib-1.12.2-1.1.jar                             | None                                     |
	| L     | mcmultipart                       | 2.5.3                                               | MCMultiPart-2.5.3.jar                                   | None                                     |
	| L     | mekanism                          | 1.12.2-9.8.3.390                                    | Mekanism-1.12.2-9.8.3.390.jar                           | None                                     |
	| L     | railcraft                         | 12.0.0                                              | railcraft-12.0.0.jar                                    | None                                     |
	| L     | immersiveengineering              | 0.12-98                                             | ImmersiveEngineering-0.12-98.jar                        | None                                     |
	| L     | exchangers                        | 1.12.2-2.10.2                                       | Exchangers-1.12.2-2.10.2.jar                            | None                                     |
	| L     | expequiv                          | 12.3.17                                             | ExpandedEquivalence-1.12.2-12.3.17.jar                  | None                                     |
	| L     | extendedcrafting                  | 1.5.6                                               | ExtendedCrafting-1.12.2-1.5.6.jar                       | None                                     |
	| L     | extrautils2                       | 1.0                                                 | extrautils2-1.12-1.9.9.jar                              | None                                     |
	| L     | fastfurnace                       | 1.3.1                                               | FastFurnace-1.12.2-1.3.1.jar                            | None                                     |
	| L     | fastleafdecay                     | v14                                                 | FastLeafDecay-v14.jar                                   | None                                     |
	| L     | sonarcore                         | 5.0.19                                              | sonarcore-1.12.2-5.0.19-20.jar                          | None                                     |
	| L     | fluxnetworks                      | 4.1.0                                               | FluxNetworks-1.12.2-4.1.1.34.jar                        | None                                     |
	| L     | foamfix                           | 0.10.10-1.12.2                                      | foamfix-0.10.10-1.12.2.jar                              | None                                     |
	| L     | forgelin                          | 1.8.4                                               | Forgelin-1.8.4.jar                                      | None                                     |
	| L     | forgemultipartcbe                 | 2.6.2.83                                            | ForgeMultipart-1.12.2-2.6.2.83-universal.jar            | None                                     |
	| L     | microblockcbe                     | 2.6.2.83                                            | ForgeMultipart-1.12.2-2.6.2.83-universal.jar            | None                                     |
	| L     | minecraftmultipartcbe             | 2.6.2.83                                            | ForgeMultipart-1.12.2-2.6.2.83-universal.jar            | None                                     |
	| L     | ftbultimine                       | 1202.3.5                                            | ftb-ultimine-1202.3.5.jar                               | None                                     |
	| L     | ftbbackups                        | 1.1.0.1                                             | FTBBackups-1.1.0.1.jar                                  | None                                     |
	| L     | ftbutilities                      | 5.4.1.131                                           | FTBUtilities-5.4.1.131.jar                              | None                                     |
	| L     | cfm                               | 6.3.0                                               | furniture-6.3.2-1.12.2.jar                              | None                                     |
	| L     | galacticraftcore                  | 4.0.5                                               | Galacticraft-1.12.2-4.0.5.jar                           | None                                     |
	| L     | galacticraftplanets               | 4.0.5                                               | Galacticraft-1.12.2-4.0.5.jar                           | None                                     |
	| L     | globe                             | 0.0.1                                               | Globe-1.12.2-0.0.1.jar                                  | None                                     |
	| L     | ichunutil                         | 7.2.2                                               | iChunUtil-1.12.2-7.2.2.jar                              | None                                     |
	| L     | gravitygun                        | 7.1.0                                               | GravityGun-1.12.2-7.1.0.jar                             | None                                     |
	| L     | gregtechmod                       | 0.9.45                                              | gregtechmod-0.9.45.jar                                  | None                                     |
	| L     | guideapi                          | 1.12-2.1.8-63                                       | Guide-API-1.12-2.1.8-63.jar                             | None                                     |
	| L     | hbm                               | Hbms Nuclear Tech - Hamster Reloaded - 1.12.2-1.0.4 | Hbms Nuclear Tech - Hamster Reloaded - 1.12.2-1.0.4.jar | None                                     |
	| L     | immersiveposts                    | 0.2.1                                               | ImmersivePosts-0.2.1.jar                                | None                                     |
	| L     | teslacorelib                      | 1.0.18                                              | tesla-core-lib-1.12.2-1.0.18.jar                        | None                                     |
	| L     | industrialforegoing               | 1.12.2-1.12.2                                       | industrialforegoing-1.12.2-1.12.13-237.jar              | None                                     |
	| L     | mysticalagriculture               | 1.7.5                                               | MysticalAgriculture-1.12.2-1.7.5.jar                    | None                                     |
	| L     | harvestcraft                      | 1.12.2zb                                            | Pam's HarvestCraft 1.12.2zg.jar                         | None                                     |
	| L     | randomthings                      | 4.2.7.4                                             | RandomThings-MC1.12.2-4.2.7.4.jar                       | None                                     |
	| L     | matteroverdrive                   | 0.7.0.0                                             | MatterOverdrive-1.12.2-0.7.1.0-universal.jar            | None                                     |
	| L     | integrationforegoing              | 1.12.2-1.10                                         | IntegrationForegoing-1.12.2-1.10.jar                    | None                                     |
	| L     | inventorysorter                   | 1.13.3+57                                           | inventorysorter-1.12.2-1.13.3+57.jar                    | None                                     |
	| L     | inventorytweaks                   | 1.64+dev.151.822d839                                | InventoryTweaks-1.64+dev.151.jar                        | None                                     |
	| L     | inzhefops_core                    | 2.0.1                                               | inzheFoPCore-v.2.0.1-1.12.2.jar                         | None                                     |
	| L     | ironchest                         | 1.12.2-7.0.67.844                                   | ironchest-1.12.2-7.0.72.847.jar                         | None                                     |
	| L     | jeiintegration                    | 1.6.0                                               | jeiintegration_1.12.2-1.6.0.jar                         | None                                     |
	| L     | jsg                               | 1.12.2-4.11.0.8                                     | jsg-1.12.2-4.11.0.8-client.jar                          | None                                     |
	| L     | jeresources                       | 0.9.3.203                                           | JustEnoughResources-1.12.2-0.9.3.203.jar                | None                                     |
	| L     | legendarytooltips                 | 1.1.9                                               | LegendaryTooltips-1.12.2-1.1.10.jar                     | None                                     |
	| L     | letsencryptcraft                  | @VERSION@                                           | letsencryptcraft-1.10.2-1.2.0.jar                       | None                                     |
	| L     | littleframes                      | 1.0.0                                               | LittleFrames_UNOFFICAL_(by_Blake)_v1.0.14_mc1.12.2.jar  | None                                     |
	| L     | llor                              | 1.1.6-mc1.12.2                                      | LLOverlayReloaded-1.1.6-mc1.12.2.jar                    | None                                     |
	| L     | logisticspipes                    | 0.10.4.44                                           | logisticspipes-0.10.4.44.jar                            | None                                     |
	| L     | lootr                             | 0.6.1                                               | lootr-1.12.2-0.6.1.jar                                  | None                                     |
	| L     | matmos                            | 1.12.2-35.4.8                                       | matmos-1.12.2-35.4.8.jar                                | None                                     |
	| L     | mcjtylib_ng                       | 3.5.4                                               | mcjtylib-1.12-3.5.4.jar                                 | None                                     |
	| L     | mcwbridges                        | 1.0.6                                               | mcw-bridges-1.0.6b-mc1.12.2.jar                         | None                                     |
	| L     | meecreeps                         | 1.3.1                                               | meecreeps-1.12-1.3.1.jar                                | None                                     |
	| L     | mekanismgenerators                | 1.12.2-9.8.3.390                                    | MekanismGenerators-1.12.2-9.8.3.390.jar                 | None                                     |
	| L     | mekanismtools                     | 1.12.2-9.8.3.390                                    | MekanismTools-1.12.2-9.8.3.390.jar                      | None                                     |
	| L     | mercurius                         | 1.0.6                                               | Mercurius-1.12.2.jar                                    | None                                     |
	| L     | modnametooltip                    | 1.10.1                                              | modnametooltip_1.12.2-1.10.1.jar                        | None                                     |
	| L     | numina                            | 1.12.2-1.0.38                                       | Numina-1.12.2-1.0.38.jar                                | None                                     |
	| L     | powersuits                        | 1.12.2-1.0.46                                       | ModularPowersuits-1.12.2-1.0.46.jar                     | None                                     |
	| L     | monk                              | 1.4                                                 | monk-mod-1.4.jar                                        | None                                     |
	| L     | stevekung's_lib                   | 1.3.0                                               | SteveKunG's-Lib-mc1.12.2-v1.3.0.jar                     | None                                     |
	| L     | moreplanets                       | 2.3.2                                               | More-Planets-1.12.2-2.3.2-GC4.0.5.jar                   | None                                     |
	| L     | moreavaritia                      | 3.5                                                 | moreavaritia-mc1.12.2-v1.5.jar                          | None                                     |
	| L     | morefurnaces                      | 1.10.5                                              | MoreFurnaces-1.12.2-1.10.6.jar                          | None                                     |
	| L     | morph                             | 7.2.0                                               | Morph-1.12.2-7.2.1.jar                                  | None                                     |
	| L     | morpheus                          | 1.12.2-3.5.106                                      | Morpheus-1.12.2-3.5.106.jar                             | None                                     |
	| L     | mrtjpcore                         | 2.1.4.43                                            | MrTJPCore-1.12.2-2.1.4.43-universal.jar                 | None                                     |
	| L     | mutantbeasts                      | 1.12.2-1.0.2                                        | MutantBeasts-1.12.2-1.0.2.jar                           | None                                     |
	| L     | mystcraft                         | 0.13.7.06                                           | mystcraft-1.12.2-0.13.7.06.jar                          | None                                     |
	| L     | mystcraft_info                    | 1.0.3.0                                             | mystcraft_info-1.12.2-1.0.5.0.jar                       | None                                     |
	| L     | naturescompass                    | 1.8.5                                               | NaturesCompass-1.12.2-1.8.5.jar                         | None                                     |
	| L     | netherportalfix                   | 5.3.17                                              | NetherPortalFix_1.12.1-5.3.17.jar                       | None                                     |
	| L     | nmsot                             | 1.2.2-mc1.12.2                                      | NoMobSpawningOnTrees-1.2.2-mc1.12.2.jar                 | None                                     |
	| L     | openmods                          | 0.12.2                                              | OpenModsLib-1.12.2-0.12.2.jar                           | None                                     |
	| L     | openblocks                        | 1.8.1                                               | OpenBlocks-1.12.2-1.8.1.jar                             | None                                     |
	| L     | packcrashinfo                     | %VERSION%                                           | packcrashinfo-1.0.1.jar                                 | None                                     |
	| L     | patchouli                         | 1.0-23.6                                            | Patchouli-1.0-23.6.jar                                  | None                                     |
	| L     | ping                              | 1.4.5                                               | Ping-1.12.2-1.4.5.jar                                   | None                                     |
	| L     | portalgun                         | 7.1.0                                               | PortalGun-1.12.2-7.1.0.jar                              | None                                     |
	| L     | powerutils                        | 1.5.3                                               | Power+Utilities.jar                                     | None                                     |
	| L     | practicallogistics2               | 3.0.8                                               | practicallogistics2-1.12.2-3.0.8-11.jar                 | None                                     |
	| L     | prefab                            | 1.3.1.7                                             | prefab-1.3.1.7.jar                                      | None                                     |
	| L     | projectred-core                   | 4.9.4.120                                           | ProjectRed-1.12.2-4.9.4.120-Base.jar                    | None                                     |
	| L     | projectred-compat                 | 1.0                                                 | ProjectRed-1.12.2-4.9.4.120-compat.jar                  | None                                     |
	| L     | projectred-integration            | 4.9.4.120                                           | ProjectRed-1.12.2-4.9.4.120-integration.jar             | None                                     |
	| L     | projectred-transmission           | 4.9.4.120                                           | ProjectRed-1.12.2-4.9.4.120-integration.jar             | None                                     |
	| L     | projectred-fabrication            | 4.9.4.120                                           | ProjectRed-1.12.2-4.9.4.120-fabrication.jar             | None                                     |
	| L     | projectred-illumination           | 4.9.4.120                                           | ProjectRed-1.12.2-4.9.4.120-lighting.jar                | None                                     |
	| L     | projectred-expansion              | 4.9.4.120                                           | ProjectRed-1.12.2-4.9.4.120-mechanical.jar              | None                                     |
	| L     | projectred-relocation             | 4.9.4.120                                           | ProjectRed-1.12.2-4.9.4.120-mechanical.jar              | None                                     |
	| L     | projectred-transportation         | 4.9.4.120                                           | ProjectRed-1.12.2-4.9.4.120-mechanical.jar              | None                                     |
	| L     | projectred-exploration            | 4.9.4.120                                           | ProjectRed-1.12.2-4.9.4.120-world.jar                   | None                                     |
	| L     | quantum_generators                | 1.3.1                                               | Quantum_Generators.jar                                  | None                                     |
	| L     | reborncore                        | 3.19.5                                              | RebornCore-1.12.2-3.19.5-universal.jar                  | None                                     |
	| L     | quantumstorage                    | 4.7.0                                               | QuantumStorage-1.12-4.7.0.jar                           | None                                     |
	| L     | quickleafdecay                    | 1.2.4                                               | QuickLeafDecay-MC1.12.1-1.2.4.jar                       | None                                     |
	| L     | recrystallizedwing                | 1.0                                                 | Re-Crystallized-Wing-1.0.jar                            | None                                     |
	| L     | rebornstorage                     | 1.0.0                                               | RebornStorage-1.12.2-3.3.4.1.jar                        | None                                     |
	| L     | redstonearsenal                   | 2.6.6                                               | RedstoneArsenal-1.12.2-2.6.6.1-universal.jar            | None                                     |
	| L     | refinedstorageaddons              | 0.4.5                                               | refinedstorageaddons-0.4.5.jar                          | None                                     |
	| L     | xreliquary                        | 1.12.2-1.3.4.796                                    | Reliquary-1.12.2-1.3.4.796.jar                          | None                                     |
	| L     | resourceloader                    | 1.5.3                                               | ResourceLoader-MC1.12.1-1.5.3.jar                       | None                                     |
	| L     | sereneseasons                     | 1.2.18                                              | SereneSeasons-1.12.2-1.2.18-universal.jar               | None                                     |
	| L     | signpost                          | 1.08.5                                              | signpost-1.12.2-1.08.5.jar                              | None                                     |
	| L     | simple-rpc                        | 1.0                                                 | simple-rpc-1.12.2-3.1.1.jar                             | None                                     |
	| L     | flashlight                        | 2.0.0                                               | simpleFlashlight-2.0.0.jar                              | None                                     |
	| L     | lteleporters                      | 1.12.2-3.0.2                                        | simpleteleporters-1.12.2-3.0.2.jar                      | None                                     |
	| L     | simplyquarries                    | 1.6.2                                               | Simply+Quarries.jar                                     | None                                     |
	| L     | stevescarts                       | 2.4.32.137                                          | StevesCarts-1.12.2-2.4.32.137.jar                       | None                                     |
	| L     | storagedrawers                    | 5.2.2                                               | StorageDrawers-1.12.2-5.4.2.jar                         | None                                     |
	| L     | sync                              | 7.1.0                                               | Sync-1.12.2-7.1.0.jar                                   | None                                     |
	| L     | tardis                            | 0.1.4A                                              | tardis-0.1.4A.jar                                       | None                                     |
	| L     | techguns                          | 2.0.2.0                                             | techguns-1.12.2-2.0.2.0_pre3.2.jar                      | None                                     |
	| L     | thaumicjei                        | 1.6.0                                               | ThaumicJEI-1.12.2-1.6.0-27.jar                          | None                                     |
	| L     | thermalcultivation                | 0.3.6                                               | ThermalCultivation-1.12.2-0.3.6.1-universal.jar         | None                                     |
	| L     | thermaldynamics                   | 2.5.6                                               | ThermalDynamics-1.12.2-2.5.6.1-universal.jar            | None                                     |
	| L     | thermalinnovation                 | 0.3.6                                               | ThermalInnovation-1.12.2-0.3.6.1-universal.jar          | None                                     |
	| L     | timber                            | 1.1.0                                               | Timber-1.12.2-1.1.0.jar                                 | None                                     |
	| L     | tinkersjei                        | 1.2                                                 | tinkersjei-1.2.jar                                      | None                                     |
	| L     | tipthescales                      | 1.0.4                                               | TipTheScales-1.12.2-1.0.4.jar                           | None                                     |
	| L     | toastcontrol                      | 1.8.1                                               | Toast Control-1.12.2-1.8.1.jar                          | None                                     |
	| L     | topaddons                         | 1.12.2-1.13.0                                       | topaddons-1.12.2-1.13.0.jar                             | None                                     |
	| L     | torched                           | 7.0.0                                               | Torched-1.12.2-7.0.0.jar                                | None                                     |
	| L     | torchslabmod                      | v1.5.2                                              | torchslabmod-1.12.2-v1.5.2.jar                          | None                                     |
	| L     | trackapi                          | 1.2                                                 | TrackAPI-1.2.jar                                        | None                                     |
	| L     | translocators                     | 2.5.2.81                                            | Translocators-1.12.2-2.5.2.81-universal.jar             | None                                     |
	| L     | travelersbackpack                 | 1.0.35                                              | TravelersBackpack-1.12.2-1.0.35.jar                     | None                                     |
	| L     | uncrafting_blacklist              | 1.12.2-0.0.0.1                                      | uncrafting-blacklist-1.12.2-0.0.0.1.jar                 | None                                     |
	| L     | universalmodcore                  | 1.1.4                                               | UniversalModCore-1.12.2-forge-1.1.4-2b81e7.jar          | None                                     |
	| L     | universalmodifiers                | 1.12.2-1.0.16.1                                     | valkyrielib-1.12.2-2.0.20.1.jar                         | None                                     |
	| L     | voicechat                         | 1.12.2-2.4.8                                        | voicechat-forge-1.12.2-2.4.8.jar                        | None                                     |
	| L     | waystones                         | 4.1.0                                               | Waystones_1.12.2-4.1.0.jar                              | None                                     |
	| L     | xaerominimap                      | 23.4.4                                              | Xaeros_Minimap_23.4.4_Forge_1.12.jar                    | None                                     |
	| L     | w2w                               | 1.2.1                                               | w2w-1.2.1.jar                                           | None                                     |
	| L     | wailaharvestability               | 1.1.12                                              | WailaHarvestability-mc1.12-1.1.12.jar                   | None                                     |
	| L     | wct                               | 3.12.97                                             | WirelessCraftingTerminal-1.12.2-3.12.97.jar             | None                                     |
	| L     | worldstripper                     | 1.6.0-1.12.2                                        | World-Stripper-1.6.0-1.12.2.jar                         | None                                     |
	| L     | wrcbe                             | 2.3.2                                               | WR-CBE-1.12.2-2.3.2.33-universal.jar                    | None                                     |
	| L     | xaeroworldmap                     | 1.30.3                                              | XaerosWorldMap_1.30.3_Forge_1.12.jar                    | None                                     |
	| L     | zerocore                          | 1.12.2-0.1.2.8                                      | zerocore-1.12.2-0.1.2.8.jar                             | None                                     |
	| L     | phosphor-lighting                 | 1.12.2-0.2.6                                        | phosphor-1.12.2-0.2.6+build50-universal.jar             | None                                     |
	| L     | reauth                            | 3.6.0                                               | reauth-3.6.0.jar                                        | None                                     |
	| L     | thebetweenlands                   | 3.9.6                                               | TheBetweenlands-3.9.6-universal.jar                     | None                                     |
	| L     | midnight                          | 0.3.5                                               | themidnight-0.3.5.jar                                   | None                                     |
	| L     | eleccoreloader                    | 1.9.453                                             | ElecCore-1.12.2-1.9.453.jar                             | None                                     |
	| L     | mysticallib                       | 1.12.2-1.13.0                                       | mysticallib-1.12.2-1.13.0.jar                           | None                                     |
	| L     | teslacorelib_registries           | 1.0.18                                              | tesla-core-lib-1.12.2-1.0.18.jar                        | None                                     |
	| L     | unidict                           | 1.12.2-2.9.7                                        | UniDict-1.12.2-2.9.7.jar                                | None                                     |

	Loaded coremods (and transformers): 
IELoadingPlugin (ImmersiveEngineering-core-0.12-98.jar)
  blusunrize.immersiveengineering.common.asm.IEClassTransformer
MekanismCoremod (Mekanism-1.12.2-9.8.3.390.jar)
  mekanism.coremod.KeybindingMigrationHelper
Uncrafting Blacklist Mixin Loading Plugin (uncrafting-blacklist-1.12.2-0.0.0.1.jar)
  
CXLibraryCore (cxlibrary-1.12.1-1.6.1.jar)
  cubex2.cxlibrary.CoreModTransformer
LittlePatchingLoader (LittleTiles_v1.5.72_mc1.12.2.jar)
  com.creativemd.littletiles.LittleTilesTransformer
EnderCorePlugin (EnderCore-1.12.2-0.5.76-core.jar)
  com.enderio.core.common.transform.EnderCoreTransformer
  com.enderio.core.common.transform.SimpleMixinPatcher
SecurityCraftLoadingPlugin ([1.12.2] SecurityCraft v1.9.6.jar)
  
PhosphorFMLLoadingPlugin (phosphor-1.12.2-0.2.6+build50-universal.jar)
  
BlurPlugin (Blur-1.0.4-14.jar)
  com.tterrag.blur.BlurTransformer
LoadingPlugin (ResourceLoader-MC1.12.1-1.5.3.jar)
  lumien.resourceloader.asm.ClassTransformer
Techguns Core (techguns-1.12.2-2.0.2.0_pre3.2.jar)
  techguns.core.TechgunsASMTransformer
LootrCore (lootr-1.12.2-0.6.1.jar)
  
CoreMod (Aroma1997Core-1.12.2-2.0.0.2.jar)
  
Inventory Tweaks Coremod (InventoryTweaks-1.64+dev.151.jar)
  invtweaks.forge.asm.ContainerTransformer
XaeroWorldMapPlugin (XaerosWorldMap_1.30.3_Forge_1.12.jar)
  xaero.map.core.transformer.ChunkTransformer
  xaero.map.core.transformer.NetHandlerPlayClientTransformer
  xaero.map.core.transformer.EntityPlayerTransformer
  xaero.map.core.transformer.AbstractClientPlayerTransformer
  xaero.map.core.transformer.WorldClientTransformer
  xaero.map.core.transformer.PlayerListTransformer
  xaero.map.core.transformer.SaveFormatTransformer
  xaero.map.core.transformer.BiomeColorHelperTransformer
  xaero.map.core.transformer.MinecraftTransformer
LoadingPlugin (RandomThings-MC1.12.2-4.2.7.4.jar)
  lumien.randomthings.asm.ClassTransformer
RandomPatches (randompatches-1.12.2-1.22.1.10.jar)
  com.therandomlabs.randompatches.core.RPTransformer
RBLoadingPlugin (RealBench-1.12.2-1.3.3.jar)
  pw.prok.realbench.asm.RBTransformer
SSLoadingPlugin (SereneSeasons-1.12.2-1.2.18-universal.jar)
  sereneseasons.asm.transformer.EntityRendererTransformer
  sereneseasons.asm.transformer.WorldTransformer
TheBetweenlandsLoadingPlugin (TheBetweenlands-3.9.6-core.jar)
  thebetweenlands.core.TheBetweenlandsClassTransformer
FTBUltimineASM (ftb-ultimine-1202.3.5.jar)
  
LogisticsPipesCoreLoader (logisticspipes-0.10.4.44.jar)
  logisticspipes.asm.LogisticsClassTransformer
ForgelinPlugin (Forgelin-1.8.4.jar)
  
midnight (themidnight-0.3.5.jar)
  com.mushroom.midnight.core.transformer.MidnightClassTransformer
CreativePatchingLoader (CreativeCore_v1.10.70_mc1.12.2.jar)
  
OpenModsCorePlugin (OpenModsLib-1.12.2-0.12.2.jar)
  openmods.core.OpenModsClassTransformer
XaeroMinimapPlugin (Xaeros_Minimap_23.4.4_Forge_1.12.jar)
  xaero.common.core.transformer.ChunkTransformer
  xaero.common.core.transformer.NetHandlerPlayClientTransformer
  xaero.common.core.transformer.EntityPlayerTransformer
  xaero.common.core.transformer.AbstractClientPlayerTransformer
  xaero.common.core.transformer.WorldClientTransformer
  xaero.common.core.transformer.EntityPlayerSPTransformer
  xaero.common.core.transformer.PlayerListTransformer
  xaero.common.core.transformer.SaveFormatTransformer
  xaero.common.core.transformer.GuiIngameForgeTransformer
  xaero.common.core.transformer.GuiBossOverlayTransformer
  xaero.common.core.transformer.ModelRendererTransformer
CTMCorePlugin (CTM-MC1.12.2-1.0.2.31.jar)
  team.chisel.ctm.client.asm.CTMTransformer
AstralCore (astralsorcery-1.12.2-1.10.27.jar)
  
HCASM (HammerLib-1.12.2-2.0.6.32.jar)
  com.zeitheron.hammercore.asm.HammerCoreTransformer
Do not report to Forge! (If you haven't disabled the FoamFix coremod, try disabling it in the config! Note that this bit of text will still appear.) (foamfix-0.10.10-1.12.2.jar)
  pl.asie.foamfix.coremod.FoamFixTransformer
MixinBooter (!mixinbooter-8.2.jar)
  
MicdoodlePlugin (Galacticraft-1.12.2-4.0.5.jar)
  micdoodle8.mods.miccore.MicdoodleTransformer
DLFMLCorePlugin (DynamicLights-1.12.2.jar)
  atomicstryker.dynamiclights.common.DLTransformer
SteveKunGLibPlugin (SteveKunG's-Lib-mc1.12.2-v1.3.0.jar)
  
	GL info: ' Vendor: 'NVIDIA Corporation' Version: '4.6.0 NVIDIA 535.98' Renderer: 'NVIDIA GeForce RTX 2060 SUPER/PCIe/SSE2'
	Launched Version: 1.12.2
	LWJGL: 2.9.4
	OpenGL: NVIDIA GeForce RTX 2060 SUPER/PCIe/SSE2 GL version 4.6.0 NVIDIA 535.98, NVIDIA Corporation
	GL Caps: Using GL 1.3 multitexturing.
Using GL 1.3 texture combiners.
Using framebuffer objects because OpenGL 3.0 is supported and separate blending is supported.
Shaders are available because OpenGL 2.1 is supported.
VBOs are available because OpenGL 1.5 is supported.

	Using VBOs: Yes
	Is Modded: Definitely; Client brand changed to 'fml,forge'
	Type: Client (map_client.txt)
	Resource Packs: 
	Current Language: English (US)
	Profiler Position: N/A (disabled)
	CPU: 8x Intel(R) Core(TM) i7-9700K CPU @ 3.60GHz
