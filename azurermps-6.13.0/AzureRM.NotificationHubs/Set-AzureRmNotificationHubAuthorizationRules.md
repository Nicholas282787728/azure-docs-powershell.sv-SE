---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 24c65b6f7bf39d4fe046b020a9427dba7bf53aa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576845"
---
# Set-AzureRmNotificationHubAuthorizationRules

## Sammanfattning
Anger auktoriseringsregler för ett meddelande nav.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### InputFileParameterSet
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmNotificationHubAuthorizationRules** ändrar en auktoriseringsregel för en säkerhets Association för en delad Access-signatur som tilldelats till en aviserings hubb.
Auktoriseringsregler hanterar åtkomst till dina meddelande nav genom att skapa länkar, i enlighet med olika behörighets nivåer.
Behörighets nivåerna kan vara något av följande: 
- Lyssna
- Bifoga
- Hantera klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.
Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.
Denna cmdlet erbjuder två sätt att ändra en auktoriseringsregel som tilldelats till ett meddelande nav.
För en kan du skapa en instans av **SharedAccessAuthorizationRuleAttributes** -objektet och sedan konfigurera objektet med de egenskaps värden du vill att regeln ska ha.
Du kan konfigurera objektet med .NET Framework.
Du kan sedan kopiera de här egenskaps värdena till regeln genom att använda parametern *SASRule* .
Alternativt kan du skapa en JSON-fil (JavaScript Object Notation) med relevanta konfigurations värden och sedan tillämpa dessa värden genom *InputFile* -parametern.
En JSON-fil är en textfil som använder syntax som liknar den här: {"name": "ContosoAuthorizationRule".  
  "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";  
  "Rättigheter": \[  
        "Lyssna",  
        Bifoga  
    \]  
  } När det används tillsammans med New-AzureRmNotificationHubAuthorizationRules cmdlet ändrar det föregående JSON-provet en auktoriseringsregel med namnet ContosoAuthorizationRule för att ge användare behörighet att avlyssna och skicka rättigheter till navet.

## BESKRIVS

### Exempel 1: ändra en auktoriseringsregel som tilldelats till ett meddelande nav
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

Det här kommandot ändrar en auktoriseringsregel som tilldelats till aviserings navet med namnet ContosoExternalHub.
Du måste ange namn området där navet finns samt resurs gruppen som navet är tilldelat.
Information om den regel som ändras är inte inkluderad i själva kommandot.
Den informationen finns i stället i C:\Configuration\AuthorizationRules.js.

## MALLPARAMETRAR

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
Fråga inte efter bekräftelse.

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

### -InputFile
Anger sökvägen till en JSON-fil med konfigurations information för den nya regeln.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namnrymd
Anger namn området som meddelande navet tilldelats till.
Med namn utrymmen kan du gruppera och kategorisera meddelande nav.

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

### -NotificationHub
Anger meddelandets hubb som denna cmdlet tilldelar auktoriseringsregler till.
Meddelande nav används för att skicka push-aviseringar till flera klienter oavsett hur dessa klienter används.

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

### -ResourceGroup
Anger den resurs grupp som meddelande navet tilldelats till. Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.

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

### -SASRule
Anger det **SharedAccessAuthorizationRuleAttributes** -objekt som innehåller konfigurations information för de auktoriseringsregler som har ändrats.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)

[New-AzureRmNotificationHubAuthorizationRules](./New-AzureRmNotificationHubAuthorizationRules.md)

[Remove-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)


