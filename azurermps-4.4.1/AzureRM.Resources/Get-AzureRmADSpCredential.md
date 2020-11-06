---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 247b0735e41f02a55b94e5a8f8ed44136eb3f37e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574538"
---
# Get-AzureRmADSpCredential

## Sammanfattning
Hämtar en lista med autentiseringsuppgifter som är associerade med ett tjänst huvud.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ObjectIdParameterSet (standard)
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Get-AzureRmADSpCredential cmdlet kan användas för att hämta en lista med autentiseringsuppgifter som är associerade med ett tjänst huvud.
Med det här kommandot hämtas alla egenskaper för autentiseringsuppgifter (men inte det Credential-värde) som är kopplat till tjänstens huvud namn.

## BESKRIVS

### --------------------------Exempel 1--------------------------
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

Returnerar en lista med autentiseringsuppgifter som är kopplade till tjänstens huvud namn (SPN) http://test12345 .

## MALLPARAMETRAR

### -ObjectId
Objekt-ID för tjänstens huvud namn att hämta autentiseringsuppgifter från.

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Namnet (SPN) för tjänstens huvud namn att hämta autentiseringsuppgifter från.

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmADSpCredential](./New-AzureRmADSpCredential.md)

[Remove-AzureRmADSpCredential](./Remove-AzureRmADSpCredential.md)

[Get-AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

