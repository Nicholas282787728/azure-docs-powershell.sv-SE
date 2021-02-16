---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 62349410e3858978166fd9c5356a8c6b568b9600
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215679"
---
# New-AzVMConfig

## SYNOPSIS
Skapar ett konfigurerbart virtuellt maskinobjekt.

## SYNTAX

### DefaultParameterSet (standard)
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzVMConfig** skapar ett konfigurerbart lokalt virtuellt maskinobjekt för Azure.
Andra cmdlets kan användas för att konfigurera ett virtuellt datorobjekt, till exempel Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface och Set-AzVMOSDisk.

## EXEMPEL

### Exempel 1: Skapa ett virtuellt datorobjekt
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

Det första kommandot hämtar tillgänglighetsuppsättningen med namnet AvailabilitySet03 i resursgruppen ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabeln.
Det andra kommandot skapar ett virtuellt maskinobjekt och lagrar det sedan i $VirtualMachine variabeln.
Kommandot tilldelar den virtuella datorn ett namn och en storlek.
Den virtuella datorn tillhör den tillgänglighetsuppsättning som lagras i $AvailabilitySet.

## PARAMETERS

### -AvailabilitySetId
Anger ID för en tillgänglighetsuppsättning.
Om du vill hämta ett objekt för tillgänglighetsuppsättning använder Get-AzAvailabilitySet-cmdleten.
Objektet med tillgänglighetsuppsättning innehåller en ID-egenskap. <br>
Virtuella datorer som anges i samma tillgänglighetsuppsättning tilldelas olika noder för att maximera tillgängligheten. <br>
Mer information om tillgänglighetsuppsättningar finns i [Hantera virtuella datorers tillgänglighet.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) <br>
Mer information om planerat Azure-underhåll finns [i Planerat underhåll för virtuella datorer i Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) <br>
För närvarande kan en VM bara läggas till i tillgänglighetsuppsättningen när den skapas. Den tillgänglighetsuppsättning som den virtuella maskinerna ska läggas till för bör finnas under samma resursgrupp som den resurs som har tillgänglighetsuppsättningen. En befintlig VM kan inte läggas till i en tillgänglighetsuppsättning. <br>
Den här egenskapen kan inte finnas tillsammans med en referens som inte är null properties.virtualMachineScaleSet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -EnableUltraSSD
Gör det möjligt att ha en eller flera hanterade datadiskar UltraSSD_LRS en lagringskontotyp på den virtuella datorn.
Hanterade diskar med lagringskontotyp UltraSSD_LRS läggas till på en virtuell dator endast om den här egenskapen är aktiverad.


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
Vår policy för den virtuella Azure Spot-datorn.  Värden som stöds är "Deallocate" och "Delete".

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

### -HostId
Id för host

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
Anger listan över användaridentiteter som är kopplade till skalningsuppsättningen för virtuell dator.
Referenserna till användaridentiteten kommer att ARM resurs-ID:n i formuläret: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'

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
Identiteten för den virtuella datorn, om den har konfigurerats.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Anger en licenstyp, som anger att bilden eller disken för den virtuella datorn licensieras lokalt.
Möjliga värden för Windows Server är:
- Windows_Client
- Windows_Server möjliga värden för Linux Server-operativsystemet är: 
- RHEL_BYOS (för RHEL) 
- SLES_BYOS (för SUSE) 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
Anger det högsta pris som du är beredd att betala för en VM/VMSS med låg prioritet. Det här priset är i US-dollar. Det här priset jämförs med det aktuella låga prioritetspriset för storleken på den virtuella maskinerna. Dessutom jämförs priserna vid tidpunkten för skapa/uppdatera virtuella maskiner/VMSS med låg prioritet och åtgärden kommer bara att lyckas om maxPris är större än det aktuella priset med låg prioritet. MaxPrice används också för att avta en vm/VMSS med låg prioritet om det nuvarande låga prioritetspriset går utöver maxpris efter skapandet av VM/VMSS. Möjliga värden är: valigt decimalvärde större än noll. Exempel: 0,01538.  -1 anger att den virtuella maskinerna/VMSSS med låg prioritet inte ska avkräpas av prisskäl. Standardvärdet för maxpris är -1 om det inte anges av dig.

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

### -EncryptionAtHost
Egenskapen EncryptionAtHost kan användas av användare i begäran om att aktivera eller inaktivera värdkryptering för skalningsuppsättningen för virtuell dator eller virtuell dator. Det här aktiverar kryptering för alla diskar, inklusive resurs/temp-disk på själva värden. Standard: Kryptering på värden inaktiveras såvida inte den här egenskapen är inställd på sant för resursen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
Prioriteten för den virtuella datorn.  Värden som endast stöds är "Normal", "Dekor" och "Låg".
"Normal" är för vanlig virtuell dator.
'Spot' är för virtuell dator.
'Low' är också för virtuell dator men har ersatts av 'Spot'. Använd "Spot" i stället för "Low".

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
Resurs-ID för gruppen för närhetsplacering som ska användas med den här virtuella datorn.

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

### -Taggar
Taggarna som är kopplade till resursen.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Anger ett namn för den virtuella datorn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
Anger storleken på den virtuella datorn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmssId
ID för skala för virtuell dator

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

### -Zone
Anger tillgänglighetszonlistan för den virtuella datorn. Tillåtna värden beror på regionens funktioner. Tillåtna värden är normalt 1;2;3.

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### System.String[]

### System.Collections.Hashtable

### System.Management.Automation.SwitchParameter

## UTDATA

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Update-AzVM](./Update-AzVM.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[Set-AzVMSourceImage](./Set-AzVMSourceImage.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)


