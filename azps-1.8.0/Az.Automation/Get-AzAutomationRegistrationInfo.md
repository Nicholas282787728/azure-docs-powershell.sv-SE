---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: f915d1637226e7381cf7da53c0a3aea022060be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754836"
---
# Get-AzAutomationRegistrationInfo

## Sammanfattning
Hämtar registrerings information för att hantera en DSC-nod eller hybrid arbetare att automatisera.

## FRÅGESYNTAXEN

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzAutomationRegistrationInfo** får den slut punkt och de nycklar som krävs för att hantera en önskad tillstånds konfiguration (DSC) eller hybrid arbetare i ett Azure Automation-konto.

## BESKRIVS

### Exempel 1: få registrerings information
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

Det här kommandot får registrerings informationen för det Automation-konto som heter AutomationAccount01 i resurs gruppen med namnet ResourceGroup01.

## MALLPARAMETRAR

### -AutomationAccountName
Anger namnet på Automation-kontot som denna cmdlet hämtar registrerings information för.

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

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -ResourceGroupName
Anger namnet på en resurs grupp.
Denna cmdlet hämtar registrerings information för den resurs grupp som den här parametern anger.

```yaml
Type: System.String
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

### System. String

## VÄRDEN

### Microsoft. Azure. commands. Automation. Model. AgentRegistration

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzAutomationAccount](./Get-AzAutomationAccount.md)

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[New-AzAutomationKey](./New-AzAutomationKey.md)


