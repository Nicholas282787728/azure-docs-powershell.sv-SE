---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321871"
---
# New-AzAutomationModule

## Sammanfattning
Importerar en modul till Automation.

## FRÅGESYNTAXEN

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzAutomationModule** importerar en modul till Azure Automation.
Det här kommandot accepterar en komprimerad fil som har fil namns tillägget. zip.
Filen innehåller en mapp som innehåller en fil som är en av följande typer: 
- Windows PowerShell-modul, som har fil namns tillägget. psm1 eller. dll 
- Manifestet för Windows PowerShell, som har fil namns tillägget. psd1 namnet på zip-filen, namnet på mappen och namnet på filen i mappen måste vara samma.
Ange zip-filen som en webb adress som Automation-tjänsten kan komma åt.
Om du importerar en Windows PowerShell-modul till Automation med den här cmdleten eller Set-AzAutomationModule cmdlet är åtgärden asynkron.
Kommandot slutförs om importen lyckas eller inte.
Om du vill kontrol lera om det lyckades kör du följande kommando: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` Modulnamn kontrol lera egenskapen **ProvisioningState** efter värdet lyckades.

## BESKRIVS

### Exempel 1: importera en modul
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

Det här kommandot importerar en modul som heter ContosoModule till det Automation-konto som heter Contoso17.
Modulen är lagrad i en Azure-blob i ett lagrings konto med namnet contosostorage och en container som heter modules.

## MALLPARAMETRAR

### -AutomationAccountName
Anger namnet på det Automation-konto som denna cmdlet importerar en modul för.

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

### -ContentLinkUri
URL-adressen till ett zip-paket för en modul

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
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

### -Namn
Anger namnet på den modul som denna cmdlet importerar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en resurs grupp för vilken denna cmdlet importerar en modul.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### System. URI

## VÄRDEN

### Microsoft. Azure. commands. Automation. Model. modul

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)

[Set-AzAutomationModule](./Set-AzAutomationModule.md)


