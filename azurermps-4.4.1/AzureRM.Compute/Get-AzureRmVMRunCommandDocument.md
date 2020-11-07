---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: fd52bf58e3e240f65be88d8f9f682b2543e1f458
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758425"
---
# Get-AzureRmVMRunCommandDocument

## Sammanfattning
Kommandot Hämta kommando.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Kommandot Hämta kommando.

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

Hämtar ett specifikt kommando dokument för "RunPowerShellScript" i "västkusten".


Get-AzureRmVMRunCommandDocument plats $loc

### Exempel 2
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

Visar alla tillgängliga kör-kommandon i "västkusten".

## MALLPARAMETRAR

### -CommandId
Kommando-ID.

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
Den plats där kommandona körs.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. Compute. Automation. Models. PSRunCommandDocument

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

