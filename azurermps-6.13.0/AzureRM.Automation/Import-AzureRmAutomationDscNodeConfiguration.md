---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 49cd2fdb2d482621ea52f1df88c9bcd95521badd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581792"
---
# Import-AzureRmAutomationDscNodeConfiguration

## Sammanfattning
Importerar ett MOF-dokument som DSC-nodkonfigurationer i Automation.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **import-AzureRmAutomationDscConfiguration** importerar ett MOF-konfigurationsobjekt (Managed Object Format) till Azure Automation som en önskad konfiguration för State Configuration (DSC).
Ange sökvägen till en. MOF-fil.

## BESKRIVS

### Exempel 1: importera DSC-nodkonfigurationer till Automation
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

Det här kommandot importerar en DSC-noduppsättning från filen med namnet webserver webserver. MOF till det Automation-konto som heter Contoso17, under DSC-konfiguration ContosoConfiguration.
Kommandot anger parametern *Force* .
Om det finns en befintlig DSC-nodadress med namnet ContosoConfiguration. webserver ersätter det här kommandot det.

### Exempel 2: importera DSC-nodkonfigurationer till Automation och skapa en ny version och inte befintliga NodeConfiguration.
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

Det här kommandot importerar en DSC-noduppsättning från filen med namnet webserver webserver. MOF till det Automation-konto som heter Contoso17, under DSC-konfiguration ContosoConfiguration.
Kommandot anger parametern *Force* .
Om det finns en befintlig DSC-nodadress med namnet ContosoConfiguration. webserver, lägger det här kommandot till en ny version med namnet ContosoConfiguration [2]. webserver.

## MALLPARAMETRAR

### -AutomationAccountName
Anger namnet på det Automation-konto där denna cmdlet importerar en DSC-noduppsättning.

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

### -ConfigurationName
Anger namnet på en DSC-konfiguration som ska användas som namn område och container för den nod som ska importeras.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -Force
Anger att denna cmdlet ersätter en befintlig DSC-nodkonfigurationer i Automation.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncrementNodeConfigurationBuild
Skapar en ny version för nodkonfigurationer.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Anger sökvägen till MOF-konfigurationsfilen som denna cmdlet importerar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en resurs grupp för vilken denna cmdlet importerar en DSC-noduppsättning.

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

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. Automation. Model. NodeConfiguration

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Exportera-AzureRmAutomationDscConfiguration](./Export-AzureRmAutomationDscConfiguration.md)

[Get-AzureRmAutomationDscConfiguration](./Get-AzureRmAutomationDscConfiguration.md)


