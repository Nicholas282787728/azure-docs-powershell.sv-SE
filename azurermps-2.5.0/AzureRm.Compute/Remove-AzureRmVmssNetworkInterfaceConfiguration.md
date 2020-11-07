---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
ms.openlocfilehash: 46058901188b99eb30d088e2ea784fdc0df8d782
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931030"
---
# <span data-ttu-id="cbd3d-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbd3d-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="cbd3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbd3d-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd3d-103">Tar bort en konfiguration för nätverks gränssnitt från en VMSS.</span><span class="sxs-lookup"><span data-stu-id="cbd3d-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbd3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbd3d-104">SYNTAX</span></span>

### <span data-ttu-id="cbd3d-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbd3d-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbd3d-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbd3d-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbd3d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbd3d-107">DESCRIPTION</span></span>
<span data-ttu-id="cbd3d-108">Cmdleten **Remove-AzureRmVmssNetworkInterfaceConfiguration** tar bort en konfiguration för nätverks gränssnitt från en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="cbd3d-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="cbd3d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbd3d-109">EXAMPLES</span></span>

### <span data-ttu-id="cbd3d-110">Exempel 1: ta bort en gränssnitts konfiguration</span><span class="sxs-lookup"><span data-stu-id="cbd3d-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="cbd3d-111">Det första kommandot får en VMSS med hjälp av Get-AzureRmVmss cmdlet och lagrar den i $VMSS-variabeln.</span><span class="sxs-lookup"><span data-stu-id="cbd3d-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="cbd3d-112">Med det andra kommandot tas konfigurationen för nätverks gränssnittet bort med namnet ContosoVmssInterface02 från uppsättningen i $VMSS.</span><span class="sxs-lookup"><span data-stu-id="cbd3d-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="cbd3d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbd3d-113">PARAMETERS</span></span>

### <span data-ttu-id="cbd3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd3d-114">-DefaultProfile</span></span>
<span data-ttu-id="cbd3d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd3d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbd3d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="cbd3d-116">-Id</span></span>
<span data-ttu-id="cbd3d-117">Anger ID: t för nätverks gränssnitts konfigurationen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="cbd3d-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cbd3d-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="cbd3d-118">-Name</span></span>
<span data-ttu-id="cbd3d-119">Anger namnet på den nätverks gränssnitts konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="cbd3d-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cbd3d-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cbd3d-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cbd3d-121">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="cbd3d-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="cbd3d-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cbd3d-122">-Confirm</span></span>
<span data-ttu-id="cbd3d-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cbd3d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbd3d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbd3d-124">-WhatIf</span></span>
<span data-ttu-id="cbd3d-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cbd3d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbd3d-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cbd3d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbd3d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd3d-127">CommonParameters</span></span>
<span data-ttu-id="cbd3d-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd3d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd3d-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd3d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd3d-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbd3d-130">INPUTS</span></span>

### <span data-ttu-id="cbd3d-131">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cbd3d-131">VirtualMachineScaleSet</span></span>
<span data-ttu-id="cbd3d-132">Parametern ' VirtualMachineScaleSet ' godkänner värdet av typen ' VirtualMachineScaleSet ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="cbd3d-132">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="cbd3d-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbd3d-133">OUTPUTS</span></span>

### <span data-ttu-id="cbd3d-134">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cbd3d-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cbd3d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbd3d-135">NOTES</span></span>

## <span data-ttu-id="cbd3d-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbd3d-136">RELATED LINKS</span></span>

[<span data-ttu-id="cbd3d-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbd3d-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="cbd3d-138">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cbd3d-138">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


