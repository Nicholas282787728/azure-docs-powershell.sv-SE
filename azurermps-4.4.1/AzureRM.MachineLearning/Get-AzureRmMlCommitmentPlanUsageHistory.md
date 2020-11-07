---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: c80278e460368ca6ec78efb4f5e74e456816df47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758055"
---
# Get-AzureRmMlCommitmentPlanUsageHistory

## Sammanfattning
Hämtar information om användnings historik för en viss åtagande plan.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämtar information om användnings historik för en viss åtagande plan, inklusive resurser som används och resurser som finns kvar i planen.

## BESKRIVS

### --------------------------Exempel 1: Hämta användnings historik för en specifik åtagandes plan--------------------------
@ {paragraf = PS C: \\ \> }





```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## MALLPARAMETRAR

### -Namn
Namnet på abonnemanget för Azure ML-åtagandet.

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

### -ResourceGroupName
Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.

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

### Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory []

## ANMÄRKNINGAR
Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml

## RELATERADE LÄNKAR

