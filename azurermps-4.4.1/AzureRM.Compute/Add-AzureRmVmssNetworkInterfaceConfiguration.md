---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 651e339de5782d288350535ba1b0527d7a3eb0de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579776"
---
# <span data-ttu-id="94571-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="94571-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="94571-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94571-102">SYNOPSIS</span></span>
<span data-ttu-id="94571-103">Lägger till en nätverks gränssnitts konfiguration i VMSS.</span><span class="sxs-lookup"><span data-stu-id="94571-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94571-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94571-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94571-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94571-105">DESCRIPTION</span></span>
<span data-ttu-id="94571-106">Cmdleten **Add-AzureRmVmssNetworkInterfaceConfiguration** lägger till en nätverks gränssnitts konfiguration på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="94571-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="94571-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94571-107">EXAMPLES</span></span>

### <span data-ttu-id="94571-108">Exempel 1: lägga till en nätverks gränssnitts konfiguration i VMSS</span><span class="sxs-lookup"><span data-stu-id="94571-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="94571-109">Det här kommandot lägger till en nätverks gränssnitts konfiguration i VMSS.</span><span class="sxs-lookup"><span data-stu-id="94571-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="94571-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94571-110">PARAMETERS</span></span>

### <span data-ttu-id="94571-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94571-111">-DefaultProfile</span></span>
<span data-ttu-id="94571-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94571-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94571-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="94571-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="94571-114">Lista med IP-adresser för DNS-servrar för DNS-inställningar.</span><span class="sxs-lookup"><span data-stu-id="94571-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94571-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="94571-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="94571-116">Anger om nätverks gränssnittet är en snabb-aktiverad nätverks funktion.</span><span class="sxs-lookup"><span data-stu-id="94571-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94571-117">-ID</span><span class="sxs-lookup"><span data-stu-id="94571-117">-Id</span></span>
<span data-ttu-id="94571-118">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="94571-118">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94571-119">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="94571-119">-IpConfiguration</span></span>
<span data-ttu-id="94571-120">Anger nätverks gränssnittets IP-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="94571-120">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94571-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="94571-121">-Name</span></span>
<span data-ttu-id="94571-122">Anger namnet på nätverks gränssnittets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="94571-122">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="94571-123">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="94571-123">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="94571-124">ID för nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="94571-124">Id of the network security group.</span></span>

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

### <span data-ttu-id="94571-125">-Primär</span><span class="sxs-lookup"><span data-stu-id="94571-125">-Primary</span></span>
<span data-ttu-id="94571-126">Anger om nätverks gränssnitt som skapas från nätverks gränssnitts konfigurationen kommer att vara det primära Network Information Center (NIC) för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="94571-126">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94571-127">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="94571-127">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="94571-128">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="94571-128">Specifies the VMSS object.</span></span>
<span data-ttu-id="94571-129">Du kan använda cmdleten [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="94571-129">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94571-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94571-130">-Confirm</span></span>
<span data-ttu-id="94571-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94571-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94571-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94571-132">-WhatIf</span></span>
<span data-ttu-id="94571-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94571-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94571-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94571-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94571-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94571-135">CommonParameters</span></span>
<span data-ttu-id="94571-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94571-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94571-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94571-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94571-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94571-138">INPUTS</span></span>

## <span data-ttu-id="94571-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94571-139">OUTPUTS</span></span>

###  
<span data-ttu-id="94571-140">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="94571-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="94571-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94571-141">NOTES</span></span>

## <span data-ttu-id="94571-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94571-142">RELATED LINKS</span></span>

[<span data-ttu-id="94571-143">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="94571-143">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
