---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101743"
---
# Set-AzAutomationModule

## Sammanfattning
Uppdaterar en modul i Automation.

## FRÅGESYNTAXEN

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzAutomationModule** uppdaterar en modul i Azure Automation.
Det här kommandot accepterar en komprimerad fil som har fil namns tillägget. zip.
Filen innehåller en mapp som innehåller en fil som är en av följande typer: 
- wps_2 modul, som har fil namns tillägget. psm1 eller. dll 
- wps_2 modul manifest, som har fil namns tillägget. psd1 namnet på zip-filen, namnet på mappen och namnet på filen i mappen måste vara samma.
Ange zip-filen som en webb adress som Automation-tjänsten kan komma åt.
Om du importerar en wps_2 modul till Automation med denna cmdlet eller New-AzAutomationModule cmdlet är åtgärden asynkron.
Kommandot slutförs om importen lyckas eller inte.
Om du vill kontrol lera om det lyckades kör du följande kommando: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` Modulnamn kontrol lera egenskapen **ProvisioningState** efter värdet lyckades.

## BESKRIVS

### Exempel 1: uppdatera en modul
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

Det här kommandot importerar en uppdaterad version av en befintlig modul som heter ContosoModule till Automation-kontot med namnet Contoso17.  Modulen är lagrad i en Azure-blob i ett lagrings konto med namnet contosostorage och en container som heter modules.

## MALLPARAMETRAR

### -AutomationAccountName
Anger namnet på det Automation-konto som denna cmdlet uppdaterar en modul för.

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
Anger URL-adressen till zip-filen som innehåller den nya versionen av en modul som denna cmdlet importerar.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkVersion
Anger vilken version av modulen som den här cmdleten uppdaterar Automation.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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
Anger namnet på en resurs grupp som denna cmdlet uppdaterar en modul för.

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

[New-AzAutomationModule](./New-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)


