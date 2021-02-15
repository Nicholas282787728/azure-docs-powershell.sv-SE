---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211711"
---
# New-AzVmssIpConfig

## SYNOPSIS
Skapar en IP-konfiguration för ett nätverksgränssnitt för en VMSS.

## SYNTAX

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzVmssIpConfig** skapar ett IP-konfigurationsobjekt för ett nätverksgränssnitt i en VMSS (Virtual Machine Scale Set).
Ange konfigurationen från den här cmdleten som *IPConfiguration-parametern* för den Add-AzVmssNetworkInterfaceConfiguration cmdleten.

## EXEMPEL

### Exempel 1: Skapa ett IP-konfigurationsobjekt för ett VMSS-gränssnitt
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Det här kommandot skapar ett IP-konfigurationsobjekt med namnet ContosoVmssInterface02.
Kommandot använder ett tidigare definierat undernäts-ID som lagrats i $SubnetId.
Kommandot lagrar konfigurationsinställningarna i den $IPConfiguration för senare användning med **Add-AzVmssNetworkInterfaceConfiguration.**

### Exempel 2: Skapa ett IP-konfigurationsobjekt som innehåller INSTÄLLNINGAR för NAT-pool
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

Det här kommandot skapar ett IP-konfigurationsobjekt med namnet ContosoVmssInterface03 och lagrar det sedan i $IPConfiguration variabeln för senare användning.
Kommandot använder ett tidigare definierat undernäts-ID som lagrats i $SubnetId.
Kommandot lagrar konfigurationsinställningarna i den nya $IPConfiguration för senare användning.
Kommandot anger värden för parametrarna *LoadBalancerInboundNatPoolsId* och *LoadBalancerBackendAddressPoolsId.*

## PARAMETERS

### -ApplicationGatewayBackendAddressPoolsId
Anger en matris med referenser till backendadresspooler för belastningsutjämnare.
En skaluppsättning kan referera till backendadresspooler för en offentlig och en intern belastningsutjämnare.
Flera skaluppsättningar kan inte använda samma belastningsutjämning.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DnsSetting
Dns-inställningarna som ska tillämpas på de offentligaIP-adresserna.
Domännamnsetiketten för DNS-inställningarna som ska tillämpas på de offentligaIP-adresserna.
Sammanfogningen av domännamnsetiketten och VM-indexet blir domännamnsetiketterna för de offentliga IP-adressresurser som skapas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
Anger ett ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
Anger en matris med IP-taggobjekt.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
Anger en matris med referenser till NAT-pooler (Incoming Network Address Translation) för belastningsutjämnare.
En skaluppsättning kan referera till inkommande NAT-pooler för en offentlig och en intern belastningsutjämnare.
Flera skaluppsättningar kan inte använda samma belastningsutjämning.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
Anger en matris med referenser till inkommande NAT-pooler för belastningsutjämnare.
En skaluppsättning kan referera till inkommande NAT-pooler för en offentlig och en intern belastningsutjämnare.
Flera skaluppsättningar kan inte använda samma belastningsutjämning.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Anger namnet på IP-konfigurationen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Primary
Anger den primära IP-konfigurationen om nätverksgränssnittet har fler än en IP-konfiguration.

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

### -PrivateIPAddressVersion
Ange IP-konfigurationen för privat IP-adress.  Standardvärdet används som IPv4.  Möjliga värden är: "IPv4" och "IPv6".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
Tidsgränsen för inaktivitet för den offentliga IP-adressen.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
Konfigurationsnamnet för den offentligaIP-adressen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressVersion
Ange IP-konfiguration för offentlig IP-adress.  Standardvärdet används som IPv4.  Möjliga värden är: "IPv4" och "IPv6".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPPrefix
ID för offentlig IP-prefix

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetId
Anger undernätets ID där konfigurationen skapar VMSS-nätverksgränssnittet.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### System.String[]

### System.Int32

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]

## UTDATA

### Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)


