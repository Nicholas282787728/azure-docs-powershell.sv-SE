---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093385"
---
# Get-AzureAutomationCredential

## Sammanfattning

Hämtar en Azure Automation-autentiseringsuppgift.

## FRÅGESYNTAXEN

### ByAll (standard)
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByName
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Cmdleten **Get-AzureAutomationCredential** hämtar en eller flera Microsoft Azure Automation-uppgifter.
Som standard returneras alla autentiseringsuppgifter.
Ange namnet på en viss autentiseringsuppgift.

## BESKRIVS

### Exempel 1: Hämta alla autentiseringsuppgifter
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

Det här kommandot får alla autentiseringsuppgifter i Automation-kontot som heter Contoso17.

### Exempel 2: skaffa en autentiseringsuppgift
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

Det här kommandot får autentiseringsuppgiften med namnet mina autentiseringsuppgifter.

## MALLPARAMETRAR

### -AutomationAccountName
Anger namnet på Automation-kontot med autentiseringsuppgiften som ska hämtas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på en autentiseringsuppgift som ska hämtas.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

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

### Microsoft. Azure. commands. Automation. Model. CredentialInfo

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureAutomationCredential](./New-AzureAutomationCredential.md)

[Remove-AzureAutomationCredential](./Remove-AzureAutomationCredential.md)

[Set-AzureAutomationCredential](./Set-AzureAutomationCredential.md)


