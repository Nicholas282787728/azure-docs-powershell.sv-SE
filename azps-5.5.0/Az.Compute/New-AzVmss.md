---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 4953e914cc52784cd815be80307babfe05f3b63c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211719"
---
# New-AzVmss

## SYNOPSIS
Skapar en VMSS.

## SYNTAX

### DefaultParameter (standard)
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzVmss** skapar en VMSS (Virtual Machine Scale Set) i Azure.
Använd den enkla parameteruppsättningen `SimpleParameterSet` () om du snabbt vill skapa en förinställt VMSS och tillhörande resurser. Använd standardparameteruppsättningen () för mer avancerade scenarier när du behöver konfigurera varje komponent i VMSS och varje associerad resurs innan `DefaultParameter` du skapar den.

## EXEMPEL

### Exempel 1: Skapa en VMSS med hjälp av **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

Kommandot ovan skapar följande med `$vmssName` namnet:
* En resursgrupp
* Ett virtuellt nätverk
* En belastningsutjämning
* En offentlig IP
* VMSS med 2 instanser

Standardbilden som valts för virtuella maskiner i VMSS är `2016-Datacenter Windows Server` och SKU:n är `Standard_DS1_v2`

### Exempel 2: Skapa en VMSS med hjälp av **`DefaultParameterSet`**
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

Det komplexa exemplet ovan skapar en VMSS, som följer en förklaring till vad som händer:
* Det första kommandot skapar en resursgrupp med angivet namn och angiven plats.
* Det andra kommandot använder **cmdleten New-AzStorageAccount** för att skapa ett lagringskonto.
* Det tredje kommandot använder sedan cmdleten **Get-AzStorageAccount** för att hämta lagringskontot som skapas i det andra kommandot och lagrar resultatet i $STOAccount variabeln.
* Det femte kommandot använder cmdleten **New-AzVirtualNetworkSubnetConfig** för att skapa ett undernät och lagrar resultatet i variabeln $SubNet.
* Det sjätte kommandot använder cmdleten **New-AzVirtualNetwork** för att skapa ett virtuellt nätverk och lagrar resultatet i variabeln $VNet.
* Det sjunde kommandot använder **Get-AzVirtualNetwork** för att få information om det virtuella nätverket som skapades i det sjätte kommandot och lagrar informationen i variabeln $VNet.
* Det åttonde och nionde kommandot använder **New-AzPublicIpAddress** och **Get- AzureRmPublicIpAddress** för att skapa och hämta information från den offentliga IP-adressen.
* Kommandona lagrar informationen i variabeln med namnet $PubIP.
* Det tionde kommandot använder cmdleten **New- AzureRmLoadBalancerFrontendIpConfig** för att skapa en frontend load balancer och lagrar resultatet i variabeln $Frontend.
* Det elfte kommandot använder **New-AzLoadBalancerBackendAddressPoolConfig** för att skapa en konfiguration av backend-adresspool och lagrar resultatet i variabeln $BackendAddressPool.
* Det tolfte kommandot använder **New-AzLoadBalancerProbeConfig** för att skapa en sonder och lagrar den sonde informationen i variabeln $Probe.
* Det trettonde kommandot använder cmdleten **New-AzLoadBalancerInboundNatPoolConfig** för att skapa en konfiguration av nat-pooler (load balancer inbound network address translation).
* Det fjortonde kommandot använder **New-AzLoadBalancerRuleConfig** för att skapa en konfiguration av belastningsutjämningsregel och lagrar resultatet i variabeln $LBRule.
* Det femtonde kommandot använder cmdleten **New-AzLoadBalancer** för att skapa en belastningsutjämning och lagrar resultatet i variabeln $ActualLb.
* Det femtonde kommandot använder **Get-AzLoadBalancer** för att hämta information om belastningsutjämningen som skapades i det femtonde kommandot och lagrar informationen i variabeln $ExpectedLb.
* Det 17:e kommandot använder cmdleten **New-AzVmssIPConfig** för att skapa en VMSS IP-konfiguration och lagrar informationen i variabeln $IPCfg.
* Det åttonde kommandot använder cmdleten **New-AzVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och lagrar resultatet för variabeln $VMSS.
* Det troliga kommandot använder **cmdleten New-AzVmss** för att skapa VMSS.

