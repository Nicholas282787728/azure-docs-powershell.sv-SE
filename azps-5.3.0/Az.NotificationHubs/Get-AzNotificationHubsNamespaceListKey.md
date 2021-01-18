---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 2217a0c8aa68e815b650cd3eb564ce7a21733e72
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525712"
---
# Get-AzNotificationHubsNamespaceListKey

## Sammanfattning
Hämtar de primära och sekundära anslutnings strängar som är associerade med en auktoriseringsregel för ett namn område för en aviserings hubb.

## FRÅGESYNTAXEN

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzNotificationHubsNamespaceListKey** returnerar de primära och sekundära anslutnings strängarna för en auktoriseringsregel för en delad Access-signatur som tilldelats ett namn område i en aviserings hubb.
Auktoriseringsregler hanterar användar rättigheter till ett namn område för aviseringar.
Varje regel innehåller en primär och en sekundär anslutnings sträng.

## BESKRIVS

### Exempel 1: Hämta primära och sekundära anslutnings strängar för en auktoriseringsregel
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Det här kommandot returnerar de primära och sekundära anslutnings strängarna för auktoriseringsregeln som heter ListenRule tilldelade till ContosoNamespace namn området.
När du kör det här kommandot måste du ange namnet på den resurs grupp som namn området är tilldelat till.

## MALLPARAMETRAR

### -AuthorizationRule
Anger namnet på en SAS-autentiseringsprocess.
Dessa regler bestämmer vilken typ av åtkomst användare har till meddelande navet.

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
Anger namn området som innehåller de anslutnings strängar som den här cmdleten får.

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

### Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)


