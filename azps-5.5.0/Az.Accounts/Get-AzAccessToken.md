---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229494"
---
# Get-AzAccessToken

## SYNOPSIS
Hämta obearbetad åtkomsttoken. När du använder -ResourceUrl kontrollerar du att värdet matchar den aktuella Azure-miljön. Du kan referera till värdet för `(Get-AzContext).Environment` .

## SYNTAX

### KnownResourceTypeName (standard)
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceUrl
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Hämta åtkomsttoken

## EXEMPEL

### Exempel 1 Hämta obearbetad åtkomsttoken för ARM slutpunkt
```powershell
PS C:\> Get-AzAccessToken
```

Hämta åtkomsttoken för ResourceManager-slutpunkt för aktuellt konto

### Exempel 2 Hämta obearbetad åtkomsttoken för AAD Graph-slutpunkten
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

Hämta åtkomsttoken för AAD graph-slutpunkt för aktuellt konto

### Exempel 3 Hämta obearbetad åtkomsttoken för AAD Graph-slutpunkten
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

Hämta åtkomsttoken för AAD graph-slutpunkt för aktuellt konto

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

### -ResourceTypeName
Valfritt namn på ny typ, värden som stöds: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse. Standardvärdet är Arm om det inte anges.

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceUrl
Resurs-URL för det du begär token, t.ex. http://graph.windows.net/ ' '.

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Valfritt klientorganisations-ID. Använd klientorganisations-ID för standardkontext om det inte anges.

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Ingen

## UTDATA

### System.String

## ANTECKNINGAR

## RELATERADE LÄNKAR
