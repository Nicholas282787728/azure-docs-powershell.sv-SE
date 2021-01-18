---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524430"
---
# Update-AzVmss

## Sammanfattning
Uppdaterar tillståndet för en VMSS.

## FRÅGESYNTAXEN

### DefaultParameter (standard)
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Update-AzVmss** uppdaterar tillståndet för en virtuell dators skalnings uppsättning (VMSS) till tillståndet för ett lokalt VMSS-objekt.

## BESKRIVS

### Exempel 1: Uppdatera statusen för en VMSS till tillståndet för ett lokalt VMSS-objekt.
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

Det här kommandot uppdaterar tillståndet för VMSS med namnet VMSS001 som tillhör resurs gruppen som heter Group001 till tillståndet för ett lokalt VMSS-objekt, $LocalVMSS.

## MALLPARAMETRAR

### -AsJob
Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutomaticOSUpgrade
Anger om OS-uppgraderingar ska användas automatiskt för att skala uppsättnings instanser när en nyare version av bilden blir tillgänglig.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutomaticRepairGracePeriod
Den tid som automatiska reparationer har upphävts på grund av en tillstånds ändring på VM. Grace-tiden inleds efter att statusen har ändrats. Detta gör att du kan undvika för tidigt eller oavsiktlig reparation. Tids längden ska anges i ISO 8601-format. Den minsta tillåtna respitperioden är 30 minuter (PT30M), vilket också är standardvärdet. Den maximala respitperioden är 90 minuter (PT90M).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsEnabled
Om startdiagnostik ska aktive ras på den virtuella datorns skal uppsättning.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsStorageUri
URI för lagrings konto som ska användas för att placera utdata och skärm bild i konsolen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomData
Anger en Base-64-kodad sträng med anpassade data.
Det här är avkodat till en binär matris som sparats som en fil på den virtuella datorn.
Den maximala längden för den binära matrisen är 65535 byte. <br>
Information om hur du använder Cloud-Init för din virtuella dator finns i [använda Cloud-Init för att anpassa en virtuella dator för Linux när den skapas](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAutoRollback
Inaktivera automatisk återställning för automatisk uppgraderings princip för operativ system

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
Anger att denna cmdlet inaktiverar lösenordsautentisering för Linux OS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticRepair
Aktivera eller inaktivera automatisk reparation på den virtuella datorns skal uppsättning.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticUpdate
Anger om de virtuella Windows-datorerna i VMSS är aktiverade för automatiska uppdateringar.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionAtHost
Denna parameter kan användas av användaren i begäran för att aktivera eller inaktivera värd krypteringen för den virtuella datorns skal uppsättning. 

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityId
Anger listan över användar identiteter som är kopplade till den virtuella datorns skal uppsättning.
Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
Anger den typ av identitet som används för den virtuella datorns skal uppsättning.
Typen "SystemAssignedUserAssigned" inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.
Typen "none" tar bort alla identiteter från den virtuella datorns skal uppsättning.
De acceptabla värdena för den här parametern är:
- SystemAssigned
- UserAssigned
- SystemAssignedUserAssigned
- Ingen

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferenceId
Anger bild referens-ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferenceOffer
Anger typen av virtuell dator avbildning (VMImage).
För att få ett bild utbud, Använd cmdleten Get-AzVMImageOffer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferencePublisher
Anger namnet på en utgivare av en VMImage.
Använd Get-AzVMImagePublisher cmdlet för att få en utgivare.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferenceSku
Anger VMImage-SKU.
För att få SKU: er, Använd Get-AzVMImageSku cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferenceVersion
Anger versionen för VMImage.
För att använda den senaste versionen, ange ett värde som är senaste i stället för en viss version.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageUri
Anger BLOB URI för användar avbildningen.
VMSS skapar en operativ Systems disk i samma behållare som användar bilden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Ange licens typ, som är till för att sätta ditt eget licens scenario.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedDiskStorageAccountType
Anger lagrings konto typen för hanterad disk.
De acceptabla värdena för den här parametern är:
- StandardLRS
- PremiumLRS

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxBatchInstancePercent
Maximalt procent av totalt antal virtuella dator instanser som kommer att uppgraderas samtidigt av den rullande uppgraderingen i en grupp.
Eftersom det är ett maximalt, kan felaktiga instanser i tidigare eller framtida batchar leda till att procent andelen instanser i en grupp minskar för att säkerställa högre pålitlighet.
Om värdet inte anges är det inställt på 20.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
Anger det högsta priset du vill betala för en VM/VMSS med lägre prioritet. Priset är i USD. Det här priset jämförs med det aktuella priset för lägre prioritet för VM-storleken. Dessutom jämförs priserna när du skapar/uppdaterar med den virtuella dator-VMSS och åtgärden utförs bara om maxPrice är större än det aktuella låga prioritets priset. MaxPrice kommer också att användas för att avlägsna en VM/VMSS med lägre prioritet om det nuvarande priset för lägre prioritet går bortom maxPrice när du har skapat en virtuell dator/VMSS. Möjliga värden är: ett decimal tal större än noll. Exempel: 0,01538.  -1 anger att den virtuella dator-VMSS för låg prioritet inte ska avlägsnas av skäl. Standard priset för max är-1 om det inte tillhandahålls av dig.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxUnhealthyInstancePercent
Den maximala procent andelen av de totala virtuella dator instanserna i den skala som kan vara ohälsosamt, antingen som ett resultat av att den har uppgraderats, eller genom att hitta en felaktig status av hälso kontroller för den virtuella datorn innan den rullande uppgraderingen avbryts.
Det här villkoret kontrol leras innan en batch startas.
Om värdet inte anges är det inställt på 20.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxUnhealthyUpgradedInstancePercent
Den maximala procent andelen uppgraderade virtuella dator instanser som kan upptäckas vara felfria.
Denna kontroll sker efter att varje kommando har uppgraderats.
Om denna procents ATS överskrids avbryts den rullande uppdateringen.
Om värdet inte anges är det inställt på 20.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OsDiskCaching
Anger operativ system diskens cacheläge. De acceptabla värdena för den här parametern är:
- Ingen
- ReadOnly
- ReadWrite standardvärdet är ReadWrite.
Om du ändrar värdet för cachelagring startas den virtuella datorn om.
Den här inställningen påverkar diskens konsekvens och prestanda.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OsDiskWriteAccelerator
Anger om WriteAccelerator ska aktive ras eller inaktive ras på OS-disken.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Överleverans
Anger om cmdleten ska VMSS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PauseTimeBetweenBatches
Vänte tiden mellan att slutföra uppdateringen för alla virtuella datorer i en batch och starta nästa sats.
Tids längden ska anges i ISO 8601-format.
Standardvärdet är 0 sekunder (PT0S).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanName
Anger plan namnet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanProduct
Anger plan produkten.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanPromotionCode
Anger abonnemangs kampanj koden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanPublisher
Anger plan utgivaren.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProvisionVMAgent
Anger om virtuell dator agent ska etableras på de virtuella Windows-datorerna i VMSS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
Resurs-ID för närhets gruppen som ska användas med den här skalnings uppsättningen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som VMSS tillhör.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
De regler som ska användas vid skalning-i en virtuell dators skala uppsättning.  Möjliga värden är: ' default ', ' OldestVM ' och ' NewestVM '.  "Standard" när en skala för virtuell dator skal för änd ras i, fördelas skalnings uppsättningen först över zoner om den är en Zonal skala.  Då kommer den att bal anse ras i så stor utsträckning som möjligt.  De virtuella datorerna som valts för borttagning är de nyaste som inte skyddas från Scale-in i varje fel domän.  ' OldestVM ' när en virtuell dators Scale-uppsättning skal för änd ras-in väljs de äldsta virtuella datorerna som inte skyddas från Scale-in att tas bort.  För Zonal för virtuell dator fördelas skalnings uppsättningen först över zoner.  Inom varje zon kommer de äldsta virtuella datorerna som inte skyddas att väljas för borttagning.  ' NewestVM ' när en virtuell dators skal uppsättning skal för änd ras-in väljs de senaste virtuella datorerna som inte skyddas från Scale-in att tas bort.  För Zonal för virtuell dator fördelas skalnings uppsättningen först över zoner.  Inom varje zon kommer de senaste virtuella datorerna som inte skyddas att väljas för borttagning.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
Anger gruppen enskild placering.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMs
Anger att tilläggen inte körs på de extra överetablerade datorerna.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuCapacity
Anger antalet instanser i VMSS.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuName
Anger storleken på alla instanser av VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuTier
Anger nivån för VMSS.
De acceptabla värdena för den här parametern är:
- Standar
- Basisk

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tagg
Par med nyckelord i form av en hash-tabell. Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TerminateScheduledEventNotBeforeTimeoutInMinutes
Konfigurerbar längd (i minuter) en virtuell dator som tas bort måste eventuellt godkänna händelsen Avsluta schemalagd händelse innan händelsen är automatiskt godkänd (tids gräns).

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TerminateScheduledEvents
Anger om den schemalagda händelsen Avbryt är aktive rad eller inaktive rad.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Anger tids zonen för Windows OS. t. \" Pacific, normal tid \" . <br>
Möjliga värden kan vara [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) värde från tids zoner som returneras av [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UltraSSDEnabled
Flaggan som aktiverar eller inaktiverar en funktion för att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorns skal uppsättning.
Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till i en VMSS om den här egenskapen är aktive rad.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UpgradePolicyMode
Angav läget för en uppgradering till virtuella datorer i skalnings uppsättningen.
De acceptabla värdena för den här parametern är:
- Versal
- Manövrer
- Rullar

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdContainer
Anger de URL-adresser som används för att lagra operativ system diskar för VMSS.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Anger ett lokalt VMSS-objekt.
För att hämta ett VMSS-objekt, Använd cmdleten Get-AzVmss.
Det här virtuella dator objektet innehåller det uppdaterade tillståndet för VMSS.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMScaleSetName
Anger namnet på den VMSS som denna cmdlet skapar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

### Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet

### System. Boolean

## VÄRDEN

### Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzVmss](./Get-AzVmss.md)

[New-AzVmss](./New-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Restart-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stopp-AzVmss](./Stop-AzVmss.md)


