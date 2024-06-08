# 1.20.1 Crash
The game crashed whilst initializing game Error: java.lang.RuntimeException: Could not execute entrypoint stage 'client' due to errors, provided by 'armorstatues'!

---- Minecraft Crash Report ----
// You're mean.

Time: 2024-06-08 14:54:02
Description: Initializing game

java.lang.RuntimeException: Could not execute entrypoint stage 'client' due to errors, provided by 'armorstatues'!
	at net.fabricmc.loader.impl.FabricLoaderImpl.lambda$invokeEntrypoints$2(FabricLoaderImpl.java:388)
	at net.fabricmc.loader.impl.util.ExceptionUtil.gatherExceptions(ExceptionUtil.java:33)
	at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:386)
	at net.fabricmc.loader.impl.game.minecraft.Hooks.startClient(Hooks.java:53)
	at net.minecraft.class_310.<init>(class_310.java:458)
	at net.minecraft.client.main.Main.main(Main.java:211)
	at net.fabricmc.loader.impl.game.minecraft.MinecraftGameProvider.launch(MinecraftGameProvider.java:470)
	at net.fabricmc.loader.impl.launch.knot.Knot.launch(Knot.java:74)
	at net.fabricmc.loader.impl.launch.knot.KnotClient.main(KnotClient.java:23)
	Suppressed: java.lang.NoClassDefFoundError: Could not initialize class net.minecraft.class_3929
		at net.fabricmc.fabric.api.client.screenhandler.v1.ScreenRegistry.register(ScreenRegistry.java:65)
		at team.creative.creativecore.client.CreativeCoreClient.onInitializeClient(CreativeCoreClient.java:62)
		at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:384)
		... 6 more
	Caused by: java.lang.ExceptionInInitializerError: Exception java.lang.BootstrapMethodError: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_4895 failed [in thread "Render thread"]
		at net.minecraft.class_3929.<clinit>(class_3929.java:103)
		at fuzs.armorstatues.client.ArmorStatuesClient.onClientSetup(ArmorStatuesClient.java:39)
		at fuzs.puzzleslib.impl.client.core.FabricClientModConstructor.construct(FabricClientModConstructor.java:41)
		at fuzs.puzzleslib.impl.client.core.FabricClientFactories.constructClientMod(FabricClientFactories.java:18)
		at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.lambda$construct$0(ClientModConstructor.java:62)
		at fuzs.puzzleslib.impl.core.ModContext.scheduleClientModConstruction(ModContext.java:113)
		at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.construct(ClientModConstructor.java:57)
		at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.construct(ClientModConstructor.java:39)
		at fuzs.armorstatues.client.ArmorStatuesFabricClient.onInitializeClient(ArmorStatuesFabricClient.java:11)
		... 7 more
	Suppressed: java.lang.NoClassDefFoundError: Could not initialize class net.minecraft.class_3929
		at fuzs.easyanvils.client.EasyAnvilsClient.onClientSetup(EasyAnvilsClient.java:26)
		at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.onClientSetup(ClientModConstructor.java:90)
		at fuzs.puzzleslib.impl.client.core.FabricClientModConstructor.construct(FabricClientModConstructor.java:41)
		at fuzs.puzzleslib.impl.client.core.FabricClientFactories.constructClientMod(FabricClientFactories.java:18)
		at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.lambda$construct$0(ClientModConstructor.java:62)
		at fuzs.puzzleslib.impl.core.ModContext.scheduleClientModConstruction(ModContext.java:113)
		at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.construct(ClientModConstructor.java:57)
		at fuzs.easyanvils.client.EasyAnvilsFabricClient.onInitializeClient(EasyAnvilsFabricClient.java:11)
		at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:384)
		... 6 more
	Caused by: [CIRCULAR REFERENCE: java.lang.ExceptionInInitializerError: Exception java.lang.BootstrapMethodError: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_4895 failed [in thread "Render thread"]]
	Suppressed: java.lang.NoClassDefFoundError: Could not initialize class net.minecraft.class_3929
		at fuzs.easymagic.client.EasyMagicClient.onClientSetup(EasyMagicClient.java:26)
		at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.onClientSetup(ClientModConstructor.java:90)
		at fuzs.puzzleslib.impl.client.core.FabricClientModConstructor.construct(FabricClientModConstructor.java:41)
		at fuzs.puzzleslib.impl.client.core.FabricClientFactories.constructClientMod(FabricClientFactories.java:18)
		at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.lambda$construct$0(ClientModConstructor.java:62)
		at fuzs.puzzleslib.impl.core.ModContext.scheduleClientModConstruction(ModContext.java:113)
		at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.construct(ClientModConstructor.java:57)
		at fuzs.easymagic.client.EasyMagicFabricClient.onInitializeClient(EasyMagicFabricClient.java:11)
		at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:384)
		... 6 more
	Caused by: [CIRCULAR REFERENCE: java.lang.ExceptionInInitializerError: Exception java.lang.BootstrapMethodError: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_4895 failed [in thread "Render thread"]]
	Suppressed: java.lang.NoClassDefFoundError: Could not initialize class net.minecraft.class_3929
		at net.fabricmc.fabric.api.client.screenhandler.v1.ScreenRegistry.register(ScreenRegistry.java:65)
		at supercoder79.ecotones.client.gui.EcotonesScreens.register(EcotonesScreens.java:19)
		at supercoder79.ecotones.client.gui.EcotonesScreens.init(EcotonesScreens.java:13)
		at supercoder79.ecotones.EcotonesClient.onInitializeClient(EcotonesClient.java:119)
		at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:384)
		... 6 more
	Caused by: [CIRCULAR REFERENCE: java.lang.ExceptionInInitializerError: Exception java.lang.BootstrapMethodError: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_4895 failed [in thread "Render thread"]]
	Suppressed: java.lang.NoClassDefFoundError: Could not initialize class net.minecraft.class_3929
		at wraith.fwaystones.registry.CustomScreenRegistry.registerScreens(CustomScreenRegistry.java:14)
		at wraith.fwaystones.client.WaystonesClient.onInitializeClient(WaystonesClient.java:30)
		at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:384)
		... 6 more
	Caused by: [CIRCULAR REFERENCE: java.lang.ExceptionInInitializerError: Exception java.lang.BootstrapMethodError: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_4895 failed [in thread "Render thread"]]
	Suppressed: java.lang.NoClassDefFoundError: Could not initialize class net.minecraft.class_3929
		at net.fabricmc.fabric.api.client.screenhandler.v1.ScreenRegistry.register(ScreenRegistry.java:65)
		at com.iamshift.pickablevillagers.PickableVillagersClient.onInitializeClient(PickableVillagersClient.java:39)
		at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:384)
		... 6 more
	Caused by: [CIRCULAR REFERENCE: java.lang.ExceptionInInitializerError: Exception java.lang.BootstrapMethodError: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_4895 failed [in thread "Render thread"]]
	Suppressed: java.lang.NoClassDefFoundError: Could not initialize class net.minecraft.class_3929
		at com.tiviacz.travelersbackpack.TravelersBackpackClient.onInitializeClient(TravelersBackpackClient.java:49)
		at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:384)
		... 6 more
	Caused by: [CIRCULAR REFERENCE: java.lang.ExceptionInInitializerError: Exception java.lang.BootstrapMethodError: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_4895 failed [in thread "Render thread"]]
	Suppressed: java.lang.NoClassDefFoundError: Could not initialize class net.minecraft.class_3929
		at com.lion.villagersplus.fabric.VillagersPlusClientFabric.onInitializeClient(VillagersPlusClientFabric.java:25)
		at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:384)
		... 6 more
	Caused by: [CIRCULAR REFERENCE: java.lang.ExceptionInInitializerError: Exception java.lang.BootstrapMethodError: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_4895 failed [in thread "Render thread"]]
	Suppressed: java.lang.NoClassDefFoundError: Could not initialize class net.minecraft.class_3929
		at fuzs.visualworkbench.client.VisualWorkbenchClient.onClientSetup(VisualWorkbenchClient.java:15)
		at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.onClientSetup(ClientModConstructor.java:90)
		at fuzs.puzzleslib.impl.client.core.FabricClientModConstructor.construct(FabricClientModConstructor.java:41)
		at fuzs.puzzleslib.impl.client.core.FabricClientFactories.constructClientMod(FabricClientFactories.java:18)
		at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.lambda$construct$0(ClientModConstructor.java:62)
		at fuzs.puzzleslib.impl.core.ModContext.scheduleClientModConstruction(ModContext.java:113)
		at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.construct(ClientModConstructor.java:57)
		at fuzs.visualworkbench.client.VisualWorkbenchFabricClient.onInitializeClient(VisualWorkbenchFabricClient.java:11)
		at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:384)
		... 6 more
	Caused by: [CIRCULAR REFERENCE: java.lang.ExceptionInInitializerError: Exception java.lang.BootstrapMethodError: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_4895 failed [in thread "Render thread"]]
