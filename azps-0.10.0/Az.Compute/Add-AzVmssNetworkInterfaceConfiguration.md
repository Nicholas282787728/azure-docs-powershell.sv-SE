---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 43d7040543beb049f46fce45cab69d9128a8954e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925289"
---
# <span data-ttu-id="6f7b6-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f7b6-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="6f7b6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="6f7b6-103">Lägger till en nätverks gränssnitts konfiguration i VMSS.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="6f7b6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f7b6-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f7b6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f7b6-105">DESCRIPTION</span></span>
<span data-ttu-id="6f7b6-106">Cmdleten **Add-AzVmssNetworkInterfaceConfiguration** lägger till en nätverks gränssnitts konfiguration på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="6f7b6-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="6f7b6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f7b6-107">EXAMPLES</span></span>

### <span data-ttu-id="6f7b6-108">Exempel 1: lägga till en nätverks gränssnitts konfiguration i VMSS</span><span class="sxs-lookup"><span data-stu-id="6f7b6-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="6f7b6-109">Det här kommandot lägger till en nätverks gränssnitts konfiguration i VMSS.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="6f7b6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f7b6-110">PARAMETERS</span></span>

### <span data-ttu-id="6f7b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f7b6-111">-DefaultProfile</span></span>
<span data-ttu-id="6f7b6-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f7b6-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="6f7b6-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="6f7b6-114">Lista med IP-adresser för DNS-servrar för DNS-inställningar.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7b6-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="6f7b6-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="6f7b6-116">Anger om nätverks gränssnittet är en snabb-aktiverad nätverks funktion.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="6f7b6-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="6f7b6-117">-EnableIPForwarding</span></span>
<span data-ttu-id="6f7b6-118">Anger om IP-vidarekoppling är aktiverat på detta nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="6f7b6-119">-ID</span><span class="sxs-lookup"><span data-stu-id="6f7b6-119">-Id</span></span>
<span data-ttu-id="6f7b6-120">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7b6-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f7b6-121">-IpConfiguration</span></span>
<span data-ttu-id="6f7b6-122">Anger nätverks gränssnittets IP-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7b6-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f7b6-123">-Name</span></span>
<span data-ttu-id="6f7b6-124">Anger namnet på nätverks gränssnittets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="6f7b6-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="6f7b6-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="6f7b6-126">ID för nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="6f7b6-127">-Primär</span><span class="sxs-lookup"><span data-stu-id="6f7b6-127">-Primary</span></span>
<span data-ttu-id="6f7b6-128">Anger om nätverks gränssnitt som skapas från nätverks gränssnitts konfigurationen kommer att vara det primära Network Information Center (NIC) för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7b6-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6f7b6-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6f7b6-130">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="6f7b6-131">Du kan använda cmdleten [New-AzVmssConfig](./New-AzVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7b6-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f7b6-132">-Confirm</span></span>
<span data-ttu-id="6f7b6-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f7b6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f7b6-134">-WhatIf</span></span>
<span data-ttu-id="6f7b6-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f7b6-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f7b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f7b6-137">CommonParameters</span></span>
<span data-ttu-id="6f7b6-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f7b6-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f7b6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f7b6-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f7b6-140">INPUTS</span></span>

### <span data-ttu-id="6f7b6-141">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6f7b6-141">VirtualMachineScaleSet</span></span>
<span data-ttu-id="6f7b6-142">Parametern ' VirtualMachineScaleSet ' godkänner värdet av typen ' VirtualMachineScaleSet ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6f7b6-142">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="6f7b6-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f7b6-143">OUTPUTS</span></span>

###  
<span data-ttu-id="6f7b6-144">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="6f7b6-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="6f7b6-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f7b6-145">NOTES</span></span>

## <span data-ttu-id="6f7b6-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f7b6-146">RELATED LINKS</span></span>

[<span data-ttu-id="6f7b6-147">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6f7b6-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
