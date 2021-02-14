---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237788"
---
# Get-AzVMGuestPolicyStatusHistory

## SYNOPSIS
Hämtar statushistorik för efterlevnadsstatus för gästkonfigurationsprincipen för ett initiativ av typen "Gästkonfiguration" som tilldelas till en VM.
Ett initiativ är en princip av definitionstyp "Initiative".

## SYNTAX

### InitiativeNameScope (standard)
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdlet Get-AzVMGuestPolicyStatusHistory får statushistorik för gästkonfigurationsprinciper för ett initiativ av typen "Gästkonfiguration" som tilldelas till en VM.
Ett initiativ är en princip av definitionstyp "Initiative".
Använd Get-AzVMGuestPolicyStatus cmdlet för att få information om en enda efterlevnadsstatus med ReportId som finns i utdata för Get-AzVMGuestPolicyStatusHistory cmdlet.

## EXEMPEL

### Exempel 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

Hämtar historik för efterlevnadsstatus efter initiativ-ID. ShowOnlyChange-växeln visar bara historiska statusändringar.
Hoppar över status som inte har ändrats mellan två efterlevnadskontroller.

### Exempel 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

Får historik för efterlevnadsstatus efter initiativnamn.
I växeln ShowOnlyChange visas bara historiska statusändringar.
Hoppar över status som inte har ändrats mellan två efterlevnadskontroller.

### Exempel 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

Hämtar historik för efterlevnadsstatus för alla principer för gästkonfiguration som tilldelats den virtuella datorn.
I växeln ShowOnlyChange visas bara historiska statusändringar.
Hoppar över status som inte har ändrats mellan två efterlevnadskontroller.

### Exempel 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Får historik för efterlevnadsstatus efter initiativ-ID.

### Exempel 5
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Får historik för efterlevnadsstatus efter initiativnamn.

### Exempel 6
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
Hämtar historik för efterlevnadsstatus för alla principer för gästkonfiguration som tilldelats den virtuella datorn.

### Exempel 7
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

Hämta status för gästkonfigurationsprincipen med ReportId.
ReportId är egenskapen ReportId som kan hittas i resultatet av Get-AzVMGuestPolicyStatusHistory. (se andra exempel)

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

Required: False
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

### -ResourceGroupName
Resursgruppnamn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowOnlyChange
Visar historiska statusändringar endast för principer för gästkonfiguration.
Hoppar över status som inte har ändrats mellan två granskningar av efterlevnadsstatus.

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

### -VMName
VM-namn.

```yaml
Type: System.String
Parameter Sets: (All)
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

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus
## ANTECKNINGAR

## RELATERADE LÄNKAR
