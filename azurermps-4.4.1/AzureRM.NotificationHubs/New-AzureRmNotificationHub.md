---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: 33dfd5a8c4bde0405351315543078558a5832aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574561"
---
# New-AzureRmNotificationHub

## Sammanfattning
Skapar ett meddelande nav.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### InputFileParameterSet
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NotificationHubParameterSet
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmNotificationHub** skapar ett meddelande nav.
Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.
Meddelande NAV är ungefär likvärdiga med enskilda appar: alla dina appar har vanligt vis sin egen meddelande hubb.

**New-AzureRmNotificationHub-** cmdleten erbjuder två sätt att skapa en ny meddelande-hubb.
Du kan skapa en instans av **NotificationHubAttributes** -objektet och sedan konfigurera det objektet.
Du kan sedan kopiera de här egenskapsvärdena till det nya navet genom att klicka på *NotificationHubObj* -parametern.

Alternativt kan du skapa en JSON-fil (JavaScript-objekttyp) med relevanta konfigurations värden och sedan tillämpa dessa värden genom att använda parametern *InputFile* .

När det används tillsammans med **New-AzureRmNotificationHub-** cmdleten skapar det föregående JSON-exemplet ett meddelande nav med namnet ContosoNotificationHub som finns på den västra amerikanska data Center.

## BESKRIVS

### Exempel 1: skapa ett meddelande nav
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

Det här kommandot skapar ett meddelande nav i namn området ContosoNamespace.
Det nya navet tilldelas till ContosoNotificationsGroup.
Du behöver inte ange ett namn eller annan konfigurations information för navet; den informationen kommer att hämtas från den indatafil som C:\Configurations\InternalHub.js.

## MALLPARAMETRAR

### -InputFile
Anger sökvägen till en JSON-fil som innehåller konfigurations värden för det nya meddelande navet.

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
Anger namn området som meddelande navet ska tilldelas till.

Med namn utrymmen kan du gruppera och kategorisera meddelande nav.
Aviserings NAV måste vara kopplade till ett befintligt namn område.
Cmdleten **New-AzureRmNotificationHub** kan inte skapa ett nytt namn område.

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

### -NotificationHubObj
Anger det **NotificationHubAttributes** -objekt som innehåller konfigurations information för det nya navet.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
Anger den resurs grupp som meddelande navet ska tilldelas till.
Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.

Du måste använda en befintlig resurs grupp.
Cmdleten **New-AzureRmNotificationHub** kan inte skapa en ny resurs grupp.

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

### Microsoft. Azure. commands. NotificationHubs. Models. NotificationHubAttributes

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmNotificationHub](./Get-AzureRmNotificationHub.md)

[Remove-AzureRmNotificationHub](./Remove-AzureRmNotificationHub.md)

[Set-AzureRmNotificationHub](./Set-AzureRmNotificationHub.md)