Caused by: java.lang.BootstrapMethodError: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_4895 failed
	at net.minecraft.class_3929.<clinit>(class_3929.java:103)
	at fuzs.armorstatues.client.ArmorStatuesClient.onClientSetup(ArmorStatuesClient.java:39)
	at fuzs.puzzleslib.impl.client.core.FabricClientModConstructor.construct(FabricClientModConstructor.java:41)
	at fuzs.puzzleslib.impl.client.core.FabricClientFactories.constructClientMod(FabricClientFactories.java:18)
	at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.lambda$construct$0(ClientModConstructor.java:62)
	at fuzs.puzzleslib.impl.core.ModContext.scheduleClientModConstruction(ModContext.java:113)
	at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.construct(ClientModConstructor.java:57)
	at fuzs.puzzleslib.api.client.core.v1.ClientModConstructor.construct(ClientModConstructor.java:39)
	at fuzs.armorstatues.client.ArmorStatuesFabricClient.onInitializeClient(ArmorStatuesFabricClient.java:11)
	at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:384)
	... 6 more
Caused by: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_4895 failed
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.getPostMixinClassByteArray(KnotClassDelegate.java:427)
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.tryLoadClass(KnotClassDelegate.java:323)
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.loadClass(KnotClassDelegate.java:218)
	at net.fabricmc.loader.impl.launch.knot.KnotClassLoader.loadClass(KnotClassLoader.java:119)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:525)
	... 16 more
Caused by: org.spongepowered.asm.mixin.transformer.throwables.MixinTransformerError: An unexpected critical error was encountered
	at org.spongepowered.asm.mixin.transformer.MixinProcessor.applyMixins(MixinProcessor.java:392)
	at org.spongepowered.asm.mixin.transformer.MixinTransformer.transformClass(MixinTransformer.java:234)
	at org.spongepowered.asm.mixin.transformer.MixinTransformer.transformClassBytes(MixinTransformer.java:202)
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.getPostMixinClassByteArray(KnotClassDelegate.java:422)
	... 20 more
Caused by: org.spongepowered.asm.mixin.injection.throwables.InjectionError: Critical injection failure: Redirector renderBg(Lnet/minecraft/class_8064;Lnet/minecraft/class_1703;Lnet/minecraft/class_332;FII)V in mixins.brb-common.json:SmithingScreenMixin from mod brb failed injection check, (0/1) succeeded. Scanned 1 target(s). Using refmap brb-common-refmap.json
	at org.spongepowered.asm.mixin.injection.struct.InjectionInfo.postInject(InjectionInfo.java:468)
	at org.spongepowered.asm.mixin.transformer.MixinTargetContext.applyInjections(MixinTargetContext.java:1384)
	at org.spongepowered.asm.mixin.transformer.MixinApplicatorStandard.applyInjections(MixinApplicatorStandard.java:1062)
	at org.spongepowered.asm.mixin.transformer.MixinApplicatorStandard.applyMixin(MixinApplicatorStandard.java:402)
	at org.spongepowered.asm.mixin.transformer.MixinApplicatorStandard.apply(MixinApplicatorStandard.java:327)
	at org.spongepowered.asm.mixin.transformer.TargetClassContext.apply(TargetClassContext.java:422)
	at org.spongepowered.asm.mixin.transformer.TargetClassContext.applyMixins(TargetClassContext.java:403)
	at org.spongepowered.asm.mixin.transformer.MixinProcessor.applyMixins(MixinProcessor.java:363)
	... 23 more


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Thread: Render thread
Stacktrace:
	at net.fabricmc.loader.impl.FabricLoaderImpl.lambda$invokeEntrypoints$2(FabricLoaderImpl.java:388)
	at net.fabricmc.loader.impl.util.ExceptionUtil.gatherExceptions(ExceptionUtil.java:33)
	at net.fabricmc.loader.impl.FabricLoaderImpl.invokeEntrypoints(FabricLoaderImpl.java:386)
	at net.fabricmc.loader.impl.game.minecraft.Hooks.startClient(Hooks.java:53)
	at net.minecraft.class_310.<init>(class_310.java:458)

