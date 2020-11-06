---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
ms.openlocfilehash: a0c3693220ab614dcb84d69bc8c17a0ad632a2b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575033"
---
# Set-AzureRmAutomationModule

## Sammanfattning
Uppdaterar en modul i Automation.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmAutomationModule** uppdaterar en modul i Azure Automation.
Det här kommandot accepterar en komprimerad fil som har fil namns tillägget. zip.
Filen innehåller en mapp som innehåller en fil som är en av följande typer: 

- wps_2 modul, som har fil namns tillägget. psm1 eller. dll 
- wps_2 modul manifest, som har fil namns tillägget. psd1

Namnet på zip-filen, namnet på mappen och namnet på filen i mappen måste vara samma.

Ange zip-filen som en webb adress som Automation-tjänsten kan komma åt.

Om du importerar en wps_2 modul till Automation med denna cmdlet eller New-AzureRmAutomationModule cmdlet är åtgärden asynkron.
Kommandot slutförs om importen lyckas eller inte.
Om du vill kontrol lera om det lyckades kör du följande kommando:

`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `Modulnamn

Kontrol lera värdet slutfört med egenskapen **ProvisioningState** .

## BESKRIVS

### Exempel 1: uppdatera en modul
```
PS C:\>Set-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

Det här kommandot importerar en uppdaterad version av en befintlig modul som heter ContosoModule till Automation-kontot med namnet Contoso17.

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

### Microsoft. Azure. commands. Automation. Model. modul

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmAutomationModule](./Get-AzureRmAutomationModule.md)

[New-AzureRmAutomationModule](./New-AzureRmAutomationModule.md)

[Remove-AzureRmAutomationModule](./Remove-AzureRmAutomationModule.md)


