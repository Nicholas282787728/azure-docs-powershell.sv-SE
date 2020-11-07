---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: da3c2e26b5b83f43802734d95d17b8bbcaa4194c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922578"
---
# New-AzAutoscaleNotification

## Sammanfattning
Skapar ett e-postmeddelande med Autoskala.

## FRÅGESYNTAXEN

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzAutoscaleNotification** skapar ett e-postmeddelande för Autoskala.

## BESKRIVS

### Exempel 1: skapa ett e-postmeddelande med Autoskala
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

Det här kommandot skapar ett Autosacale-e-postmeddelande för två angivna adresser.

### Exempel 2: skapa ett e-postmeddelande för en Autoskala för abonnemangs administratören
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

Det här kommandot skapar ett Autosacale-e-postmeddelande för prenumerations administratören.

## MALLPARAMETRAR

### -CustomEmail
Anger en kommaavgränsad lista med e-postadresser.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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

### -SendEmailToSubscriptionAdministrator
Anger att den här åtgärden skickar ett e-postmeddelande till prenumerations administratören.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SendEmailToSubscriptionCoAdministrator
Indikerar att den här åtgärden skickar ett e-postmeddelande till medarbetarna för abonnemanget.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Webhook
Anger en kommaavgränsad lista med Autoskala-webhookar.

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Microsoft. Azure. Management. Monitoring. Management. Models. WebhookNotification []

### System. string []

### System. Management. Automation. SwitchParameter

## VÄRDEN

### Microsoft. Azure. Management. Monitoring. Management. Models. AutoscaleNotification

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzAutoscaleWebhook](./New-AzAutoscaleWebhook.md)