## PARAMETERS

### -AllocationMethod
Tilldelningsmetod för den offentliga IP-adressen för skaluppsättningen (statisk eller dynamisk).  Om inget värde anges blir tilldelningen statisk.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### -As Ent fån
Kör cmdleten i bakgrunden och returnera ett jobb för att följa förloppet.

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

### -BackendPoolName
Namnet på backend-adresspoolen som ska användas i belastningsutjämaren för den här skaluppsättningen.  Om inget värde anges skapas en ny backendpool med samma namn som skaluppsättningen.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPort
Portnummer för backend som används av belastningsutjämaren för skaluppsättningen för att kommunicera med virtuella maskiner i skaluppsättningen.  Om inga värden anges används portarna 3389 och 5985 för Windows VMS, och port 22 används för virtuella Linux-maskiner.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Administratörsautentiseringsuppgifter (användarnamn och lösenord) för virtuella maskiner i den här skaluppsättningen.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataDiskSizeInGb
Anger storleken på datadiskar i GB.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -DomainNameLabel
Domännamnsetiketten för den offentliga Fully-Qualified domännamnet (FQDN) för den här skaluppsättningen. Det här är den första komponenten i domännamnet som automatiskt tilldelas till skaluppsättningen. Automatiskt tilldelade domännamn använder formuläret ( <DomainNameLabel> . <Location> . cloudapp.azure.com). Om inget värde anges blir standarddomännamnetiketten sammanfogning av <ScaleSetName> <ResourceGroupName> och.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUltraSSD
Använd UltraSSD-diskar för virtuella maskiner i skaluppsättningen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionAtHost
Den här parametern aktiverar kryptering för alla diskar, inklusive en Resource/Temp-disk på själva värden. Standard: Kryptering på värden inaktiveras såvida inte den här egenskapen är inställd på sant för resursen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EvictionPolicy
Skalningsprincipen för den virtuella datorskalorna med låg prioritet.  Endast värden som stöds är "Deallocate" och "Delete".

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPoolName
Namnet på frontend-adresspoolen som ska användas i belastningsutjämaren Skaluppsättning.  Om inget värde anges skapas en ny adresspool på framsidan med samma namn som skaluppsättningen.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostGroupId
Anger den dedikerade värdgrupp som skaluppsättningen för virtuell dator ska finnas i.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -ImageName
Namnet på bilden för virtuella maskiner i den här skaluppsättningen. Om inget värde anges används "Windows Server 2016 DataCenter"-bilden.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceCount
Antalet VM-bilder i skaluppsättningen.  Om inget värde anges skapas 2 instanser.

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerName
Namnet på belastningsutjämaren som ska användas med den här skaluppsättningen.  En ny belastningsutjämnare med samma namn som skaluppsättningen skapas om inget värde anges.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Azure-platsen där den här skaluppsättningen skapas.  Om inget värde anges härförs platsen från platsen för andra resurser som refereras till i parametrarna.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
Det maximala priset för faktureringen för en virtuell skalskala med låg prioritet.

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NatBackendPort
Backend-port för översättning av inkommande nätverksadress.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlatformFaultDomainCount
Antal feldomäner för varje placeringsgrupp.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority
Prioriteten för den virtuella datorn i skaluppsättningen.  Endast värden som stöds är "Normal", "Dekor" och "Låg".
"Normal" är för vanlig virtuell dator.
'Spot' är till för virtuell dator.
'Low' är också för virtuell dator men har ersatts av 'Spot'. Använd "Spot" i stället för "Low".

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
Resurs-ID för gruppen för närhetsplacering som ska användas med den här skalskalan.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressName
Namnet på den offentliga IP-adressen som ska användas med den här skalskalan.  En ny offentlig IPAdress med samma namn som skaluppsättningen skapas om inget värde anges.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resursgruppen för VMSS.  Om inget värde anges skapas en ny Resursgrupp med samma namn som skaluppsättningen.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
De regler som ska följas vid skalning i en skala för en virtuell dator.  Möjliga värden är: "Standard", "ÄldstaVM" och "NyasteVM".  Standard när en uppsättning med virtuella maskiner skalar skalas in balanseras skaluppsättningen först i olika zoner om det är en zonskalauppsättning.  Sedan kommer det att balanseras över feldomäner så långt det är möjligt.  Inom varje feldomän är de virtuella maskiner som valts för borttagning de senaste som inte är skyddade från skalning.  "ÄldstaVM" när en uppsättning av virtuella maskiner skalas in väljs de äldsta virtuella maskinerna som inte skyddas från skalning för borttagning.  För uppsättningar med zonbaserade virtuella maskiner kommer skaluppsättningen först att balanseras mellan zoner.  Inom varje zon väljs de äldsta virtuella maskinerna som inte är skyddade för borttagning.  "NewestVM" när en uppsättning av virtuella maskinskalor skalas in väljs de senaste virtuella maskinerna som inte skyddas från skalning för borttagning.  För uppsättningar med zonbaserade virtuella maskiner kommer skaluppsättningen först att balanseras mellan zoner.  Inom varje zon väljs de senaste virtuella maskinerna som inte är skyddade för borttagning.

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityGroupName
Namnet på den nätverkssäkerhetsgrupp som ska användas för den här skaluppsättningen.  Om inget värde anges skapas en standardnätverkssäkerhetsgrupp med samma namn som skaluppsättningen och används i skaluppsättningen.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
Använd det här till att skapa skalningsuppsättningen i en enskild placeringsgrupp. Standardinställningen är flera grupper

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMs
Anger att tilläggen inte körs på extraometablera virtuella maskiner.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetAddressPrefix
Adressprefixet för det undernät som ska användas i ScaleSet. Standardinställningar för undernät (192.168.1.0/24) används om inget värde anges.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
Namnet på undernätet som ska användas med den här skaluppsättningen.  Ett nytt undernät skapas med samma namn som skaluppsättningen om inget värde anges.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SystemAssignedIdentity
Om parametern finns tilldelas de virtuella maskinerna i skaluppsättningen(är) en hanterad systemidentitet som genereras automatiskt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradePolicyMode
Uppgraderingsprincipläget för VM-instanser i den här skaluppsättningen.  Uppgraderingsprincipen kan specificera automatiska, manuella eller rullande uppgraderingar.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserAssignedIdentity
Namnet på en hanterad tjänst-identitet som ska tilldelas till de virtuella maskinerna i skaluppsättningen.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Anger det **VirtualMachineScaleSet-objekt** som innehåller egenskaperna för de VMSS som den här cmdleten skapar.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
Namnet för det virtuella nätverket som ska användas med den här skaluppsättningen.  Om inget värde anges skapas ett nytt virtuellt nätverk med samma namn som skaluppsättningen.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
Anger namnet på den VMSS som denna cmdlet skapar.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
Storleken på VM-instanser i den här skaluppsättningen.  En standardstorlek (Standard_DS1_v2) används om ingen storlek anges.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### -VnetAddressPrefix
Adressprefixet för det virtuella nätverket som används med den här skaluppsättningen.  Standardinställningar för virtuella nätverksadressprefix (192.168.0.0/16) används om inget värde anges.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zone
En lista med tillgänglighetsområden som anger den IP som tilldelats för resursen måste komma från.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## UTDATA

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzVmss](./Get-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Restart-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stop-AzVmss](./Stop-AzVmss.md)

[Update-AzVmss](./Update-AzVmss.md)


