---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323196"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## Sammanfattning
Hämtar information om de auktoriseringsregler som är associerade med en namnrymd för meddelande navet.

## FRÅGESYNTAXEN

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzNotificationHubsNamespaceAuthorizationRule** returnerar information om behörighets reglerna för de delade Access-signaturerna (säkerhets associationer) som är associerade med ett namn område.
Du kan returnera information om alla regler som är kopplade till namn området.
Du kan också returnera information för en viss regel genom att ta med parametern *AuthorizationRule* .
Auktoriseringsregler hanterar åtkomst till namn utrymmen.
Detta görs genom att länkar skapas som URI: er baserat på olika behörighets nivåer.
Plattforms nivåerna kan vara något av följande: 
- Lyssna
- Bifoga
- Hantera klienter dirigeras till en av dessa URI: er baserat på rätt behörighets nivå.
Till exempel kommer en klient med lyssnings behörighet att dirigeras till URI för den behörigheten.
Denna cmdlet får bara auktoriseringsregler som är associerade med ett namn område.
Använd Get-AzNotificationHubsNamespace för att få information om själva namn området.

## BESKRIVS

### Exempel 1: få information om alla auktoriseringsregler som tilldelats till namn områden
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Med det här kommandot får du information om alla auktoriseringsregler som tilldelats både namn områdets ContosoNamespace och ContosoNotificationsGroup.

### Exempel 2: Hämta information om en auktoriseringsregel
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Det här kommandot får information om en enda auktoriseringsregel med namnet ListenRule.
Du måste inkludera namn området och resurs gruppen när du får information för en specifik auktoriseringsregel.

## MALLPARAMETRAR

### -AuthorizationRule
Anger namnet på en SAS-autentiseringsprocess.
Dessa regler bestämmer vilken typ av åtkomst användare har till namn området.

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

### -Namnrymd
Anger namn området som auktoriseringsregler tilldelas.
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

### -ResourceGroup
Anger resurs gruppen som auktoriseringsregler tilldelas.
Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.

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

## VÄRDEN

### Microsoft. Azure. commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


