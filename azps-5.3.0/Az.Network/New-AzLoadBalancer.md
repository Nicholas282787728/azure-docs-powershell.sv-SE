---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 558f7bb9937d52117f37cc4964d4dc925b0dca47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421680"
---
# New-AzLoadBalancer

## Sammanfattning
Skapar en belastningsutjämnare.

## FRÅGESYNTAXEN

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzLoadBalancer** skapar en Azure belastnings utjämning.

## BESKRIVS

### Exempel 1: skapa en belastningsutjämnare
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

För att distribuera en belastningsutjämnare måste du först skapa flera objekt och de första sju kommandona visar hur du skapar objekten.
Med kommandot åtto skapas en belastningsutjämnare med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup.
Det nionde och sista kommandot får den nya belastningsutjämnaren för att kontrol lera att den har skapats.
Observera att det här exemplet visar hur du skapar en belastnings utjämning. Du måste också konfigurera den med hjälp av Add-AzNetworkInterfaceIpConfig cmdlet för att koppla nätverkskorten till olika virtuella datorer.

### Exempel 2: skapa en global belastningsutjämnare
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

För att distribuera en global belastningsutjämnare måste du först skapa flera objekt och de första fem kommandona visar hur du skapar objekten.
Med det sjätte kommandot skapar du belastningsutjämnaren med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup.
Det sjunde och sista kommandot får den nya belastningsutjämnaren för att kontrol lera att den har skapats.
Observera att det här exemplet visar hur du skapar en global belastningsutjämnare. Du måste också konfigurera den med hjälp av New-AzLoadBalancerBackendAddressConfig cmdlet för att tilldela regionala startpooler-ID: n till backend-adresspoolen

## MALLPARAMETRAR

### -AsJob
Kör cmdlet i bakgrunden

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

### -BackendAddressPool
Anger en server dels adresspool att koppla till en belastningsutjämnare.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -Force
Anger att denna cmdlet skapar en belastningsutjämnare även om det redan finns en belastningsutjämnare med samma namn.

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

### -FrontendIpConfiguration
Anger en lista över de front-IP-adresser som ska kopplas till en belastningsutjämnare.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InboundNatPool
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InboundNatRule
Anger en lista över inkommande NAT-regler (Network Address Translation) som ska kopplas till en belastningsutjämnare.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancingRule
Anger en lista över regler för belastnings utjämning som ska kopplas till en belastningsutjämnare.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plats
Anger i vilken region du vill skapa en belastningsutjämnare.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på den belastningsutjämnare som skapas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutboundRule
Reglerna för utgående trafik.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sond
Anger en lista över avsökningar som ska kopplas till en belastningsutjämnare.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp där belastningsutjämnaren ska skapas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
SKU-namnet för belastningsutjämnaren.

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

### -Tagg
Par med nyckelord i form av en hash-tabell. Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tier
SKU-nivån för belastningsutjämnaren.

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

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

### System. Collections. hash

### Microsoft. Azure. commands. Network. Models. PSFrontendIPConfiguration []

### Microsoft. Azure. commands. Network. Models. PSBackendAddressPool []

### Microsoft. Azure. commands. Network. Models. PSLoadBalancingRule []

### Microsoft. Azure. commands. Network. Models. PSProbe []

### Microsoft. Azure. commands. Network. Models. PSInboundNatRule []

### Microsoft. Azure. commands. Network. Models. PSInboundNatPool []

### Microsoft. Azure. commands. Network. Models. PSOutboundRule []

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSLoadBalancer

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzNetworkInterfaceIpConfig](./Add-AzNetworkInterfaceIpConfig.md)

[Get-AzLoadBalancer](./Get-AzLoadBalancer.md)

[Remove-AzLoadBalancer](./Remove-AzLoadBalancer.md)

[Set-AzLoadBalancer](./Set-AzLoadBalancer.md)
