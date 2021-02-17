---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 88e43b182694b50169738e0b775d9202aac15ffa
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399863"
---
# Get-AzNotificationHubsNamespaceListKey

## SYNOPSIS
Hämtar de primära och sekundära anslutningssträngarna som är kopplade till en namnområdesauktoriseringsregel för meddelandehubben.

## SYNTAX

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzNotificationHubsNamespaceListKey** returnerar de primära och sekundära anslutningssträngarna för en SAS-auktoriseringsregel (Shared Access Signature) som tilldelats till ett meddelandehubbens namnområde.
Auktoriseringsregler hanterar användarrättigheter till ett namnområde för meddelandehubben.
Varje regel innehåller en primär och en sekundär anslutningssträng.

## EXEMPEL

### Exempel 1: Hämta de primära och sekundära anslutningssträngarna för en auktoriseringsregel
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Det här kommandot returnerar de primära och sekundära anslutningssträngarna för auktoriseringsregeln med namnet ListenRule som tilldelats contosoNamespace-namnområdet.
När du kör det här kommandot måste du inkludera namnet på den resursgrupp som namnområdet är tilldelat till.

## PARAMETERS

### -AuthorizationRule
Anger namnet på en SAS-autentiseringsregel.
Dessa regler avgör vilken typ av åtkomst användarna har till meddelandehubben.

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
Anger namnområdet som innehåller de anslutningssträngar som denna cmdlet hämtar.

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

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)



