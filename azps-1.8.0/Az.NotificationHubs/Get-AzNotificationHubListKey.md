---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 7ce6c3c08c1794e2bed794186203a5c6c0d1fdea
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399897"
---
# Get-AzNotificationHubListKey

## SYNOPSIS
Hämtar de primära och sekundära anslutningssträngarna som är kopplade till en auktoriseringsregel för meddelandehubben.

## SYNTAX

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzNotificationHubListKey** returnerar de primära och sekundära anslutningssträngarna för en auktoriseringsregel för meddelandehubben SAS (Shared Access Signature).
Auktoriseringsregler hanterar användarrättigheter till hubben.
Varje regel innehåller en primär och en sekundär anslutningssträng.
Följande anslutningssträngar (URI:er) utförs:
- Peka användare till en resurs.
- Ta med en token som innehåller frågeparametrar.
En av dessa parametrar, signaturen, används för att autentisera användaren och ange angiven åtkomstnivå.

## EXEMPEL

### Exempel 1: Hämta de primära och sekundära anslutningssträngarna för en auktoriseringsregel
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Det här kommandot hämtar de primära och sekundära anslutningssträngarna för auktoriseringsregeln ListenRule, en regel som tilldelas till meddelandehubben ContosoInternalHub.
Kommandot måste innehålla navets namnområde och resursgrupp.

## PARAMETERS

### -AuthorizationRule
Anger namnet på en SAS-autentiseringsregel (Shared Access Signature).
Dessa regler avgör vilken typ av åtkomst användarna har till meddelandehubben.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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
Anger meddelandehubben som den här cmdleten tilldelar en auktoriseringsregel.
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
Resursgrupper organiserar objekt som namnområden, meddelandehubben och auktoriseringsregler på sätt som hjälper dig med lagerhantering och Azure-administration.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys

## ANTECKNINGAR

## RELATERADE LÄNKAR



