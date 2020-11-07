---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 0b21b5fa3b5b605ee3092a61eaf67a2c63c4346b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755267"
---
# <span data-ttu-id="33ead-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="33ead-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="33ead-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33ead-102">SYNOPSIS</span></span>
<span data-ttu-id="33ead-103">Lägger till en nätverks gränssnitts konfiguration i VMSS.</span><span class="sxs-lookup"><span data-stu-id="33ead-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33ead-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33ead-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33ead-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33ead-105">DESCRIPTION</span></span>
<span data-ttu-id="33ead-106">Cmdleten **Add-AzureRmVmssNetworkInterfaceConfiguration** lägger till en nätverks gränssnitts konfiguration på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="33ead-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="33ead-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33ead-107">EXAMPLES</span></span>

### <span data-ttu-id="33ead-108">Exempel 1: lägga till en nätverks gränssnitts konfiguration i VMSS</span><span class="sxs-lookup"><span data-stu-id="33ead-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="33ead-109">Det här kommandot lägger till en nätverks gränssnitts konfiguration i VMSS.</span><span class="sxs-lookup"><span data-stu-id="33ead-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="33ead-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33ead-110">PARAMETERS</span></span>

### <span data-ttu-id="33ead-111">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="33ead-111">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="33ead-112">Lista med IP-adresser för DNS-servrar för DNS-inställningar.</span><span class="sxs-lookup"><span data-stu-id="33ead-112">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33ead-113">-ID</span><span class="sxs-lookup"><span data-stu-id="33ead-113">-Id</span></span>
<span data-ttu-id="33ead-114">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="33ead-114">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="33ead-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="33ead-115">-IpConfiguration</span></span>
<span data-ttu-id="33ead-116">Anger nätverks gränssnittets IP-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="33ead-116">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="33ead-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="33ead-117">-Name</span></span>
<span data-ttu-id="33ead-118">Anger namnet på nätverks gränssnittets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="33ead-118">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="33ead-119">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="33ead-119">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="33ead-120">ID för nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="33ead-120">Id of the network security group.</span></span>

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

### <span data-ttu-id="33ead-121">-Primär</span><span class="sxs-lookup"><span data-stu-id="33ead-121">-Primary</span></span>
<span data-ttu-id="33ead-122">Anger om nätverks gränssnitt som skapas från nätverks gränssnitts konfigurationen kommer att vara det primära Network Information Center (NIC) för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="33ead-122">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="33ead-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="33ead-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="33ead-124">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="33ead-124">Specifies the VMSS object.</span></span>
<span data-ttu-id="33ead-125">Du kan använda cmdleten [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="33ead-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33ead-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33ead-126">-Confirm</span></span>
<span data-ttu-id="33ead-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33ead-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33ead-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33ead-128">-WhatIf</span></span>
<span data-ttu-id="33ead-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33ead-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33ead-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33ead-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33ead-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ead-131">CommonParameters</span></span>
<span data-ttu-id="33ead-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33ead-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ead-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33ead-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ead-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33ead-134">INPUTS</span></span>

### <span data-ttu-id="33ead-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="33ead-135">None</span></span>
<span data-ttu-id="33ead-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="33ead-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33ead-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33ead-137">OUTPUTS</span></span>

###  
<span data-ttu-id="33ead-138">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="33ead-138">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="33ead-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33ead-139">NOTES</span></span>

## <span data-ttu-id="33ead-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33ead-140">RELATED LINKS</span></span>

[<span data-ttu-id="33ead-141">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="33ead-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
