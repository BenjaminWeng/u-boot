#Copyright 2012 The Chromium Authors
#
# SPDX-License-Identifier:	GPL-2.0+
#

obj-y += OpteeClientMem.o
obj-y += OpteeClientApiLib.o
obj-y += OpteeClientInterface.o
obj-y += OpteeClientSMC.o
obj-y += OpteeClientRPC.o
obj-y += tee_smc-arm64.o

ifdef CONFIG_OPTEE_V1
obj-y += OpteeClientRkFs.o
obj-y += 258be795-f9ca-40e6-a8699ce6886c5d5d.o
lib/optee_clientApi/258be795-f9ca-40e6-a8699ce6886c5d5d.o: lib/optee_clientApi/258be795-f9ca-40e6-a8699ce6886c5d5d.c
lib/optee_clientApi/258be795-f9ca-40e6-a8699ce6886c5d5d.c: lib/optee_clientApi/258be795-f9ca-40e6-a8699ce6886c5d5d.ta
	$(srctree)/lib/optee_clientApi/tabinary_to_cfile.py --prefix keymaster --TA $< --out $@

obj-y += c11fe8ac-b997-48cf-a28de2a55e5240ef.o
lib/optee_clientApi/c11fe8ac-b997-48cf-a28de2a55e5240ef.o: lib/optee_clientApi/c11fe8ac-b997-48cf-a28de2a55e5240ef.c
lib/optee_clientApi/c11fe8ac-b997-48cf-a28de2a55e5240ef.c: lib/optee_clientApi/c11fe8ac-b997-48cf-a28de2a55e5240ef.ta
	$(srctree)/lib/optee_clientApi/tabinary_to_cfile.py --prefix widevine_keybox --TA $< --out $@
endif

ifdef CONFIG_OPTEE_V2
obj-y += OpteeClientRkFs-v2.o
obj-y += 258be795-f9ca-40e6-a8699ce6886c5d5d-for-optee-v2.o
lib/optee_clientApi/258be795-f9ca-40e6-a8699ce6886c5d5d-for-optee-v2.o: lib/optee_clientApi/258be795-f9ca-40e6-a8699ce6886c5d5d-for-optee-v2.c
lib/optee_clientApi/258be795-f9ca-40e6-a8699ce6886c5d5d-for-optee-v2.c: lib/optee_clientApi/258be795-f9ca-40e6-a8699ce6886c5d5d-for-optee-v2.ta
	$(srctree)/lib/optee_clientApi/tabinary_to_cfile.py --prefix keymaster --TA $< --out $@
endif

