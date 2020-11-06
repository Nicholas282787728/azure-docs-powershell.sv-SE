---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 8f2d061fa67ed8e588ae162fbf7bd0a094ae6b1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576582"
---
# <span data-ttu-id="fba7c-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fba7c-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="fba7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fba7c-102">SYNOPSIS</span></span>
<span data-ttu-id="fba7c-103">Tar bort en konfiguration för nätverks gränssnitt från en VMSS.</span><span class="sxs-lookup"><span data-stu-id="fba7c-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fba7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fba7c-104">SYNTAX</span></span>

### <span data-ttu-id="fba7c-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba7c-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fba7c-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba7c-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Id] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fba7c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fba7c-107">DESCRIPTION</span></span>
<span data-ttu-id="fba7c-108">Cmdleten **Remove-AzureRmVmssNetworkInterfaceConfiguration** tar bort en konfiguration för nätverks gränssnitt från en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="fba7c-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="fba7c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fba7c-109">EXAMPLES</span></span>

### <span data-ttu-id="fba7c-110">Exempel 1: ta bort en gränssnitts konfiguration</span><span class="sxs-lookup"><span data-stu-id="fba7c-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="fba7c-111">Det första kommandot får en VMSS med hjälp av Get-AzureRmVmss cmdlet och lagrar den i $VMSS-variabeln.</span><span class="sxs-lookup"><span data-stu-id="fba7c-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="fba7c-112">Med det andra kommandot tas konfigurationen för nätverks gränssnittet bort med namnet ContosoVmssInterface02 från uppsättningen i $VMSS.</span><span class="sxs-lookup"><span data-stu-id="fba7c-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="fba7c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fba7c-113">PARAMETERS</span></span>

### <span data-ttu-id="fba7c-114">-ID</span><span class="sxs-lookup"><span data-stu-id="fba7c-114">-Id</span></span>
<span data-ttu-id="fba7c-115">Anger ID: t för nätverks gränssnitts konfigurationen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="fba7c-115">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba7c-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="fba7c-116">-Name</span></span>
<span data-ttu-id="fba7c-117">Anger namnet på den nätverks gränssnitts konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="fba7c-117">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba7c-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fba7c-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fba7c-119">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="fba7c-119">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="fba7c-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fba7c-120">-Confirm</span></span>
<span data-ttu-id="fba7c-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fba7c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fba7c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fba7c-122">-WhatIf</span></span>
<span data-ttu-id="fba7c-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fba7c-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fba7c-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fba7c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fba7c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba7c-125">CommonParameters</span></span>
<span data-ttu-id="fba7c-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba7c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba7c-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fba7c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba7c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fba7c-128">INPUTS</span></span>

### <span data-ttu-id="fba7c-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="fba7c-129">None</span></span>
<span data-ttu-id="fba7c-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="fba7c-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fba7c-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fba7c-131">OUTPUTS</span></span>

## <span data-ttu-id="fba7c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fba7c-132">NOTES</span></span>

## <span data-ttu-id="fba7c-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fba7c-133">RELATED LINKS</span></span>

[<span data-ttu-id="fba7c-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fba7c-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="fba7c-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fba7c-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


