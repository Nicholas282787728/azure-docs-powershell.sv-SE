---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 629f7d0b04c0b5b511e26a25657deb611497f497
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917501"
---
# <span data-ttu-id="5a640-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a640-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="5a640-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a640-102">SYNOPSIS</span></span>
<span data-ttu-id="5a640-103">Lägger till en nätverks gränssnitts konfiguration i VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a640-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="5a640-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a640-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a640-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a640-105">DESCRIPTION</span></span>
<span data-ttu-id="5a640-106">Cmdleten **Add-AzVmssNetworkInterfaceConfiguration** lägger till en nätverks gränssnitts konfiguration på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5a640-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5a640-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a640-107">EXAMPLES</span></span>

### <span data-ttu-id="5a640-108">Exempel 1: lägga till en nätverks gränssnitts konfiguration i VMSS</span><span class="sxs-lookup"><span data-stu-id="5a640-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="5a640-109">Det här kommandot lägger till en nätverks gränssnitts konfiguration i VMSS.</span><span class="sxs-lookup"><span data-stu-id="5a640-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="5a640-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a640-110">PARAMETERS</span></span>

### <span data-ttu-id="5a640-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a640-111">-DefaultProfile</span></span>
<span data-ttu-id="5a640-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a640-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a640-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="5a640-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="5a640-114">Lista med IP-adresser för DNS-servrar för DNS-inställningar.</span><span class="sxs-lookup"><span data-stu-id="5a640-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="5a640-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="5a640-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="5a640-116">Anger om nätverks gränssnittet är en snabb-aktiverad nätverks funktion.</span><span class="sxs-lookup"><span data-stu-id="5a640-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="5a640-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="5a640-117">-EnableIPForwarding</span></span>
<span data-ttu-id="5a640-118">Anger om IP-vidarekoppling är aktiverat på detta nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="5a640-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="5a640-119">-ID</span><span class="sxs-lookup"><span data-stu-id="5a640-119">-Id</span></span>
<span data-ttu-id="5a640-120">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5a640-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="5a640-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a640-121">-IpConfiguration</span></span>
<span data-ttu-id="5a640-122">Anger nätverks gränssnittets IP-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="5a640-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="5a640-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a640-123">-Name</span></span>
<span data-ttu-id="5a640-124">Anger namnet på nätverks gränssnittets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5a640-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="5a640-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="5a640-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="5a640-126">ID för nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="5a640-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="5a640-127">-Primär</span><span class="sxs-lookup"><span data-stu-id="5a640-127">-Primary</span></span>
<span data-ttu-id="5a640-128">Anger om nätverks gränssnitt som skapas från nätverks gränssnitts konfigurationen kommer att vara det primära Network Information Center (NIC) för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="5a640-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="5a640-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5a640-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5a640-130">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="5a640-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="5a640-131">Du kan använda cmdleten [New-AzVmssConfig](./New-AzVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="5a640-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="5a640-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5a640-132">-Confirm</span></span>
<span data-ttu-id="5a640-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5a640-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a640-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a640-134">-WhatIf</span></span>
<span data-ttu-id="5a640-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5a640-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a640-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5a640-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a640-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a640-137">CommonParameters</span></span>
<span data-ttu-id="5a640-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a640-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a640-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a640-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a640-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a640-140">INPUTS</span></span>

### <span data-ttu-id="5a640-141">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5a640-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="5a640-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5a640-142">System.String</span></span>

### <span data-ttu-id="5a640-143">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5a640-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5a640-144">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="5a640-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="5a640-145">System. string []</span><span class="sxs-lookup"><span data-stu-id="5a640-145">System.String[]</span></span>

## <span data-ttu-id="5a640-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a640-146">OUTPUTS</span></span>

### <span data-ttu-id="5a640-147">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5a640-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5a640-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a640-148">NOTES</span></span>

## <span data-ttu-id="5a640-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a640-149">RELATED LINKS</span></span>

[<span data-ttu-id="5a640-150">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5a640-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
