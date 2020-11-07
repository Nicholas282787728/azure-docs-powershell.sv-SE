---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 58029017f4a6a272856f7badd6b09a9ba1f37ac3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744999"
---
# <span data-ttu-id="4b602-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b602-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="4b602-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b602-102">SYNOPSIS</span></span>
<span data-ttu-id="4b602-103">Tar bort en konfiguration för nätverks gränssnitt från en VMSS.</span><span class="sxs-lookup"><span data-stu-id="4b602-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="4b602-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b602-104">SYNTAX</span></span>

### <span data-ttu-id="4b602-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b602-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b602-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b602-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b602-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b602-107">DESCRIPTION</span></span>
<span data-ttu-id="4b602-108">Cmdleten **Remove-AzVmssNetworkInterfaceConfiguration** tar bort en konfiguration för nätverks gränssnitt från en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="4b602-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="4b602-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b602-109">EXAMPLES</span></span>

### <span data-ttu-id="4b602-110">Exempel 1: ta bort en gränssnitts konfiguration</span><span class="sxs-lookup"><span data-stu-id="4b602-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="4b602-111">Det första kommandot får en VMSS med hjälp av Get-AzVmss cmdlet och lagrar den i $VMSS-variabeln.</span><span class="sxs-lookup"><span data-stu-id="4b602-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="4b602-112">Med det andra kommandot tas konfigurationen för nätverks gränssnittet bort med namnet ContosoVmssInterface02 från uppsättningen i $VMSS.</span><span class="sxs-lookup"><span data-stu-id="4b602-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="4b602-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b602-113">PARAMETERS</span></span>

### <span data-ttu-id="4b602-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b602-114">-DefaultProfile</span></span>
<span data-ttu-id="4b602-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b602-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b602-116">-ID</span><span class="sxs-lookup"><span data-stu-id="4b602-116">-Id</span></span>
<span data-ttu-id="4b602-117">Anger ID: t för nätverks gränssnitts konfigurationen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="4b602-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b602-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4b602-118">-Name</span></span>
<span data-ttu-id="4b602-119">Anger namnet på den nätverks gränssnitts konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="4b602-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b602-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4b602-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4b602-121">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="4b602-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="4b602-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4b602-122">-Confirm</span></span>
<span data-ttu-id="4b602-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4b602-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b602-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b602-124">-WhatIf</span></span>
<span data-ttu-id="4b602-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4b602-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b602-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4b602-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b602-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b602-127">CommonParameters</span></span>
<span data-ttu-id="4b602-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b602-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b602-129">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b602-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b602-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b602-130">INPUTS</span></span>

### <span data-ttu-id="4b602-131">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4b602-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="4b602-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4b602-132">System.String</span></span>

## <span data-ttu-id="4b602-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b602-133">OUTPUTS</span></span>

### <span data-ttu-id="4b602-134">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4b602-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4b602-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b602-135">NOTES</span></span>

## <span data-ttu-id="4b602-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b602-136">RELATED LINKS</span></span>

[<span data-ttu-id="4b602-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b602-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="4b602-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4b602-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


