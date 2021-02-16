---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226479"
---
# Send-AzIotHubDevice2CloudMessage

## SYNOPSIS
Skicka meddelande om enhet till molnet.

## SYNTAX

### ResourceSet (standard)
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectSet
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceIdSet
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESKRIVNING
Kommandot stöder sändning av meddelanden med program- och systemegenskaper.

## EXEMPEL

### Exempel 1
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

Skickar enhet till molnmeddelande med standardtransporttyp.

### Exempel 2
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

Skickar en mqtt-enhet till ett molnmeddelande.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -DeviceId
Målenhets-ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
IotHub-objekt

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IotHubName
Namn på ot-hubben

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Meddelande
Meddelandetext som ska skickas till IoT-hubben.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gör att det booleska objektet kan returneras. Som standard genererar inte den här cmdleten några utdata.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namn på resursgruppen

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Resurs-ID för IotHub

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TransportType
Transporttyp som ska användas.
Standardvärdet är Amqp.

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSTransportType
Parameter Sets: (All)
Aliases:
Accepted values: Amqp, Http1, Amqp_WebSocket_Only, Amqp_Tcp_Only, Mqtt, Mqtt_WebSocket_Only, Mqtt_Tcp_Only

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte.

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

### Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub

### System.String

## UTDATA

### System.Boolean

## ANTECKNINGAR

## RELATERADE LÄNKAR
