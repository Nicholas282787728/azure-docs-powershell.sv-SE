---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: dfdd4d4de935d83beaa20246c490ded7b23dcc9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573564"
---
# Get-AzureRmAutomationRegistrationInfo

## Sammanfattning
Hämtar registrerings information för att hantera en DSC-nod eller hybrid arbetare att automatisera.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmAutomationRegistrationInfo** får den slut punkt och de nycklar som krävs för att hantera en önskad tillstånds konfiguration (DSC) eller hybrid arbetare i ett Azure Automation-konto.

## BESKRIVS

### Exempel 1: få registrerings information
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

Det här kommandot får registrerings informationen för det Automation-konto som heter AutomationAccount01 i resurs gruppen med namnet ResourceGroup01.

## MALLPARAMETRAR

### -AutomationAccountName
Anger namnet på Automation-kontot som denna cmdlet hämtar registrerings information för.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en resurs grupp.
Denna cmdlet hämtar registrerings information för den resurs grupp som den här parametern anger.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. Automation. Model. AgentRegistration

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmAutomationAccount](./Get-AzureRmAutomationAccount.md)

[Get-AzureRmAutomationDscNode](./Get-AzureRmAutomationDscNode.md)

[New-AzureRmAutomationKey](./New-AzureRmAutomationKey.md)


