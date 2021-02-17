---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 3fb98dc1ef4b13b87fc7cfa41e165d9bc24fc17c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227310"
---
# New-AzNotificationHub

## SYNOPSIS
Skapar ett meddelandenav.

## SYNTAX

### InputFileParameterSet
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NotificationHubParameterSet
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzNotificationHub** skapar ett meddelandenav.
Meddelandehubben används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.
Meddelandehubben motsvarar på ungefär samma sätt enskilda appar: var och en av dina appar har vanligtvis ett eget meddelandenav.
Med **cmdleten New-AzNotificationHub** kan du skapa ett nytt meddelandenav på två sätt.
Du kan skapa en instans av **NotificationHubAttributes-objektet** och sedan konfigurera objektet.
Sedan kan du kopiera egenskapsvärdena till det nya navet med *parametern NotificationHubObj.*
Du kan också skapa en JSON-fil (JavaScript Object Notation) som innehåller de relevanta konfigurationsvärdena och sedan använda dessa värden med hjälp av *InputFile-parametern.*
När det används tillsammans med cmdleten **New-AzNotificationHub** skapar det föregående JSON-exemplet ett meddelandenav med namnet ContosoNotificationHub på datacentret väst usa.

## EXEMPEL

### Exempel 1: Skapa ett meddelandenav
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

Det här kommandot skapar ett meddelandehubben i namnområdet ContosoNamespace.
Det nya navet tilldelas till ContosoNotificationsGroup.
Du behöver inte ange ett namn eller någon annan konfigurationsinformation för navet. den informationen kommer att tas från den indatafil C:\Configurations\InternalHub.jspå.

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

### -InputFile
Anger sökvägen till en JSON-fil som innehåller konfigurationsvärden för det nya meddelandehubben.

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
Anger det namnområde som meddelandehubben ska tilldelas till.
Namnområden är ett sätt att gruppera och kategorisera meddelandehubben.
Meddelandehubben måste tilldelas till ett befintligt namnområde.
Cmdleten **New-AzNotificationHub** kan inte skapa ett nytt namnområde.

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
Anger det **NotificationHubAttributes-objekt** som innehåller konfigurationsinformation för det nya navet.

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
Anger den resursgrupp som meddelandehubben ska tilldelas till.
Resursgrupper organiserar objekt som namnområden, meddelandehubben och auktoriseringsregler på sätt som hjälper dig med lagerhantering och Azure-administration.
Du måste använda en befintlig resursgrupp.
Cmdleten **New-AzNotificationHub** kan inte skapa en ny resursgrupp.

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

### Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzNotificationHub](./Get-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


