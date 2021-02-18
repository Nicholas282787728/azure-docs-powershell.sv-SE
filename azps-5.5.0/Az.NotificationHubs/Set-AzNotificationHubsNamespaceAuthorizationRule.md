---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 34f63dfc89f2bb1b3b9601e8ff51b280fee9ee42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252165"
---
# Set-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
Anger auktoriseringsregler för ett namnområde i meddelandehubben.

## SYNTAX

### InputFileParameterSet
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SASRuleParameterSet
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzNotificationHubsNamespaceAuthorizationRule** ändrar en SAS-auktoriseringsregel (Shared Access Signature) som tilldelats till ett meddelandehubbens namnområde.
Auktoriseringsregler hanterar användarrättigheter till namnområdet och till meddelandehubben som finns i namnområdet.
Med den här cmdleten kan du ändra en auktoriseringsregel som tilldelats till ett namnområde på två sätt.
Du kan till exempel skapa en instans av objektet **SharedAccessAuthorizationRuleAttributes** och sedan konfigurera objektet med de egenskapsvärden som du vill att regeln ska ha.
Du kan använda .NET Framework för att uppnå detta.
Du kan sedan kopiera dessa egenskapsvärden till regeln via *SASRule-parametern.*
Du kan också skapa en JSON-fil (JavaScript Object Notation) som innehåller de relevanta konfigurationsvärdena och sedan använda dessa värden via *InputFile-parametern.*
En JSON-fil är en textfil som använder syntax ungefär så här: {  
    "Namn": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXjkommando56gg1gMR3NHoMs29KkUnnpUk01Y=",  
    "Rättigheter": \[  
        "Lyssna",  
        "Skicka"  
    \]  
} När det används tillsammans med cmdleten **Set-AzNotificationHubsNamespaceAuthorizationRule** ändrar det föregående JSON-exemplet en auktoriseringsregel med namnet ContosoAuthorizationRule för att ge användare behörigheten Lyssna och Skicka till namnområdet.

## EXEMPEL

### Exempel 1: Ändra en auktoriseringsregel som tilldelats ett namnområde
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

Det här kommandot ändrar en auktoriseringsregel som tilldelats namnområdet ContosoNamespace.
Du måste ange den resursgrupp som namnområdet är tilldelat till.
Information om auktoriseringsregeln ingår inte i själva kommandot.
I stället hämtas den informationen från den indatafil som C:\Configuration\AuthorizationRules.jspå.

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
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Anger namnområdet som innehåller auktoriseringsreglerna som cmdleten ändrar.
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

### -ResourceGroup
Anger den resursgrupp som namnområdet är tilldelat till.
Resursgrupper organiserar objekt som namnområden, meddelandehubben och auktoriseringsregler på ett sätt som bara hjälper lagerhantering och Azure-administration.

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
Anger objektet **SharedAccessAuthorizationRuleAttributes** som innehåller konfigurationsinformation för auktoriseringsreglerna som denna cmdlet ändrar.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
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

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubsNamespaceAuthorizationRule](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[Remove-AzNotificationHubsNamespaceAuthorizationRule](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


