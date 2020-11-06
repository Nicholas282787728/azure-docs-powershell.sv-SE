---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 5d2398e86a5507e5672dba46cafbbb1f27c402a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585396"
---
# Get-AzureRmNotificationHubAuthorizationRules

## Sammanfattning
Hämtar information om de auktoriseringsregler som är associerade med ett meddelande nav.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmNotificationHubAuthorizationRules** hämtar information om de auktoriseringsregler som är associerade med en meddelande hubb.
Cmdleten returnerar information om alla regler som associeras med ett nav eller, genom att inkludera parametern *AuthorizationRule* , får du information om en viss regel.

Auktoriseringsregler hantera åtkomst till dina meddelande nav.
En auktoriseringsregel skapar länkar, som en URI, baserat på olika behörighets nivåer.
Klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.
Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.

Cmdleten **Get-AzureRmNotificationHubAuthorizationRules** får bara information om de auktoriseringsregler som är associerade med en meddelande hubb.
Använd Get-AzureRmNotificationHub för att få information om navet själv.

## BESKRIVS

### Exempel 1: Hämta information om alla auktoriseringsregler som tilldelats ett meddelande nav
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

Med det här kommandot får du information för alla auktoriseringsregler som tilldelats till aviserings navet som heter ContosoInternalHub i namn området ContosoNamespace.
Du måste ange namn området där navet finns samt resurs gruppen som navet tilldelats till.

### Exempel 2: Hämta information om en auktoriseringsregel som tilldelats ett meddelande nav
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

Med det här kommandot får du information för alla auktoriseringsregler som tilldelats till aviserings navet som heter ContosoInternalHub i namn området ContosoNamespace.
Kommandot använder parametern *AuthorizationRule* för att begränsa vilka data som returneras till en enda auktoriseringsregel med namnet ListenRule.

## MALLPARAMETRAR

### -AuthorizationRule
Anger namnet på en SAS-autentiseringsprocess.
Dessa regler bestämmer vilken typ av åtkomst användare har till meddelande navet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Anger meddelandets hubb som den här cmdleten tilldelar auktoriseringsregler.
Meddelande nav används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.

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
Anger den resurs grupp som meddelande navet tilldelats till.
Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar hantering av lager och Azure-administrationen.

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

### System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[New-AzureRmNotificationHubAuthorizationRules](./New-AzureRmNotificationHubAuthorizationRules.md)

[Remove-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[Set-AzureRmNotificationHubAuthorizationRules](./Set-AzureRmNotificationHubAuthorizationRules.md)


