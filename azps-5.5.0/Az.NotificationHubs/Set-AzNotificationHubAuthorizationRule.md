---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: f95b016380f640154533f69d3942b8fe12a064d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252188"
---
# Set-AzNotificationHubAuthorizationRule

## SYNOPSIS
Anger auktoriseringsregler för ett meddelandenav.

## SYNTAX

### InputFileParameterSet
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzNotificationHubAuthorizationRule** ändrar en SAS-auktoriseringsregel (Shared Access Signature) som tilldelats till ett meddelandenav.
Auktoriseringsregler hanterar åtkomst till dina meddelandehubben genom att skapa länkar, som URI:er, baserat på olika behörighetsnivåer.
Behörighetsnivåer kan vara något av följande: 
- Lyssna
- Skicka
- Hantera klienter dirigeras till någon av dessa URI:er baserat på rätt behörighetsnivå.
Till exempel dirigeras en klient som får behörigheten Lyssna till URI:en för den behörigheten.
Med den här cmdleten kan du ändra en auktoriseringsregel som tilldelats till ett meddelandenav på två sätt.
Du kan till exempel skapa en instans av objektet **SharedAccessAuthorizationRuleAttributes** och sedan konfigurera objektet med de egenskapsvärden som du vill att regeln ska ha.
Du kan konfigurera objektet via .NET Framework.
Du kan sedan kopiera dessa egenskapsvärden till regeln med hjälp av *SASRule-parametern.*
Du kan också skapa en JSON-fil (JavaScript Object Notation) som innehåller de relevanta konfigurationsvärdena och sedan använda dessa värden via *InputFile-parametern.*
En JSON-fil är en textfil som använder syntax som liknar följande: { "Namn": "ContosoAuthorizationRule",  
  "PrimaryKey": "WE4qH0398AyXjkommando56gg1gMR3NHoMs29KkUnnpUk01Y=",  
  "Rättigheter": \[  
        "Lyssna",  
        "Skicka"  
    \]  
  } När det används tillsammans med New-AzNotificationHubAuthorizationRule-cmdleten ändrar det föregående JSON-exemplet en auktoriseringsregel med namnet ContosoAuthorizationRule för att ge användarna behörigheten Lyssna och skicka till navet.

## EXEMPEL

### Exempel 1: Ändra en auktoriseringsregel som tilldelats till ett meddelandenav
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

Det här kommandot ändrar en auktoriseringsregel som tilldelats meddelandehubben med namnet ContosoExternalHub.
Du måste ange namnområdet där navet finns samt resursgruppen som navet har tilldelats.
Information om den regel som ändras tas inte med i själva kommandot.
Informationen finns i stället i den indatafil som C:\Configuration\AuthorizationRules.jspå.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

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

### -Force
Be inte om bekräftelse.

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
Anger sökvägen till en JSON-fil som innehåller konfigurationsinformation för den nya regeln.

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

### -Namespace
Anger det namnområde som meddelandehubben är tilldelat till.
Namnområden är ett sätt att gruppera och kategorisera meddelandehubben.

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
Anger meddelandehubben som den här cmdleten tilldelar auktoriseringsregler till.
Meddelandehubben används för att skicka push-meddelanden till flera klienter oavsett vilka klienter som används.

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
Anger den resursgrupp som meddelandehubben är tilldelad till. Resursgrupper organiserar objekt som namnområden, meddelandehubben och auktoriseringsregler på ett sätt som bara hjälper lagerhantering och Azure-administration.

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
Anger objektet **SharedAccessAuthorizationRuleAttributes** som innehåller konfigurationsinformation för auktoriseringsreglerna som ändras.

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
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs. Cmdleten körs inte.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[New-AzNotificationHubauthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)


