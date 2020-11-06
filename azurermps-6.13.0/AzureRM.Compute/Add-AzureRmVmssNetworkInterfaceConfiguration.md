---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 6789b2a0f3309e8011cc6e87a27dbf9f28579d05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577107"
---
# <span data-ttu-id="e3c84-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3c84-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="e3c84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3c84-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c84-103">Lägger till en nätverks gränssnitts konfiguration i VMSS.</span><span class="sxs-lookup"><span data-stu-id="e3c84-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3c84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3c84-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3c84-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3c84-105">DESCRIPTION</span></span>
<span data-ttu-id="e3c84-106">Cmdleten **Add-AzureRmVmssNetworkInterfaceConfiguration** lägger till en nätverks gränssnitts konfiguration på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e3c84-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e3c84-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3c84-107">EXAMPLES</span></span>

### <span data-ttu-id="e3c84-108">Exempel 1: lägga till en nätverks gränssnitts konfiguration i VMSS</span><span class="sxs-lookup"><span data-stu-id="e3c84-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="e3c84-109">Det här kommandot lägger till en nätverks gränssnitts konfiguration i VMSS.</span><span class="sxs-lookup"><span data-stu-id="e3c84-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="e3c84-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3c84-110">PARAMETERS</span></span>

### <span data-ttu-id="e3c84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c84-111">-DefaultProfile</span></span>
<span data-ttu-id="e3c84-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c84-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3c84-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="e3c84-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="e3c84-114">Lista med IP-adresser för DNS-servrar för DNS-inställningar.</span><span class="sxs-lookup"><span data-stu-id="e3c84-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="e3c84-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="e3c84-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="e3c84-116">Anger om nätverks gränssnittet är en snabb-aktiverad nätverks funktion.</span><span class="sxs-lookup"><span data-stu-id="e3c84-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="e3c84-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="e3c84-117">-EnableIPForwarding</span></span>
<span data-ttu-id="e3c84-118">Anger om IP-vidarekoppling är aktiverat på detta nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="e3c84-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="e3c84-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e3c84-119">-Id</span></span>
<span data-ttu-id="e3c84-120">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e3c84-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="e3c84-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3c84-121">-IpConfiguration</span></span>
<span data-ttu-id="e3c84-122">Anger nätverks gränssnittets IP-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="e3c84-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="e3c84-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3c84-123">-Name</span></span>
<span data-ttu-id="e3c84-124">Anger namnet på nätverks gränssnittets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e3c84-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="e3c84-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e3c84-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e3c84-126">ID för nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="e3c84-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="e3c84-127">-Primär</span><span class="sxs-lookup"><span data-stu-id="e3c84-127">-Primary</span></span>
<span data-ttu-id="e3c84-128">Anger om nätverks gränssnitt som skapas från nätverks gränssnitts konfigurationen kommer att vara det primära Network Information Center (NIC) för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e3c84-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="e3c84-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e3c84-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e3c84-130">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="e3c84-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="e3c84-131">Du kan använda cmdleten [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="e3c84-131">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="e3c84-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3c84-132">-Confirm</span></span>
<span data-ttu-id="e3c84-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3c84-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3c84-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3c84-134">-WhatIf</span></span>
<span data-ttu-id="e3c84-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3c84-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3c84-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3c84-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3c84-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c84-137">CommonParameters</span></span>
<span data-ttu-id="e3c84-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c84-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c84-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3c84-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c84-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3c84-140">INPUTS</span></span>

### <span data-ttu-id="e3c84-141">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e3c84-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e3c84-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e3c84-142">System.String</span></span>

### <span data-ttu-id="e3c84-143">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e3c84-143">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e3c84-144">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="e3c84-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="e3c84-145">System. string []</span><span class="sxs-lookup"><span data-stu-id="e3c84-145">System.String[]</span></span>

## <span data-ttu-id="e3c84-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3c84-146">OUTPUTS</span></span>

### <span data-ttu-id="e3c84-147">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e3c84-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e3c84-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3c84-148">NOTES</span></span>

## <span data-ttu-id="e3c84-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3c84-149">RELATED LINKS</span></span>

[<span data-ttu-id="e3c84-150">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e3c84-150">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
