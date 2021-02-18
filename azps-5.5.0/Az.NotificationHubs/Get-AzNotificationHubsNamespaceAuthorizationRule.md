---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252189"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
Hämtar information om auktoriseringsregler som är kopplade till ett namnområde för meddelandehubben.

## SYNTAX

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzNotificationHubsNamespaceAuthorizationRule** returnerar information om SAS-auktoriseringsregler (Shared Access Signature) som är kopplade till ett meddelandehubbens namnområde.
Du kan returnera information om alla regler som är kopplade till namnområdet.
Alternativt, och genom att inkludera *parametern AuthorizationRule,* kan du returnera information för en viss regel.
Auktoriseringsregler hanterar åtkomst till namnområden.
Det gör du genom att skapa länkar, som URI:er, baserat på olika behörighetsnivåer.
Plattformsnivåer kan vara något av följande: 
- Lyssna
- Skicka
- Hantera klienter dirigeras till någon av dessa URI:er baserat på rätt behörighetsnivå.
Till exempel dirigeras en klient som får behörigheten Lyssna till URI:en för den behörigheten.
Den här cmdleten får endast de auktoriseringsregler som är kopplade till ett namnområde.
Om du vill ha information om själva namnområdet använder du Get-AzNotificationHubsNamespace.

## EXEMPEL

### Exempel 1: Få information om alla auktoriseringsregler som tilldelats namnområden
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Med det här kommandot får du information om alla auktoriseringsregler som tilldelats både namnområdet ContosoNamespace och resursgruppen ContosoNotificationsGroup.

### Exempel 2: Få information om en auktoriseringsregel
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Det här kommandot hämtar information om en enda namnområdesauktoriseringsregel med namnet ListenRule.
Du måste ta med namnområdet och resursgruppen när du får information för en viss auktoriseringsregel.

## PARAMETERS

### -AuthorizationRule
Anger namnet på en SAS-autentiseringsregel.
Dessa regler avgör vilken typ av åtkomst användarna har till namnområdet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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
Anger det namnområde som auktoriseringsreglerna har tilldelats till.
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
Anger den resursgrupp som auktoriseringsreglerna tilldelas till.
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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


