---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088880"
---
# Get-AzVMGuestPolicyStatus

## Sammanfattning
Hämtar status för gäst konfigurations principer (detaljerade) för ett initiativ av typen "gäst konfiguration" som är tilldelad en virtuell dator.
Ett initiativ är en policy för definitions typen "initiativ".

## FRÅGESYNTAXEN

### VmScope (standard)
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeNameScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ReportIdScope
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Get-AzVMGuestPolicyStatus-cmdleten får status för gäst konfigurations principer för ett initiativ av typen "gäst konfiguration" som är tilldelad en virtuell dator.
Ett initiativ är en policy för definitions typen "initiativ".
Denna cmdlet tar emot efterlevnad för den virtuella datorn och gör varför den inte är kompatibel för de enskilda principerna i initiativet.

## BESKRIVS

### Exempel 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Få alla senaste status för gäst konfigurations principer för en virtuell dator.
Statusen innehåller överensstämmelse status för VM för varje princip i alla initiativ av typen "gäst konfiguration", krav på efterlevnad, tid för kompatibilitetskontrollen, resursinformation som kontrol leras.
Resultaten inkluderar senaste status, inkluderar inte tidigare historik status.

### Exempel 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Få den senaste statusen för princip för gäst konfiguration efter initiativ-ID. Statusen innehåller överensstämmelse status för den virtuella datorn för varje princip i initiativet, förvalda krav, tiden för kontrollen av efterlevnad, resursinformation som kontrol leras efter efterlevnad.
Resultaten inkluderar inte tidigare genererade status värden, det inkluderar bara den senaste statusen för varje policy i initiativet.

### Exempel 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Skaffa den senaste statusen för gäst konfigurations principen per initiativ namn.
Statusen innehåller överensstämmelse status för den virtuella datorn för varje princip i initiativet, förvalda krav, tiden för kontrollen av efterlevnad, resursinformation som kontrol leras efter efterlevnad.
Resultaten inkluderar inte tidigare genererade status värden, det inkluderar bara den senaste statusen för varje policy i initiativet.

### Exempel 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

Hämta status för gäst konfigurations principer via ReportId.
Egenskapen ReportId är den ReportId-egenskap som finns i resultatet av Get-AzVMGuestPolicyStatus efter initiativeId eller initiativ namn (se andra exempel)

## MALLPARAMETRAR

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

### -InitiativeId
Definitions-ID för en policy där definitions typ är initiativ och kategori är gäst konfiguration

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitiativeName
Namnet på en policy där definitions typen är initiativ och kategori är gäst konfiguration

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportId
ID för statusen för en gäst konfigurations princip.
En policy där definitions typ är initiativ och kategori är gäst konfiguration måste tilldelas ett scope för att få status.

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resurs grupps namn.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Namn på virtuell dator.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
## VÄRDEN

### Microsoft. Azure. commands. GuestConfiguration. Models. PolicyStatusDetailed
## ANMÄRKNINGAR

## RELATERADE LÄNKAR
