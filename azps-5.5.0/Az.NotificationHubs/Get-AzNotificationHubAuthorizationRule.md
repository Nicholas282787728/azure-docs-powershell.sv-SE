---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225599"
---
# Get-AzNotificationHubAuthorizationRule

## SYNOPSIS
Hämtar information om auktoriseringsregler som är kopplade till ett meddelandenav.

## SYNTAX

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzNotificationHubAuthorizationRule** hämtar information om SAS-auktoriseringsregler (Shared Access Signature) som är kopplade till ett meddelandenav.
Cmdleten returnerar information om alla regler som är associerade med ett nav eller, genom att inkludera *AuthorizationRule-parametern,* hämtar information om en viss regel.
Auktoriseringsregler hanterar åtkomst till dina meddelandehubben.
En auktoriseringsregel skapar länkar som en URI baserat på olika behörighetsnivåer.
Klienter dirigeras till någon av dessa URI:er baserat på rätt behörighetsnivå.
Till exempel dirigeras en klient med behörigheten Lyssna till URI:en för den behörigheten.
Cmdleten **Get-AzNotificationHubAuthorizationRule** hämtar bara information om auktoriseringsregler som är kopplade till ett meddelandenav.
Om du vill ha information om själva navet använder du Get-AzNotificationHub.

## EXEMPEL

### Exempel 1: Hämta information för alla auktoriseringsregler som tilldelats till ett meddelandenav
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

Det här kommandot hämtar information för alla auktoriseringsregler som tilldelats meddelandehubben ContosoInternalHub i namnområdet ContosoNamespace.
Du måste ange namnområdet där hubben finns samt resursgruppen som navet har tilldelats till.

### Exempel 2: Hämta information för en auktoriseringsregler som tilldelats till ett meddelandenav
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

Det här kommandot hämtar information för alla auktoriseringsregler som tilldelats meddelandehubben ContosoInternalHub i namnområdet ContosoNamespace.
Kommandot använder parametern *AuthorizationRule för* att begränsa data som returneras till en enda auktoriseringsregel med namnet ListenRule.

## PARAMETERS

### -AuthorizationRule
Anger namnet på en SAS-autentiseringsregel.
Dessa regler avgör vilken typ av åtkomst användarna har till meddelandehubben.

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
Anger meddelandehubben som den här cmdleten tilldelar auktoriseringsregler.
Meddelandehubben används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.

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
Anger den resursgrupp som meddelandehubben är tilldelad till.
Resursgrupper ordnar objekt som namnområden, meddelandehubben och auktoriseringsregler på ett sätt som förenklar lagerhantering och Azure-administration.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubauthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


