---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221727"
---
# Get-AzVMGuestPolicyStatus

## SYNOPSIS
Hämtar status för gästkonfigurationsprincipen (detaljerad) för ett initiativ av typen "Gästkonfiguration" som tilldelas till en VM.
Ett initiativ är en princip av definitionstyp "Initiative".

## SYNTAX

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

## BESKRIVNING
Cmdlet Get-AzVMGuestPolicyStatus får status för gästkonfigurationsprincipen för ett initiativ av typen "Gästkonfiguration" som är tilldelad till en VM.
Ett initiativ är en princip av definitionstyp "Initiative".
Den här cmdleten får efterlevnadsstatus för den virtuella maskinerna och orsaker till varför den inte är kompatibel för de enskilda principerna i initiativet.

## EXEMPEL

### Exempel 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Hämta alla senaste statusar för gästkonfigurationsprincipen för en VM.
Statusen innehåller efterlevnadsstatus för den virtuella maskinerna för varje princip i alla initiativ av typen "Gästkonfiguration", orsaker till efterlevnad, tidpunkten för efterlevnadskontrollen, resursinformation som har kontrollerats för efterlevnad.
Resultatet innehåller de senaste statusarna, innehåller inte tidigare historiska statusar.

### Exempel 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Hämta de senaste statusarna för gästkonfigurationsprincipen med initiativ-ID. Statusen innehåller efterlevnadsstatus för den virtuella maskinerna för varje princip i initiativet, efterlevnadsorsaker, tid för efterlevnadskontrollen, resursinformation som kontrollerats för efterlevnad.
Resultatet innehåller inte tidigare genererade statusar, utan innehåller bara den senaste statusen för varje princip i initiativ.

### Exempel 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Hämta de senaste statusarna för gästkonfigurationsprincipen efter initiativnamn.
Statusen innehåller efterlevnadsstatus för den virtuella maskinerna för varje princip i initiativet, efterlevnadsorsaker, tid för efterlevnadskontrollen, resursinformation som kontrollerats för efterlevnad.
Resultatet innehåller inte tidigare genererade statusar, utan innehåller bara den senaste statusen för varje princip i initiativ.

### Exempel 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

Hämta status för gästkonfigurationsprincipen med ReportId.
ReportId är egenskapen ReportId som kan hittas i resultatet av ett Get-AzVMGuestPolicyStatus initiativeId eller Initiative Name (se andra exempel)

## PARAMETERS

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

### -InitiativeId
Definition-ID för en princip där definitionstyp är Initiative och kategori är Gästkonfiguration

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
Namnet på en princip där definitionstyp är Initiative och kategorin är Gästkonfiguration

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
ID för status för en gästkonfigurationsprincip.
En princip där definitionstyp är Initiative och kategori är Gästkonfiguration måste tilldelas till en omfattning för att få status.

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
Resursgruppnamn.

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
VM-namn.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Ingen
## UTDATA

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed
## ANTECKNINGAR

## RELATERADE LÄNKAR