-- Initialization --
Details:
	Modules: 
		ADVAPI32.dll:Advanced Windows 32 Base API:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		COMCTL32.dll:User Experience Controls Library:6.10 (WinBuild.160101.0800):Microsoft Corporation
		CRYPT32.dll:Crypto API32:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		CRYPTBASE.dll:Base cryptographic API DLL:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		CRYPTSP.dll:Cryptographic Service Provider API:10.0.22621.2506 (WinBuild.160101.0800):Microsoft Corporation
		DBGHELP.DLL:Windows Image Helper:10.0.22621.2506 (WinBuild.160101.0800):Microsoft Corporation
		DNSAPI.dll:DNS Client API DLL:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		GDI32.dll:GDI Client DLL:10.0.22621.3085 (WinBuild.160101.0800):Microsoft Corporation
		IMM32.DLL:Multi-User Windows IMM32 API Client DLL:10.0.22621.3374 (WinBuild.160101.0800):Microsoft Corporation
		IPHLPAPI.DLL:IP Helper API:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		KERNEL32.DLL:Windows NT BASE API Client DLL:10.0.22621.3374 (WinBuild.160101.0800):Microsoft Corporation
		KERNELBASE.dll:Windows NT BASE API Client DLL:10.0.22621.3374 (WinBuild.160101.0800):Microsoft Corporation
		MpOav.dll:IOfficeAntiVirus Module:4.18.24040.4 (aa69a05caa955e1cebcc4d2dd249082d41b510c2):Microsoft Corporation
		NSI.dll:NSI User-mode interface DLL:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		NTASN1.dll:Microsoft ASN.1 API:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		OLEAUT32.dll:OLEAUT32.DLL:10.0.22621.3527 (WinBuild.160101.0800):Microsoft Corporation
		Ole32.dll:Microsoft OLE for Windows:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		POWRPROF.dll:Power Profile Helper DLL:10.0.22621.3374 (WinBuild.160101.0800):Microsoft Corporation
		PSAPI.DLL:Process Status Helper:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		Pdh.dll:Windows Performance Data Helper DLL:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		RPCRT4.dll:Remote Procedure Call Runtime:10.0.22621.2506 (WinBuild.160101.0800):Microsoft Corporation
		SHCORE.dll:SHCORE:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		SHELL32.dll:Windows Shell Common Dll:10.0.22621.2792 (WinBuild.160101.0800):Microsoft Corporation
		UMPDC.dll:User Mode Power Dependency Coordinator:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		USER32.dll:Multi-User Windows USER API Client DLL:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		USERENV.dll:Userenv:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		VCRUNTIME140.dll:Microsoft® C Runtime Library:14.29.30139.0 built by: vcwrkspc:Microsoft Corporation
		VERSION.dll:Version Checking and File Installation Libraries:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		WINHTTP.dll:Windows HTTP Services:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		WINMM.dll:MCI API DLL:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		WS2_32.dll:Windows Socket 2.0 32-Bit DLL:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		WSOCK32.dll:Windows Socket 32-Bit DLL:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		amsi.dll:Anti-Malware Scan Interface:10.0.22621.3527 (WinBuild.160101.0800):Microsoft Corporation
		apphelp.dll:Application Compatibility Client Library:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		awt.dll:OpenJDK Platform binary:17.0.8.0:Microsoft
		bcrypt.dll:Windows Cryptographic Primitives Library:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		bcryptPrimitives.dll:Windows Cryptographic Primitives Library:10.0.22621.3374 (WinBuild.160101.0800):Microsoft Corporation
		clbcatq.dll:COM+ Configuration Catalog:2001.12.10941.16384 (WinBuild.160101.0800):Microsoft Corporation
		combase.dll:Microsoft COM for Windows:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		dbgcore.DLL:Windows Core Debugging Helpers:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		dhcpcsvc.DLL:DHCP Client Service:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		dhcpcsvc6.DLL:DHCPv6 Client:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		fwpuclnt.dll:FWP/IPsec User-Mode API:10.0.22621.2506 (WinBuild.160101.0800):Microsoft Corporation
		gdi32full.dll:GDI Client DLL:10.0.22621.3527 (WinBuild.160101.0800):Microsoft Corporation
		glfw.dll:GLFW 3.4.0 DLL:3.4.0:GLFW
		java.dll:OpenJDK Platform binary:17.0.8.0:Microsoft
		javaw.exe:OpenJDK Platform binary:17.0.8.0:Microsoft
		jemalloc.dll
		jimage.dll:OpenJDK Platform binary:17.0.8.0:Microsoft
		jli.dll:OpenJDK Platform binary:17.0.8.0:Microsoft
		jna1257121228413592166.dll:JNA native library:6.1.4:Java(TM) Native Access (JNA)
		jsvml.dll:OpenJDK Platform binary:17.0.8.0:Microsoft
		jvm.dll:OpenJDK 64-Bit server VM:17.0.8.0:Microsoft
		kernel.appcore.dll:AppModel API Host:10.0.22621.2715 (WinBuild.160101.0800):Microsoft Corporation
		lwjgl.dll
		management.dll:OpenJDK Platform binary:17.0.8.0:Microsoft
		management_ext.dll:OpenJDK Platform binary:17.0.8.0:Microsoft
		msvcp140.dll:Microsoft® C Runtime Library:14.29.30139.0 built by: vcwrkspc:Microsoft Corporation
		msvcp_win.dll:Microsoft® C Runtime Library:10.0.22621.3374 (WinBuild.160101.0800):Microsoft Corporation
		msvcrt.dll:Windows NT CRT DLL:7.0.22621.2506 (WinBuild.160101.0800):Microsoft Corporation
		mswsock.dll:Microsoft Windows Sockets 2.0 Service Provider:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		napinsp.dll:E-mail Naming Shim Provider:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		ncrypt.dll:Windows NCrypt Router:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		net.dll:OpenJDK Platform binary:17.0.8.0:Microsoft
		nio.dll:OpenJDK Platform binary:17.0.8.0:Microsoft
		nlansp_c.dll:NLA Namespace Service Provider DLL:10.0.22621.3527 (WinBuild.160101.0800):Microsoft Corporation
		ntdll.dll:NT Layer DLL:10.0.22621.3374 (WinBuild.160101.0800):Microsoft Corporation
		ntmarta.dll:Windows NT MARTA provider:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		perfos.dll:Windows System Performance Objects DLL:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		perfproc.dll:Windows System Process Performance Objects DLL:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		pfclient.dll:SysMain Client:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		pnrpnsp.dll:PNRP Name Space Provider:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		profapi.dll:User Profile Basic API:10.0.22621.3527 (WinBuild.160101.0800):Microsoft Corporation
		rasadhlp.dll:Remote Access AutoDial Helper:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		rsaenh.dll:Microsoft Enhanced Cryptographic Provider:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		sechost.dll:Host for SCM/SDDL/LSA Lookup APIs:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		shlwapi.dll:Shell Light-weight Utility Library:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		sunmscapi.dll:OpenJDK Platform binary:17.0.8.0:Microsoft
		ucrtbase.dll:Microsoft® C Runtime Library:10.0.22621.3374 (WinBuild.160101.0800):Microsoft Corporation
		vcruntime140_1.dll:Microsoft® C Runtime Library:14.29.30139.0 built by: vcwrkspc:Microsoft Corporation
		verify.dll:OpenJDK Platform binary:17.0.8.0:Microsoft
		win32u.dll:Win32u:10.0.22621.3527 (WinBuild.160101.0800):Microsoft Corporation
		windows.storage.dll:Microsoft WinRT Storage API:10.0.22621.3527 (WinBuild.160101.0800):Microsoft Corporation
		winrnr.dll:LDAP RnR Provider DLL:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		wintypes.dll:Windows Base Types DLL:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		wshbth.dll:Windows Sockets Helper DLL:10.0.22621.3374 (WinBuild.160101.0800):Microsoft Corporation
		wshunix.dll:AF_UNIX Winsock2 Helper DLL:10.0.22621.1 (WinBuild.160101.0800):Microsoft Corporation
		zip.dll:OpenJDK Platform binary:17.0.8.0:Microsoft
