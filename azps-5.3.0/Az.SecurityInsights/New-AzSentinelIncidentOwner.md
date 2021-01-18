---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: aa3cddd70ad1c17df9415499d0b33fa33e68f7f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525572"
---
# New-AzSentinelIncidentOwner

## Sammanfattning
Skapa ett incident ägar objekt för att uppdatera en incident ägare.

## FRÅGESYNTAXEN

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzSentinelIncidentOwner** skapar ett incident ägar objekt i minnet för att uppdatera ett samtal.

## BESKRIVS

### Exempel 1
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

I det här exemplet skapas en **IncidentOwner** och en incident uppdateras till den nya ägaren.

## MALLPARAMETRAR

### -Tilldelat
Incident ägare-tilldelad

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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

### -E-postadress
Incident ägare – e-post

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Incident ägare – ObjectId

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPrincipalName
Incident ägare – användarens huvud namn

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Ingen
## VÄRDEN

### Microsoft. Azure. commands. SecurityInsights. Models. incidenter. PSSentinelIncident
## ANMÄRKNINGAR

## RELATERADE LÄNKAR
