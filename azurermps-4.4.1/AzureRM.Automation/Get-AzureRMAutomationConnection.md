---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
ms.openlocfilehash: e83a4c71656feb9dbe766339244e54038fa56c84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581556"
---
# Get-AzureRmAutomationConnection

## Sammanfattning
Hämtar en automatiserings anslutning.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByAll (standard)
```
Get-AzureRmAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConnectionName
```
Get-AzureRmAutomationConnection [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConnectionTypeName
```
Get-AzureRmAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmAutomationConnection** har en eller flera Azure Automation-anslutningar.
Som standard hämtar denna cmdlet alla anslutningar.
Ange namnet på en anslutning för att få en specifik anslutning.
Ange namnet på anslutnings typen för att få alla anslutningar av en viss typ.

## BESKRIVS

### Exempel 1: Hämta alla anslutningar
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

Det här kommandot får metadata för alla anslutningar i Automation-kontot med namnet Contoso17.

### Exempel 2: Hämta alla anslutningar av en typ
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

Det här kommandot får metadata för anslutningar i Automation-kontot med namnet Contoso17.
Det här kommandot får fram anslutningar av typen SqlServer.

### Exempel 3: skaffa en anslutning
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

Det här kommandot får metadata för anslutningen med namnet ContosoConnection.

## MALLPARAMETRAR

### -AutomationAccountName
Anger namnet på det Automation-konto som denna cmdlet ansluter till.

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

### -ConnectionTypeName
Anger namnet på en Anslutnings typ för vilken denna cmdlet hämtar anslutningar.

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på en anslutning som hämtas av denna cmdlet.

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en resurs grupp som denna cmdlet ansluter till.

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

### Microsoft. Azure. commands. Automation. Model. Connection

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmAutomationConnection](./New-AzureRMAutomationConnection.md)

[Remove-AzureRmAutomationConnection](./Remove-AzureRMAutomationConnection.md)


