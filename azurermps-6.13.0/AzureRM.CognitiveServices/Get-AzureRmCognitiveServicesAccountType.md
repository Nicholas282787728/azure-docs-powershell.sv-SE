---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
ms.openlocfilehash: 05a4af3e92febcf30d44de9b114972a7c1f61d5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581752"
---
# Get-AzureRmCognitiveServicesAccountType

## Sammanfattning
Hämtar de tillgängliga konto typerna för kognitiva tjänster.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### GetAccountTypeWithName
```
Get-AzureRmCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetAccountTypes
```
Get-AzureRmCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmCognitiveServicesAccountType** hämtar de tillgängliga konto typerna för kognitiva tjänster under det här abonnemanget.

## BESKRIVS

### Exempel 1
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType
```

Hämta listan med tillgängliga typer.

### Exempel 2
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -Location westus
```

Hämta listan med tillgängliga typer i väst.

### Exempel 3
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -TypeName Face

Face
```

Kontrol lera om `Face` det är ett giltigt typnamn, att namnet returneras om det är ett giltigt namn.

## MALLPARAMETRAR

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

### -Plats
Konto plats för kognitiva tjänster.

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeName
Konto typs namn för kognitiva tjänster.

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### System. string []

### System. String

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
