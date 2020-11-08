---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 3c22f34b1dc4e01cf4e3ea2f2b3f9c6045197734
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088020"
---
# New-AzVmssConfig

## Sammanfattning
Skapar ett VMSS.

## FRÅGESYNTAXEN

### DefaultParameterSet (standard)
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AssignIdentityParameterSet
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzVmssConfig** skapar en konfigurerbar lokal virtuell hanterarens (VMSS) objekt. Andra cmdletar behövs för att konfigurera VMSS-objektet. Dessa cmdletar är:
- Set-AzVmssOsProfile
- Set-AzVmssStorageProfile
- Add-AzVmssNetworkInterfaceConfiguration
- Add-AzVmssExtension

## BESKRIVS

### Exempel 1: skapa ett VMSS-konfigurationsobjekt
```
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

I det här exemplet skapas ett VMSS. I det första kommandot används cmdleten **New-AzVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS. I det andra kommandot används cmdleten **New-AzVmss** för att skapa en VMSS som använder VMSS-konfigurationsobjektet som skapats i det första kommandot.

## MALLPARAMETRAR

### -AssignIdentity
Ange systemets tilldelade identitet för den virtuella datorns skal uppsättning.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutomaticRepairGracePeriod
Den tid som automatiska reparationer har upphävts på grund av en tillstånds ändring på VM. Grace-tiden inleds efter att statusen har ändrats. Detta gör att du kan undvika för tidigt eller oavsiktlig reparation. Tids längden ska anges i ISO 8601-format. Standardvärdet är 5 minuter (PT5M).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutomaticRepairMaxInstanceRepairsPercent
Procent andelen (kapaciteten för scaleset) för virtuella datorer som kommer att repare ras samtidigt. Standardvärdet är 20%.

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

### -AutoOSUpgrade
Anger om OS-uppgraderingar ska användas automatiskt för att skala uppsättnings instanser när en nyare version av bilden blir tillgänglig.

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

### -BootDiagnostic
Anger den virtuella datorns skalnings profil för Autostart.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -EnableAutomaticRepair
Aktiverar automatisk reparation på den virtuella datorns skal uppsättning.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableUltraSSD
Gör det möjligt att ha en eller flera hanterade data diskar med UltraSSD_LRS lagrings konto typ på den virtuella datorns skal uppsättning.
Hanterade diskar med lagrings konto typen UltraSSD_LRS kan bara läggas till i en VMSS om den här egenskapen är aktive rad.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EvictionPolicy
Anger avlägsna principer för de virtuella datorerna i skalan.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Anknytning
Anger VMSS för tillägget. Du kan använda cmdleten **Add-AzVmssExtension** för att lägga till det här objektet.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HealthProbeId
Anger ID för en avsökaren för belastnings utjämning som används för att fastställa statusen för en instans i den virtuella datorns skal uppsättning.
HealthProbeId är i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plats
Anger den Azure-plats där VMSS skapas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkInterfaceConfiguration
Anger det nätverks profil objekt som innehåller nätverks egenskaper för konfiguration av VMSS.
Du kan använda cmdleten **Add-AzVmssNetworkInterfaceConfiguration** för att lägga till det här objektet.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsProfile
Anger operativ systemets profil objekt som innehåller egenskaper för operativ systemet för VMSS-konfigurationen.
Du kan använda cmdleten **set-AzVmssOsProfile** för att ange detta objekt.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Överleverans
Anger om cmdleten ska VMSS.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PlatformFaultDomainCount
Fel domän antal för varje placerings grupp.

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

### -Prioritet
Prioriteten för den virtuella machien i skalnings uppsättningen.  Endast värden som stöds är "regular", "dekor" och "Low".
' Regular ' är för vanlig virtuell dator.
"Plats" gäller för en virtuell dator.
"Low" är också för en virtuell dator, men ersätts med ' dekor ". Använd "plats" istället för "Low".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RollingUpgradePolicy
Anger principen för rullande uppgradering.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SinglePlacementGroup
Anger gruppen enskild placering.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMs
Anger att tilläggen inte körs på de extra överetablerade datorerna.

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

### -SkuCapacity
Anger antalet instanser i VMSS.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuName
Anger storleken på alla instanser av VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuTier
Anger nivån för VMSS. De acceptabla värdena för den här parametern är:
- Standar
- Basisk

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageProfile
Anger det lagrings profil objekt som innehåller disk egenskaperna för VMSS-konfigurationen.
Du kan använda cmdleten **set-AzVmssStorageProfile** för att ange detta objekt.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
Par med nyckelord i form av en hash-tabell. Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Aktivera avsluta schemalagda händelser

```yaml
Type: System.Management.Automation.SwitchParameter
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

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Anger zon listan för den virtuella datorns skal uppsättning.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ZoneBalance
Om du vill tvinga en helt jämn virtuell dator distribution mellan x-zoner om det finns zon avbrott.

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

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]

### System. String

### System. Collections. hash

### System. Int32

### System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. UpgradeMode, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

### Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetOSProfile

### Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetStorageProfile

### Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetNetworkConfiguration []

### Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetExtension []

### System. string []

### Microsoft. Azure. Management. Compute. Models. RollingUpgradePolicy

### System. Management. Automation. SwitchParameter

### Microsoft. Azure. Management. Compute. Models. BootDiagnostics

### System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ResourceIdentityType, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

## VÄRDEN

### Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzVmssOsProfile](./Set-AzVmssOsProfile.md)

[Set-AzVmssStorageProfile](./Set-AzVmssStorageProfile.md)

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)

[Add-AzVmssExtension](./Add-AzVmssExtension.md)

[New-AzVmss](./New-AzVmss.md)
