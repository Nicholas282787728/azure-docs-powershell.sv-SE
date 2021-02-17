---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233215"
---
# Update-AzVmss

## SYNOPSIS
Uppdaterar statusen för en VMSS.

## SYNTAX

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

## BESKRIVNING
Cmdleten **Update-AzVmss** uppdaterar statusen för en skaluppsättning för virtuell dator (VMSS) till tillståndet för ett lokalt VMSS-objekt.

## EXEMPEL

### Exempel 1: Uppdatera tillståndet för en VMSS till tillståndet för ett lokalt VMSS-objekt.
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

Det här kommandot uppdaterar statusen för den VMSS som heter VMSS001 som tillhör resursgruppen med namnet Group001 till statusen för ett lokalt VMSS-objekt $LocalVMSS.

## PARAMETERS

### -As Ent fån
Kör cmdleten i bakgrunden och returnera ett jobb för att följa förloppet.

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
Anger om OS-uppgraderingar ska tillämpas automatiskt för att skala vissa instanser på ett rullande sätt när en nyare version av bilden blir tillgänglig.

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
Den tid som automatiska reparationer är pausade på grund av en tillståndsändring på den virtuella maskinerna. Respittiden startar när tillståndsändringen har slutförts. På så sätt undviker du oavsiktliga eller oavsiktliga reparationer. Tidslängden ska anges i ISO 8601-format. Den minsta tillåtna respitperioden är 30 minuter (PT30M), som också är standardvärdet. Den högsta tillåtna respitperioden är 90 minuter (PT90M).

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
Om startdiagnostik ska aktiveras på den virtuella datorns skaluppsättning.

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
URI för lagringskontot som ska användas för att placera konsolens utdata och skärmbild.

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
Anger en bas-64-kodad sträng med anpassade data.
Detta avkodas till en binär matris som sparas som en fil på den virtuella datorn.
Den maximala längden på den binära matrisen är 65 535 byte. <br>
Mer information om hur du använder moln init för den virtuella maskinerna finns i Använda moln init för att [anpassa en Linux VM när den skapas.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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
Inaktivera Automatisk återställning för principen för automatisk OS-uppgradering

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
Aktivera eller inaktivera automatiska reparationer på skaluppsättningen för den virtuella datorn.

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
Anger om Windows virtuella datorer i VMSS har aktiverats för automatiska uppdateringar.

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
Den här parametern kan användas av användaren i begäran att aktivera eller inaktivera värdkryptering för skalningsuppsättningen för virtuell dator. 

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
Anger listan över användaridentiteter som är kopplade till skaluppsättningen för virtuell dator.
Referenserna till användaridentiteten kommer att ARM resurs-ID:n i formuläret: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'

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
Anger vilken typ av identitet som används för skaluppsättningen för den virtuella datorn.
Typen "SystemAssignedUserAssigned" innehåller både en implicit skapad identitet och en uppsättning användartilldelade identiteter.
Typen Ingen tar bort alla identiteter från skaluppsättningen för virtuell dator.
De godtagbara värdena för den här parametern är:
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
Anger bildens referens-ID.

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
Anger typen av vmImage-erbjudande (Virtual Machine Image).
Om du vill få ett bilderbjudande använder du Get-AzVMImageOffer cmdlet.

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
Om du vill skaffa en utgivare använder Get-AzVMImagePublisher-cmdleten.

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
Använd cmdleten Get-AzVMImageSku för att erhålla SKU:er.

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
Anger versionen av VMImage.
Om du vill använda den senaste versionen anger du det senaste värdet i stället för en viss version.

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
Anger blob-URI:en för användarbilden.
VMSS skapar en operativsystemdisk i samma behållare för användarbilden.

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
Ange licenstyp, som används för att ta med ditt eget licensscenario.

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
Anger lagringskontotyp för hanterad disk.
De godtagbara värdena för den här parametern är:
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
Maximalt antal procent av den totala virtuella datorinstansen som kommer att uppgraderas samtidigt genom den rullna uppgraderingen i en batch.
Eftersom det är ett maximalt fel antal instanser i tidigare eller framtida batchar kan procentandelen instanser i en batch minska för att säkerställa högre tillförlitlighet.
Om värdet inte anges anges det till 20.

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
Anger det högsta pris du är beredd att betala för en VM/VMSS med låg prioritet. Det här priset är i US-dollar. Det här priset jämförs med det aktuella låga prioritetspriset för storleken på den virtuella maskinerna. Dessutom jämförs priserna vid tidpunkten för create/update av vm/VMSS med låg prioritet och åtgärden kommer bara att lyckas om maxPris är större än det aktuella priset med låg prioritet. MaxPrice används också för att avta en vm/VMSS med låg prioritet om det nuvarande låga prioritetspriset går utöver maxpris efter skapandet av VM/VMSS. Möjliga värden är: val helst decimalvärde större än noll. Exempel: 0,01538.  -1 anger att den virtuella maskinerna/VMSS med låg prioritet inte ska avkräpas av prisskäl. Standardvärdet för maxpris är -1 om det inte anges av dig.

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
Maximal procentandel av den totala virtuella datorinstansen i skaluppsättningen som kan vara felskyddad samtidigt, antingen som ett resultat av uppgradering eller genom att påträffas i ett feltillstånd av hälsokontrollerna av den virtuella datorn innan den rullande uppgraderingen avbryts.
Det här villkoret kontrolleras innan du startar en batch.
Om värdet inte anges anges det till 20.

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
Den maximala procentandelen uppgraderade virtuella datorinstanser som kan hittas vara i feltillstånd.
Den här kontrollen inträffar när varje batch har uppgraderats.
Om den här procentandelen överskrids avbryts den rullningsna uppdateringen.
Om värdet inte anges anges det till 20.

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
Anger cachelagringsläge för operativsystemets disk. De godtagbara värdena för den här parametern är:
- Ingen
- ReadOnly
- SkrivSkydda Standardvärdet är Skrivskydd.
Om du ändrar cachelagringsvärdet startar cmdleten om den virtuella datorn.
Den här inställningen påverkar konsekvensen och prestandan på disken.

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
Anger om WriteAccelerator ska aktiveras eller inaktiveras på operativsystemets disk.

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

### -Overprovision
Anger om cmdleten överetablerar VMSS.

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
Väntetiden mellan att slutföra uppdateringen för alla virtuella datorer i en batch och starta nästa batch.
Tidslängden ska anges i ISO 8601-format.
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
Anger planens namn.

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
Anger planens produkt.

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
Anger kampanjkoden för abonnemanget.

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
Anger planutgivaren.

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
Anger om virtuell datoragent ska tillhandahållas på Windows virtuella datorer i VMSS.

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
Resurs-ID för gruppen för närhetsplacering som ska användas med den här skalskalan.

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
Anger namnet på resursgruppen som VMSS tillhör.

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
De regler som ska följas vid skalning i en skala för en virtuell dator.  Möjliga värden är: "Standard", "ÄldstaVM" och "NyasteVM".  Standard när en uppsättning med virtuella maskiner skalar skalas in balanseras skaluppsättningen först i olika zoner om det är en zonskalauppsättning.  Sedan kommer det att balanseras över feldomäner så långt det är möjligt.  Inom varje feldomän är de virtuella maskiner som valts för borttagning de senaste som inte är skyddade från skalning.  "ÄldstaVM" när en uppsättning av virtuella maskiner skalas in väljs de äldsta virtuella maskinerna som inte skyddas från skalning för borttagning.  För uppsättningar med zonbaserade virtuella maskiner kommer skaluppsättningen först att balanseras mellan zoner.  Inom varje zon väljs de äldsta virtuella maskinerna som inte är skyddade för borttagning.  "NewestVM" när en uppsättning av virtuella maskinskalor skalas in väljs de senaste virtuella maskinerna som inte skyddas från skalning för borttagning.  För uppsättningar med zonbaserade virtuella maskiner kommer skaluppsättningen först att balanseras mellan zoner.  Inom varje zon väljs de senaste virtuella maskinerna som inte är skyddade för borttagning.

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
Anger den enskilda placeringsgruppen.

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
Anger att tilläggen inte körs på extraometablera virtuella maskiner.

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

### -SKUName
Anger storleken för alla instanser av VMSS.

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
De godtagbara värdena för den här parametern är:
- Standard
- Grundläggande

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

### -Tag
Nyckelvärdepar i form av en hash-tabell. Exempel: @{key0="value0";key1=$null;key2="value2"}

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
Konfigurerbar tidslängd (i minuter) en virtuell dator som tas bort måste godkänna potentiellt händelsen Avbryt schemalagd innan händelsen godkänns automatiskt (timed out).

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
Anger om händelsen Avbryt schemalagd är aktiverad eller inaktiverad.

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
Anger tidszonen för Windows OS. t.ex. \" Pacific Standard \" Time. <br>
Möjliga värden kan [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) tidszoner som returneras av [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)

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

### UltraSSDEnabled
Flaggan som aktiverar eller inaktiverar en funktion för att ha en eller flera hanterade datadiskar med UltraSSD_LRS-lagringskontotyp på skaluppsättningen för virtuell dator.
Hanterade diskar med lagringskontotyp kan UltraSSD_LRS läggas till i en VMSS endast om den här egenskapen är aktiverad.

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
Angav läge för uppgradering till virtuella datorer i skaluppsättningen.
De godtagbara värdena för den här parametern är:
- Automatisk
- Manuellt
- Rullande

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
Anger behållarens URL:er som används för att lagra operativsystemdiskar för VMSS.

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
Om du vill hämta ett VMSS-objekt använder du Get-AzVmss-cmdleten.
Det här virtuella datorobjektet innehåller det uppdaterade läget för VMSS.

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
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs.
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.Boolean

## UTDATA

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzVmss](./Get-AzVmss.md)

[New-AzVmss](./New-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Restart-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stop-AzVmss](./Stop-AzVmss.md)


