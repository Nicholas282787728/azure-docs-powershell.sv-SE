---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090505"
---
# New-AzNotificationHubsNamespaceAuthorizationRule

## Sammanfattning
Skapar en auktoriseringsregel och tilldelar regeln en namnrymd till ett namn område.

## FRÅGESYNTAXEN

### InputFileParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzNotificationHubsNamespaceAuthorizationRule** skapar en auktoriseringsregel för delad åtkomst-signatur (SAS) och tilldelar den till ett namn område.
Auktoriseringsregler hanterar användar rättigheter till namn området och aviserings nav som ingår i namn området.
Denna cmdlet ger två sätt att skapa en ny auktoriseringsregel och tilldela den till ett namn område.
Du kan skapa en instans av **SharedAccessAuthorizationRuleAttributes** -objektet och sedan konfigurera objektet med de egenskaps värden du vill att den nya regeln ska ha.
Det här kan du göra med .NET Framework.
Du kan sedan kopiera de här egenskaps värdena till den nya regeln genom att använda parametern *SASRule* .
Alternativt kan du skapa en JSON-fil (JavaScript-objekttyp) med relevanta konfigurations värden och sedan tillämpa dessa värden genom att använda parametern *InputFile* .
En JSON-fil är en textfil som använder syntax av följande slag: {  
    "Namn": "ContosoAuthorizationRule";  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";  
    "Rättigheter": \[  
        "Lyssna",  
        Bifoga  
    \]  
} När det används tillsammans med **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet skapar det föregående JSON-exemplet en auktoriseringsregel med namnet ContosoAuthorizationRule som gör att användarna lyssnar och skickar rättigheter till namn området.
*PrimaryKey* som används för inloggningsautentisering kan skapas slumpmässigt med hjälp av följande Windows PowerShell-kommando: \[ konvertera \] :: ToBase64String ((1.. 32 |% { \[ byte/] (Get-slump-minimum 0-maximalt 255)}))

## BESKRIVS

### Exempel 1: skapa en auktoriseringsregel och tilldela den till ett namn område
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

Det här kommandot skapar en auktoriseringsregel och tilldelar regeln till namn området ContosoNamespace.
När du skapar den här regeln måste du ange lämpligt namnrymd och resurs gruppen som namn området är tilldelat till.
Men du behöver inte ange någon information om regeln själv: regel informationen kommer att hämtas från den indatafil som C:\Configuration\NamespaceAuthorizationRules.js.

## MALLPARAMETRAR

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

### -InputFile
Anger sökvägen till en JSON-fil som innehåller konfigurations information för den nya auktoriseringsregeln.

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

### -Namnrymd
Anger namn området som auktoriseringsregler ska tilldelas till.
Med namn utrymmen kan du gruppera och kategorisera meddelande nav.
De nya reglerna måste kopplas till ett befintligt namn område.
Cmdleten **New-AzNotificationHubsNamespaceAuthorizationRule** kan inte skapa ett nytt namn område.

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
Anger den resurs grupp som namn området tilldelats till.
Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.
Du måste använda en befintlig resurs grupp.
Denna cmdlet kan inte skapa en ny resurs grupp.

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
Anger det **SharedAccessAuthorizationRuleAttributes** -objekt som innehåller konfigurations information för de nya reglerna.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


