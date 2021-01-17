---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393235"
---
# Get-AzAccessToken

## Sammanfattning
Få åtkomst till RAW-åtkomsttoken. När du använder-ResourceUrl kontrollerar du att värdet stämmer överens med den aktuella Azure-miljön. Du kan referera till värdet i `(Get-AzContext).Environment` .

## FRÅGESYNTAXEN

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

## PROBLEMBESKRIVNING
Hämta åtkomsttoken

## BESKRIVS

### Exempel 1 Hämta token för RAW-åtkomst för ARM slut punkt
```powershell
PS C:\> Get-AzAccessToken
```

Hämta åtkomst-token för slut punkten för det aktuella kontot

### Exempel 2 Hämta åtkomsttoken för Access-graf för AAD
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

Hämta Access-token för AAD-slutpunktsmappare för aktuellt konto

### Exempel 3 Hämta åtkomsttoken för Access-graf för AAD
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

Hämta Access-token för AAD-slutpunktsmappare för aktuellt konto

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

### -ResourceTypeName
Valfritt namn på reresurs-typ, tillåtna värden: AadGraph, AnalysisServices, arm, attestering, batch, DataLake,, OperationalInsights, ResourceManager, Synapse. Standardvärdet är arm om det inte anges.

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
Resurs-URL för att begära token, till exempel " http://graph.windows.net/ ".

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
Valfritt klient-ID. Använd klient-ID för standard kontext om det inte anges.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Ingen

## VÄRDEN

### System. String

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
