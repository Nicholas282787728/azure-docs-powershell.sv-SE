---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Send-Feedback.md
ms.openlocfilehash: 4ebdb51fdc6129f0e980282b6588324505e62bcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581371"
---
# Send-Feedback

## Sammanfattning
Skickar feedback till Azure PowerShell-gruppen via en uppsättning instruktioner.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Send-Feedback cmdlet skickar feedback till Azure PowerShell-teamet.

## BESKRIVS

### Exempel 1:
```
PS C:\> Send-Feedback

With zero (0) being the least and ten (10) being the most, how likely are you to recommend Azure PowerShell to a friend or colleague?

10

What does Azure PowerShell do well?

Response.

Upon what could Azure PowerShell improve?

Response.

Please enter your email if you are interested in providing follow up information:

your@email.com
```

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, klient organisationen och prenumerationen som används för kommunikation med Azure.

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

### System. Void

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