Stacktrace:
	at net.minecraft.client.main.Main.main(Main.java:211)
	at net.fabricmc.loader.impl.game.minecraft.MinecraftGameProvider.launch(MinecraftGameProvider.java:470)
	at net.fabricmc.loader.impl.launch.knot.Knot.launch(Knot.java:74)
	at net.fabricmc.loader.impl.launch.knot.KnotClient.main(KnotClient.java:23)

-- System Details --
Details:
	Minecraft Version: 1.20.1
	Minecraft Version ID: 1.20.1
	Operating System: Windows 11 (amd64) version 10.0
	Java Version: 17.0.8, Microsoft
	Java VM Version: OpenJDK 64-Bit Server VM (mixed mode), Microsoft
	Memory: 534357144 bytes (509 MiB) / 1124073472 bytes (1072 MiB) up to 12985565184 bytes (12384 MiB)
	CPUs: 12
	Processor Vendor: AuthenticAMD
	Processor Name: AMD Ryzen 5 3600 6-Core Processor              
	Identifier: AuthenticAMD Family 23 Model 113 Stepping 0
	Microarchitecture: Zen 2
	Frequency (GHz): 3.59
	Number of physical packages: 1
	Number of physical CPUs: 6
	Number of logical CPUs: 12
	Graphics card #0 name: NVIDIA GeForce RTX 3050
	Graphics card #0 vendor: NVIDIA (0x10de)
	Graphics card #0 VRAM (MB): 4095.00
	Graphics card #0 deviceId: 0x2507
	Graphics card #0 versionInfo: DriverVersion=32.0.15.5599
	Memory slot #0 capacity (MB): 16384.00
	Memory slot #0 clockSpeed (GHz): 3.20
	Memory slot #0 type: DDR4
	Memory slot #1 capacity (MB): 16384.00
	Memory slot #1 clockSpeed (GHz): 3.20
	Memory slot #1 type: DDR4
	Virtual memory max (MB): 37514.63
	Virtual memory used (MB): 14796.65
	Swap memory total (MB): 4864.00
	Swap memory used (MB): 9.83
	JVM Flags: 4 total; -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -Xss1M -Xmx12384m -Xms256m
	Fabric Mods: 
		achiopt: AchievementOptimizer 1.0.1
		additionalstructures: Additional Structures 4.2.1
		advancementinfo: AdvancementInfo 1.20-fabric0.83.0-1.4
		advancementplaques: Advancement Plaques 1.4.11
		alwaysawitherskull: Always a Wither Skull 3.2
		ambientenvironment: Ambient Environment 11.0.0.1
		ambientsounds: AmbientSounds 6.0.1
		amplified_nether: Amplified Nether 1.2.5
		anvilrepairing: AnvilRepairing 4.0.7
		anvilrestoration: Anvil Restoration 2.2
		appleskin: AppleSkin 2.5.1+mc1.20
		architectury: Architectury 9.2.14
		armorstatues: Armor Statues 8.0.6
		ash_api: Ash API 3.0.2+1.20.1
		attributefix: AttributeFix 21.0.4
		badpackets: Bad Packets 0.4.3
		balm-fabric: Balm 7.3.4
			kuma_api: KumaAPI 20.1.6
		bcc: BetterCompatibilityChecker 4.0.8
		beaconoverhaul: Beacon Overhaul 1.8.4+1.20
			reach-entity-attributes: Reach Entity Attributes 2.4.0
		bedbenefits: BedBenefits 13.0.3
		beekeeperhut: Friends&Foes - Beekeeper Hut 2.0.0
		better-trim-tooltips: Better Trim Tooltips 1.0.1
		better_climbing: Better Climbing 3
		betteradvancements: Better Advancements 0.3.2.162
		betteranimationscollection: Better Animations Collection 8.0.0
		betterbeaconplacement: Better Beacon Placement 3.3
		betterbeds: Better Beds 1.3.0
		betterchunkloading: Better chunk loading mod 1.20.1-4.3
		betterconduitplacement: Better Conduit Placement 3.2
		betterdeserttemples: YUNG's Better Desert Temples 1.20-Fabric-3.0.3
			org_reflections_reflections: reflections 0.10.2
		betterdungeons: YUNG's Better Dungeons 1.20-Fabric-4.0.4
		betterendisland: YUNG's Better End Island 1.20-Fabric-2.0.6
		betterf3: BetterF3 7.0.2
		betterfortresses: YUNG's Better Nether Fortresses 1.20-Fabric-2.0.6
		betterfpsdist: Better FPS distance Mod 1.20.1-4.3
		betterjungletemples: YUNG's Better Jungle Temples 1.20-Fabric-2.0.5
		bettermineshafts: YUNG's Better Mineshafts 1.20-Fabric-4.0.4
		bettermounthud: Better Mount HUD 1.2.2
		betteroceanmonuments: YUNG's Better Ocean Monuments 1.20-Fabric-3.0.4
		bettersmithingtable: BetterSmithingTable 1.1.0
		betterstats: Better Statistics Screen 3.9.7+fabric-1.20.1
			tcdcommons: TCD Commons API 3.9.6+fabric-1.20.1
		betterstrongholds: YUNG's Better Strongholds 1.20-Fabric-4.0.3
		betterthirdperson: Better Third Person 1.9.0
		betterwitchhuts: YUNG's Better Witch Huts 1.20-Fabric-3.0.3
		biomemusic: Biome Music Mod 1.20.1-2.3
		biomesize: Biome size Mod 1.20.1-1.3
		blastingraw: BlastingRaw 1.20.1-1-fabric
		blastingsand: Smelting Sand In Blast a Furnace 1.20.1-11-fabric
		blur: Blur (Fabric) 3.1.0
		boatbreakfix: Boat Break Fix 1.0.2
		boatiview: Boat Item View Fabric 0.0.5
		bobby: Bobby 5.0.1
			com_typesafe_config: config 1.4.2
			io_leangen_geantyref_geantyref: geantyref 1.3.13
			org_spongepowered_configurate-core: configurate-core 4.1.2
			org_spongepowered_configurate-hocon: configurate-hocon 4.1.2
		bookshelf: Bookshelf 20.1.11
		borderlessmining: Borderless Mining 1.1.8+1.20.1
		brb: Better Recipe Book 1.10.0+1.20.0-1
		bushierflowers: Bushier Flowers 0.0.3-1.20.1
		bypass_anvil_restriction: Bypass Anvil Restriction 1.0.7+1.20.1
			ch_skyfy_tomlconfiglib_toml-config-lib: toml-config-lib 1.0.4
			io_github_microutils_kotlin-logging-jvm: kotlin-logging-jvm 3.0.5
			net_peanuuutz_tomlkt-jvm: tomlkt-jvm 0.2.0
		callablehorsefabric: CallableHorseFabric 1.0.0
			porting_lib_core: Porting Lib Core 2.3.0+1.20.1
		cameraoverhaul: Camera Overhaul 1.4.0-fabric-universal
		camerautils: Camera Utils 1.20.1-1.0.5
		cerbons_api: Cerbons API 1.1.0
			cardinal-components-base: Cardinal Components API (base) 5.2.2
			cardinal-components-world: Cardinal Components API (worlds) 5.2.2
		charmofundying: Charm of Undying 6.5.0+1.20.1
			spectrelib: SpectreLib 0.13.15+1.20.1
		chas: Craftable Horse Armour & Saddle 1.20
		cherishedworlds: Cherished Worlds 6.1.6+1.20.1
		chunksending: Chunksending Mod 1.20.1-2.8
		chunksfadein: Chunks Fade In 1.0.6-1.20.1
			com_moandjiezana_toml_toml4j: toml4j 0.7.2
			crowdin-translate: CrowdinTranslate 1.4+1.19.3
		chunky: Chunky 1.3.146
		clayblasting: ClayBlasting 1.20.1-0-fabric
		clean_tooltips: Clean Tooltips 1.0
		clickadv: Clickable Advancements Mod 1.20.1-3.8
		cloth-config: Cloth Config v11 11.1.118
			cloth-basic-math: cloth-basic-math 0.6.1
		clumps: Clumps 12.0.0.4
		collective: Collective 7.61
		colorize: Colorize 1.9.0
		combatroll: Combat Roll 1.3.2+1.20.1
		configureddefaults: Configured Defaults 8.0.1
		connectiblechains: Connectible Chains 2.2.1+1.20.1
		connectivity: Connectivity Mod 1.20.1-5.5
		continue: Continue 1.2.2+1.20
		controlling: Controlling For Fabric 12.0.2
		couplings: Couplings 1.9.5+1.20
		craftablesaddle: Craftable Saddle 1.20.1-1.6.4-[FABRIC]
		craftsaddles: Craft Saddles 1.0.10
		crafttweaker: CraftTweaker 14.0.40
		crawl: Crawl 0.12.0
			mm: Manningham Mills 2.3
		creativecore: CreativeCore 2.11.30
			net_minecraftforge_eventbus: eventbus 6.0.3
		creeperoverhaul: Creeper Overhaul 3.0.2
		cristellib: Cristel Lib 1.1.5
			blue_endless_jankson: jankson 1.2.3
		cryingportals: Crying Portals 2.7
		ctov: ChoiceTheorem's Overhauled Village 3.4.3
		cupboard: cupboard 1.20.1-2.6
		darksmithing: DarkSmithing - Smithing Template Recipes (for Trims) 1.0.6
		deepslatecutting: Deepslate Cutting 1.7.0
		distinguishedpotions: Distinguished Potions 8.0.2
		doubledoors: Double Doors 5.7
		dragondropselytra: Dragon Drops Elytra 3.3
		dragonfight: Dragonfight Mod 1.20.1-4.5
		durabilitytooltip: Durability Tooltip 1.1.5
		easiervillagertrading: EasierVillagerTrading 1.20-fabric0.83.0-1.5.4
			gbfabrictools: GBfabrictools 1.3.5+1.20
		easyanvils: Easy Anvils 8.0.2
		easyelytratakeoff: Easy Elytra Takeoff 4.2
		easymagic: Easy Magic 8.0.1
		easyshulkerboxes: Easy Shulker Boxes 8.0.2
			puzzlesapi: Puzzles Api 8.1.6
				cardinal-components-entity: Cardinal Components API (entities) 5.2.2
				puzzlesaccessapi: Puzzles Access Api 8.0.9
		eatinganimationid: Eating Animation 1.20+1.9.61
		eco: Ecospherical Expansion 2.4.6
		ecologics: Ecologics 2.2.0
		ecotones: Ecotones 0.9.3
		effectdescriptions: Effect Descriptions 8.0.2
		elytraslot: Elytra Slot 6.3.0+1.20.1
		enchdesc: EnchantmentDescriptions 17.0.16
		endermanoverhaul: Enderman Overhaul 1.0.4
		endrem: End Remastered 5.2.4
		enhancedvisuals: EnhancedVisuals 1.8.1
		entity_model_features: Entity Model Features 2.0.2
		entity_texture_features: Entity Texture Features 6.0.1
			org_apache_httpcomponents_httpmime: httpmime 4.5.10
		entityculling: EntityCulling 1.6.5
		equipmentcompare: Equipment Compare 1.3.8
		expanded_ecosphere: Expanded Ecosphere 3.2.4
		expandedworld: Expanded World 1.2.0
		explorations: Explorations 1.20.1-1.5.2
		explorerscompass: Explorer's Compass 1.20.1-2.2.3-fabric
		explorify: Explorify v1.4.0
		extendedbonemeal: Extended Bone Meal 3.4
		fabric-api: Fabric API 0.92.2+1.20.1
			fabric-api-base: Fabric API Base 0.4.31+1802ada577
			fabric-api-lookup-api-v1: Fabric API Lookup API (v1) 1.6.36+1802ada577
			fabric-biome-api-v1: Fabric Biome API (v1) 13.0.13+1802ada577
			fabric-block-api-v1: Fabric Block API (v1) 1.0.11+1802ada577
			fabric-block-view-api-v2: Fabric BlockView API (v2) 1.0.1+1802ada577
			fabric-blockrenderlayer-v1: Fabric BlockRenderLayer Registration (v1) 1.1.41+1802ada577
			fabric-client-tags-api-v1: Fabric Client Tags 1.1.2+1802ada577
			fabric-command-api-v1: Fabric Command API (v1) 1.2.34+f71b366f77
			fabric-command-api-v2: Fabric Command API (v2) 2.2.13+1802ada577
			fabric-commands-v0: Fabric Commands (v0) 0.2.51+df3654b377
			fabric-containers-v0: Fabric Containers (v0) 0.1.64+df3654b377
			fabric-content-registries-v0: Fabric Content Registries (v0) 4.0.11+1802ada577
			fabric-convention-tags-v1: Fabric Convention Tags 1.5.5+1802ada577
			fabric-crash-report-info-v1: Fabric Crash Report Info (v1) 0.2.19+1802ada577
			fabric-data-attachment-api-v1: Fabric Data Attachment API (v1) 1.0.0+de0fd6d177
			fabric-data-generation-api-v1: Fabric Data Generation API (v1) 12.3.4+1802ada577
			fabric-dimensions-v1: Fabric Dimensions API (v1) 2.1.54+1802ada577
			fabric-entity-events-v1: Fabric Entity Events (v1) 1.6.0+1c78457f77
			fabric-events-interaction-v0: Fabric Events Interaction (v0) 0.6.2+1802ada577
			fabric-events-lifecycle-v0: Fabric Events Lifecycle (v0) 0.2.63+df3654b377
			fabric-game-rule-api-v1: Fabric Game Rule API (v1) 1.0.40+1802ada577
			fabric-item-api-v1: Fabric Item API (v1) 2.1.28+1802ada577
			fabric-item-group-api-v1: Fabric Item Group API (v1) 4.0.12+1802ada577
			fabric-key-binding-api-v1: Fabric Key Binding API (v1) 1.0.37+1802ada577
			fabric-keybindings-v0: Fabric Key Bindings (v0) 0.2.35+df3654b377
			fabric-lifecycle-events-v1: Fabric Lifecycle Events (v1) 2.2.22+1802ada577
			fabric-loot-api-v2: Fabric Loot API (v2) 1.2.1+1802ada577
			fabric-loot-tables-v1: Fabric Loot Tables (v1) 1.1.45+9e7660c677
			fabric-message-api-v1: Fabric Message API (v1) 5.1.9+1802ada577
			fabric-mining-level-api-v1: Fabric Mining Level API (v1) 2.1.50+1802ada577
			fabric-model-loading-api-v1: Fabric Model Loading API (v1) 1.0.3+1802ada577
			fabric-models-v0: Fabric Models (v0) 0.4.2+9386d8a777
			fabric-networking-api-v1: Fabric Networking API (v1) 1.3.11+1802ada577
			fabric-networking-v0: Fabric Networking (v0) 0.3.51+df3654b377
			fabric-object-builder-api-v1: Fabric Object Builder API (v1) 11.1.3+1802ada577
			fabric-particles-v1: Fabric Particles (v1) 1.1.2+1802ada577
			fabric-recipe-api-v1: Fabric Recipe API (v1) 1.0.21+1802ada577
			fabric-registry-sync-v0: Fabric Registry Sync (v0) 2.3.3+1802ada577
			fabric-renderer-api-v1: Fabric Renderer API (v1) 3.2.1+1802ada577
			fabric-renderer-indigo: Fabric Renderer - Indigo 1.5.2+85287f9f77
			fabric-renderer-registries-v1: Fabric Renderer Registries (v1) 3.2.46+df3654b377
			fabric-rendering-data-attachment-v1: Fabric Rendering Data Attachment (v1) 0.3.37+92a0d36777
			fabric-rendering-fluids-v1: Fabric Rendering Fluids (v1) 3.0.28+1802ada577
			fabric-rendering-v0: Fabric Rendering (v0) 1.1.49+df3654b377
			fabric-rendering-v1: Fabric Rendering (v1) 3.0.8+1802ada577
			fabric-resource-conditions-api-v1: Fabric Resource Conditions API (v1) 2.3.8+1802ada577
			fabric-resource-loader-v0: Fabric Resource Loader (v0) 0.11.10+1802ada577
			fabric-screen-api-v1: Fabric Screen API (v1) 2.0.8+1802ada577
			fabric-screen-handler-api-v1: Fabric Screen Handler API (v1) 1.3.30+1802ada577
			fabric-sound-api-v1: Fabric Sound API (v1) 1.0.13+1802ada577
			fabric-transfer-api-v1: Fabric Transfer API (v1) 3.3.5+8dd72ea377
			fabric-transitive-access-wideners-v1: Fabric Transitive Access Wideners (v1) 4.3.1+1802ada577
		fabric-language-kotlin: Fabric Language Kotlin 1.11.0+kotlin.2.0.0
			org_jetbrains_kotlin_kotlin-reflect: kotlin-reflect 2.0.0
			org_jetbrains_kotlin_kotlin-stdlib: kotlin-stdlib 2.0.0
			org_jetbrains_kotlin_kotlin-stdlib-jdk7: kotlin-stdlib-jdk7 2.0.0
			org_jetbrains_kotlin_kotlin-stdlib-jdk8: kotlin-stdlib-jdk8 2.0.0
			org_jetbrains_kotlinx_atomicfu-jvm: atomicfu-jvm 0.24.0
			org_jetbrains_kotlinx_kotlinx-coroutines-core-jvm: kotlinx-coroutines-core-jvm 1.8.1
			org_jetbrains_kotlinx_kotlinx-coroutines-jdk8: kotlinx-coroutines-jdk8 1.8.1
			org_jetbrains_kotlinx_kotlinx-datetime-jvm: kotlinx-datetime-jvm 0.6.0
			org_jetbrains_kotlinx_kotlinx-serialization-cbor-jvm: kotlinx-serialization-cbor-jvm 1.6.3
			org_jetbrains_kotlinx_kotlinx-serialization-core-jvm: kotlinx-serialization-core-jvm 1.6.3
			org_jetbrains_kotlinx_kotlinx-serialization-json-jvm: kotlinx-serialization-json-jvm 1.6.3
		fabric-skinmc: SkinMC Mod 1.20-1.0.0
		fabricloader: Fabric Loader 0.15.11
			mixinextras: MixinExtras 0.3.5
		fallingleaves: Falling Leaves 1.15.6
		fallingtree: FallingTree 4.3.4
		fastquit: FastQuit 3.0.0+1.20+
		faux-custom-entity-data: Faux-Custom-Entity-Data 6.0.1
		firstperson: FirstPerson 2.4.1
		fixedanvilrepaircost: Fixed Anvil Repair Cost 3.3
		flatbedrock: Flat Bedrock 3.0.1-build.18+mc1.20.1
		flowerpatch: Flower Patch 3.1.0
		flowerymooblooms: Friends&Foes - Flowery Mooblooms 2.0.1
		forgeconfigapiport: Forge Config API Port 8.0.0
		formations: Formations 1.0.2
		formationsnether: Formations Nether 1.0.4
		formationsoverworld: Formations Overworld 1.0.3
		fpsreducer: FPS Reducer 1.20-2.5
		framework: Framework 0.6.16
			org_javassist_javassist: javassist 3.29.2-GA
		friendlyfire: FriendlyFire 18.0.7
		friendsandfoes: Friends&Foes 2.0.10
		ftblibrary: FTB Library 2001.2.2
		ftbultimine: FTB Ultimine 2001.1.5
		ftbxmodcompat: FTB XMod Compat 2.1.1
		furnacerecycle: Furnace Recycle 2.2
		fwaystones: Fabric Waystones 3.3.2+mc1.20.1
		gamemenuremovegfarb: Game Menu Remove GFARB 2.1.2
		geckolib: GeckoLib 4 4.4.5
			com_eliotlash_mclib_mclib: mclib 20
		geophilic: Geophilic v2.2.0-mc1.20u1.20.2
		goblintraders: Goblin Traders 1.9.3
		grindenchantments: Grind Enchantments 3.1.2+1.20
			codec-config-api: Codec Config API 1.0.2+1.19.3
		harvestwithease: Harvest with ease 8.0.1.0
		healingcampfire: Healing Campfire 5.3
		herdspanic: Herds Panic 1.1.0
		hiddenrecipebook: Hidden Recipe Book 4.6
		highlighter: Highlighter 1.1.9
		horseexpert: Horse Expert 8.1.1
		horsestatsvanilla: Horse Stats Vanilla 4.3.0
			libgui: LibGui 8.0.0+1.20
				jankson: Jankson 5.0.1+j1.2.2
				libninepatch: LibNinePatch 1.2.0
		horsestonks: Horse Stonks 1.0.1
		iceberg: Iceberg 1.1.18
		immediatelyfast: ImmediatelyFast 1.2.17+1.20.4
			net_lenni0451_reflect: Reflect 1.3.3
		imst: Immersive structures 2.1.0
		incendium: Incendium 5.3.5
		indium: Indium 1.0.30+mc1.20.4
		infinitetrading: Infinite Trading 4.3
		inventoryhud: Inventory HUD + 3.4.18
		inventorysorter: Inventory Sorter 1.9.0-1.20
			kyrptconfig: Kyrpt Config 1.5.6-1.20
		inventorytotem: Inventory Totem 3.2
		invisframes: Invisible Frames 2.2.2
			tf_ssf_sfort_ini_sf-ini: SF-INI 1
		iris: Iris 1.7.0+mc1.20.1
			io_github_douira_glsl-transformer: glsl-transformer 2.0.0-pre13
			org_anarres_jcpp: jcpp 1.4.14
			org_antlr_antlr4-runtime: antlr4-runtime 4.11.1
		itemborders: Item Borders 1.2.2
		itemphysic: ItemPhysic 1.7.1
		jade: Jade 11.9.2+fabric
		jadeaddons: Jade Addons 5.2.5
		jamlib: JamLib 0.6.1+1.20.x
		java: OpenJDK 64-Bit Server VM 17
		jeed: Just Enough Effects Descriptions 1.20-2.1.12
		jei: Just Enough Items 15.3.0.4
		jeitweaker: JeiTweaker 8.0.6
		jepp: Just Enough Painting Previews 1.20-1.1.2
		jeresources: Just Enough Resources 1.4.0.247
		jmi: JourneyMapIntegration 1.20.1-0.14-45
		journeymap: Journeymap 5.9.22
			journeymap-api-fabric: JourneyMap API 1.20-1.9-fabric-SNAPSHOT
		jumpoverfences: Jump Over Fences 1.3.1
		just_enough_beacons: Just Enough Beacons 1.2.0
		justenoughbreeding: Just Enough Breeding 1.2.1
		justenoughprofessions: Just Enough Professions (JEP) 3.0.1
		kiwi: Kiwi Library 11.6.2
		kleeslabs: KleeSlabs 15.0.0
		lambdynlights: LambDynamicLights 2.3.2+1.20.1
			pride: Pride Lib 1.2.0+1.19.4
			spruceui: SpruceUI 5.0.0+1.20
		lapisreserve: Lapis Reserve 1.0.8
		leavemybarsalone: Leave My Bars Alone 8.0.0
		leavesbegone: Leaves Be Gone 8.0.0
		legendarytooltips: Legendary Tooltips 1.4.5
		lightoverlay: Light Overlay 8.0.0
		litematica: Litematica 0.15.3
		lithium: Lithium 0.11.2
		lithostitched: Lithostitched 1.1.5
		lootintegrations: Loot integration Mod 1.20.1-3.7
		malilib: MaLiLib 0.16.3
		maxenchantx: Max Enchant X 1.3-1.20
		mcwpaintings: Macaw's Paintings 1.0.5
		medieval_buildings: Medieval Buildings 1.0.1
		medievalend: Medieval Buildings [The End Edition] 1.0.1
		medievalmusic: Medieval Music Mod 1.20.1-2.1
		memorysettings: Memorysettings Mod 1.20.1-5.3
		mes: Moog's End Structures 1.3.1-1.20-fabric
		midnightlib: MidnightLib 1.4.1
		milkallthemobs: Milk All The Mobs 3.2
		minecraft: Minecraft 1.20.1
		minerally: Minerally 1.20.2-1.2
		minihud: MiniHUD 0.27.0
		mns: Moog's Nether Structures 1.0.1-1.20-fabric
		modernfix: ModernFix 5.17.0+mc1.20.1
		modmenu: Mod Menu 7.2.2
		monsters_in_the_closet: Monsters in the Closet 1.0.3+1.20
		moonlight: Moonlight 1.20-2.11.30
		moremobvariants: More Mob Variants 1.3.0.1
		morezombievillagers: More Zombie Villagers 3.5
		mousetweaks: Mouse Tweaks 2.26
		mousewheelie: Mouse Wheelie 1.13.0+mc1.20.1
			amecsapi: Amecs API 1.5.1+mc1.20-pre1
			coat: Coat 1.0.0-beta.20+mc1.20-pre1
			tweed4_annotated: tweed4_annotated 1.3.1+mc1.20-pre1
			tweed4_base: tweed4_base 1.7.1+mc1.20-pre1
			tweed4_data: tweed4_data 1.2.1+mc1.20-pre1
			tweed4_data_hjson: tweed4_data_hjson 1.1.1+mc1.20-pre1
			tweed4_tailor_coat: tweed4_tailor_coat 1.1.3+mc1.20-pre1
			tweed4_tailor_lang_json_descriptions: tweed4_tailor_lang_json_descriptions 1.1.0+mc1.20-pre1
			tweed4_tailor_screen: tweed4_tailor_screen 1.1.4+mc1.20-pre1
		mr_dungeons_andtaverns: Dungeons and Taverns 3.0.3.f
		mr_dungeons_andtavernsancientcityoverhaul: Dungeons and Taverns Ancient City Overhaul 1
		mr_dungeons_andtavernspillageroutpostrework: Dungeons and Taverns Pillager Outpost Rework 1.1
		mr_dungeons_andtavernsstrongholdrework: Dungeons and Taverns Stronghold Rework 1
		mr_dungeons_andtavernsswamphutrework: Dungeons and Taverns Swamp Hut Rework 1
		mr_eugenes_wealthyplainsvillage: Eugene's Wealthy Plains Village 1.0
		mr_hero_proof: Hero Proof 5.1.2
		mr_smelting_plus: Smelting Plus 1.0.5
		mru: Mineblock's Repeated Utilities 0.4.2+1.20.1
			yet_another_config_lib_v3: YetAnotherConfigLib 3.4.2+1.20.1-fabric
				com_twelvemonkeys_common_common-image: common-image 3.10.0
				com_twelvemonkeys_common_common-io: common-io 3.10.0
				com_twelvemonkeys_common_common-lang: common-lang 3.10.0
				com_twelvemonkeys_imageio_imageio-core: imageio-core 3.10.0
				com_twelvemonkeys_imageio_imageio-metadata: imageio-metadata 3.10.0
				com_twelvemonkeys_imageio_imageio-webp: imageio-webp 3.10.0
				org_quiltmc_parsers_gson: gson 0.2.1
				org_quiltmc_parsers_json: json 0.2.1
		mvs: Moog's Voyager Structures 4.1.2-1.20-fabric
		nametagtweaks: Name Tag Tweaks 3.3
		naturalist: Naturalist 4.0.3
		naturescompass: Nature's Compass 1.20.1-2.2.3-fabric
		nbc_mr: Netherite But Cheaper 1.0
		necronomicon: Necronomicon 1.4.2
		nerb: Not Enough Recipe Book 0.3
		netherrackblasting: NetherrackBlasting 1.20.1-0-fabric
		netherwardblock: Nether Wart Block to Nether Warts 1.20.1-6-fabric
		nicer-skies: Nicer Skies 1.3.0
		noexpensive: NoExpensive 1.20.1-1.9.0
		noincreasingrepaircost: No Increasing Repair Cost 1.0.0
		noisium: Noisium 2.0.3+mc1.20-1.20.1
		notenoughanimations: NotEnoughAnimations 1.7.3
		owo: oωo 0.11.2+1.20
		passablefoliage: Passable Foliage 1.20.1-fabric-8.2.1
		pickablepiglins: PickablePiglins 2.0.0+1.20.1
		pickablevillagers: Pickable Villagers 1.4.5+1.20.1
		pickupnotifier: Pick Up Notifier 8.0.0
		player-animator: Player Animator 1.0.2-rc1+1.20
		polymorph: Polymorph 0.49.5+1.20.1
			cardinal-components-block: Cardinal Components API (blocks) 5.2.1
			cardinal-components-item: Cardinal Components API (items) 5.2.1
		prism: Prism 1.0.5
		puzzleslib: Puzzles Lib 8.1.20
		randombonemealflowers: Random Bone Meal Flowers 4.5
		reacharound: Reacharound 1.1.2
		realisticbees: Realistic Bees 3.8
		recast: Recast 3.4
		recipeessentials: recipeessentials Mod 1.20.1-3.4
		repurposed_structures: Repurposed Structures 7.1.15+1.20.1-fabric
		resourcefulconfig: Resourcefulconfig 2.1.2
		resourcefullib: Resourceful Lib 2.1.25
			com_teamresourceful_bytecodecs: bytecodecs 1.0.2
			com_teamresourceful_yabn: yabn 1.0.3
		resourcepackoverrides: Resource Pack Overrides 8.0.3
		respawninganimals: Respawning Animals 8.2.0
		respawningshulkers: Respawning Shulkers 3.7
		rightclickharvest: Right Click Harvest 3.2.3+1.19.x-1.20.1-fabric
		seamless_loading_screen: Seamless Loading Screen 2.0.3+1.20.1
		searchables: Searchables 1.0.3
		shulkerboxtooltip: Shulker Box Tooltip 4.0.4+1.20.1
		shulkerdropstwo: Shulker Drops Two 3.3
		simplehudenhanced: Simple Hud Enhanced 4.6.1
		simply_houses: Simply Houses 1.1.4-1.20.1
		sit: Sit 1.20.1-27
		sleepsooner: Sleep Sooner 4.5
		smallernetherportals: Smaller Nether Portals 3.6
		smarterfarmers: Smarter Farmers 1.20-1.8.2
		smeltingstone: SmeltingStone 1.20.1-0-fabric
		smoothswapping: Smooth Swapping 0.9.3.1
		snowundertrees: Snow Under Trees 2.3.0+1.20.1
		sodium: Sodium 0.5.8+mc1.20.1
		sodium-extra: Sodium Extra 0.5.4+mc1.20.1-build.115
			caffeineconfig: CaffeineConfig 1.3.0+1.17
		sound_physics_remastered: Sound Physics Remastered 1.20.1-1.4.2
		spark: spark 1.10.53
			fabric-permissions-api-v0: fabric-permissions-api 0.1-SNAPSHOT
		squatgrow: Squat Grow 5.3.0+mc1.20.1
		stackrefill: Stack Refill 4.4
		starlight: Starlight 1.1.2+fabric.dbc156f
		starterkit: Starter Kit 6.7
		status-effect-bars: Status Effect Bars 1.0.3
		structory: Structory 1.3.5
		structory_towers: Structory: Towers 1.0.7
		structureessentials: Structure Essentials Mod 1.20.1-3.4
		stylisheffects: Stylish Effects 8.0.2
		supermartijn642configlib: SuperMartijn642's Config Lib 1.1.8+a
		t_and_t: Towns and Towers 1.12
		tectonic: Tectonic 2.3.4
		terrablender: TerraBlender 3.0.1.7
			com_electronwill_night-config_core: core 3.6.7
			com_electronwill_night-config_toml: toml 3.6.7
		terralith: Terralith 2.5.1
		thiccpackets: Extra Thicc Packets 1.17-1.19+
		tipsmod: Tips 12.0.5
		tntbreaksbedrock: TNT Breaks Bedrock 3.2
		toolstats: ToolStats 16.0.8
		totw_additions: Towers of the Wild: Additions 1.3
		totw_modded: Towers Of The Wild: Modded fabric-1.20.1-1.0.5
		trade_cycling: Trade Cycling 1.20.1-1.0.7
		transparent: Transparent 8.0.1+1.20.1
		travelersbackpack: Traveler's Backpack fabric-1.20.1-9.1.13
		treasuredistance: TreasureDistance 1.20.1-1.0.1
		treeharvester: Tree Harvester 8.7
		trinkets: Trinkets 3.7.2
		tweakermore: TweakerMore 3.17.0
			conditional-mixin: conditional mixin 0.5.1
		tweakeroo: Tweakeroo 0.17.1
		universalbonemeal: Universal Bone Meal 8.0.1
		universalenchants: Universal Enchants 8.0.0
			extensibleenums: Extensible Enums 7.0.1
		updatingworldicon: Updating World Icon 1.0.1
		villagernames: Villager Names 7.3
		villagersplus: Villagers Plus 3.1
		visuality: Visuality 0.7.1+1.20
		visualworkbench: Visual Workbench 8.0.0
		wakes: Wakes 0.2.4+1.20.1
			com_github_jdiemke_delaunay-triangulator_delaunaytriangulator: DelaunayTriangulator 1.0.0
			satin: Satin 1.14.0
		weaponmaster: YDM's Weapon Master 3.0.5
		wits: WITS 1.1.0+1.20.1-fabric
		woof: Woof 4.0.2+1.20.1
		world_preview: World preview 1.2.2
		wso16: Why stacks of 16? 1.2
		wwoo: William Wythers' Overhauled Overworld 2.0.0
		yeetusexperimentus: Yeetus Experimentus 2.3.1-build.6+mc1.20.1
		yungsapi: YUNG's API 1.20-Fabric-4.0.5
		yungsbridges: YUNG's Bridges 1.20-Fabric-4.0.3
		yungsextras: YUNG's Extras 1.20-Fabric-4.0.3
		yungsmenutweaks: YUNG's Menu Tweaks 1.20.1-Fabric-1.0.2
		zombieproofdoors: Zombie Proof Doors 3.2
	Launched Version: fabric-loader-0.15.11-1.20.1
	Backend library: LWJGL version 3.3.1 SNAPSHOT
	Backend API: Unknown
	Window size: <not initialized>
	GL Caps: Using framebuffer using OpenGL 3.2
	GL debug messages: <disabled>
	Using VBOs: Yes
	Is Modded: Definitely; Client brand changed to 'fabric'
	Type: Client (map_client.txt)
	CPU: <unknown>
