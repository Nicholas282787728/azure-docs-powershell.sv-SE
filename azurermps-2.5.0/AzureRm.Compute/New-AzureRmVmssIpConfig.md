---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssipconfig
schema: 2.0.0
ms.openlocfilehash: 82c27b6f8f926d273948bdfcb519a10ee1e0a3c7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930686"
---
# New-AzureRmVmssIpConfig

## Sammanfattning
Skapar en IP-konfiguration för ett nätverks gränssnitt för en VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmVmssIpConfig** skapar ett IP-konfigurationsobjekt för ett nätverks gränssnitt med en virtuell dators skalnings uppsättning (VMSS).
Ange konfigurationen från den här cmdleten som *IPConfiguration* för Add-AzureRmVmssNetworkInterfaceConfiguration cmdleten.

## BESKRIVS

### Exempel 1: skapa ett IP-konfigurationsobjekt för ett VMSS gränssnitt
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Det här kommandot skapar ett IP-konfigurationsobjekt med namnet ContosoVmssInterface02.
Kommandot använder ett tidigare definierat undernät-ID som lagras i $SubnetId.
Kommandot lagrar konfigurations inställningarna i $IPConfiguration variabel för senare användning med **Add-AzureRmVmssNetworkInterfaceConfiguration**.

### Exempel 2: skapa ett IP-konfigurationsobjekt som innehåller inställningar för NAT-pool
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

Det här kommandot skapar ett IP-konfigurationsobjekt med namnet ContosoVmssInterface03 och lagrar det sedan i $IPConfiguration variabel för senare användning.
Kommandot använder ett tidigare definierat undernät-ID som lagras i $SubnetId.
Kommandot lagrar konfigurations inställningarna i $IPConfiguration variabel för senare användning.
Kommandot anger värden för parametrarna *LoadBalancerInboundNatPoolsId* och *LoadBalancerBackendAddressPoolsId* .

## MALLPARAMETRAR

### -ApplicationGatewayBackendAddressPoolsId
Anger en matris med referenser till Server delens adresspooler för belastnings utjämning.
Med en skalnings uppsättning kan Server gruppens adresspooler referera till en offentlig och en intern belastningsutjämnare.
Multiple Scale set kan inte använda samma belastningsutjämnare.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSetting
De DNS-inställningar som ska tillämpas på publicIP-adresser.
Domän namns etiketten för DNS-inställningarna för att tillämpas på publicIP-adresser.
Sammanfogningen av domän namns etiketten och VM-indexet blir domän namns etiketterna för de offentliga IP-adresserna som kommer att skapas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Anger ett ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
Anger en matris med referenser till inkommande NAT-pooler (Network Address Translation) för belastnings utjämning.
En skalnings uppsättning kan referera inkommande NAT-pooler för en offentlig och en intern belastningsutjämnare.
Multiple Scale set kan inte använda samma belastningsutjämnare.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
Anger en matris med referenser till inkommande NAT-pooler för belastnings utjämning.
En skalnings uppsättning kan referera inkommande NAT-pooler för en offentlig och en intern belastningsutjämnare.
Multiple Scale set kan inte använda samma belastningsutjämnare.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på IP-konfigurationen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Primär
Anger primär IP-konfiguration om nätverks gränssnittet har mer än en IP-konfiguration.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIPAddressVersion
Ange IP-konfigurationen är IPv4 eller IPv6. Standard är IPv4.  Möjliga värden är: IPv4 och IPv6.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
Idle-timeout för den offentliga IP-adressen.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
Konfigurations namnet för publicIP-adressen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetId
Anger det nätmask-ID som konfigurationen skapar VMSS nätverks gränssnitt för.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmVmssNetworkInterfaceConfiguration](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


