---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: d2e9ad0d83c573292996b65924ab7078368d328f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757137"
---
# <span data-ttu-id="fe94e-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe94e-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="fe94e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe94e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe94e-103">Hämtar egenskaperna för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="fe94e-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe94e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe94e-104">SYNTAX</span></span>

### <span data-ttu-id="fe94e-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="fe94e-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe94e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="fe94e-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe94e-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="fe94e-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe94e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe94e-108">DESCRIPTION</span></span>
<span data-ttu-id="fe94e-109">Cmdleten **Get-AzureRmVmss** hämtar modellen och instans vyn för en virtuell dators skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="fe94e-109">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="fe94e-110">Model-vyn är de användardefinierade egenskaperna för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="fe94e-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="fe94e-111">Instans visningen är instans nivå statusen för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="fe94e-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="fe94e-112">Ange parametern *InstanceView* om du bara vill få instans visningen av en virtuell dators skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="fe94e-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="fe94e-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe94e-113">EXAMPLES</span></span>

### <span data-ttu-id="fe94e-114">Exempel 1: Hämta egenskaper för en VMSS</span><span class="sxs-lookup"><span data-stu-id="fe94e-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="fe94e-115">Det här kommandot får egenskaperna för VMSS med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="fe94e-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="fe94e-116">Eftersom kommandot inte anger parameter för *InstanceView* -växeln får cmdleten modell läget för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="fe94e-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

## <span data-ttu-id="fe94e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe94e-117">PARAMETERS</span></span>

### <span data-ttu-id="fe94e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe94e-118">-DefaultProfile</span></span>
<span data-ttu-id="fe94e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe94e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe94e-120">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="fe94e-120">-InstanceView</span></span>
<span data-ttu-id="fe94e-121">Anger att denna cmdlet endast får instans visning av den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="fe94e-121">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe94e-122">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="fe94e-122">-OSUpgradeHistory</span></span>
<span data-ttu-id="fe94e-123">Anger att den här cmdleten visar system uppgraderings historiken för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="fe94e-123">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe94e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe94e-124">-ResourceGroupName</span></span>
<span data-ttu-id="fe94e-125">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="fe94e-125">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="fe94e-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fe94e-126">-VMScaleSetName</span></span>
<span data-ttu-id="fe94e-127">Arter namnet på VMSS.</span><span class="sxs-lookup"><span data-stu-id="fe94e-127">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe94e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe94e-128">CommonParameters</span></span>
<span data-ttu-id="fe94e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe94e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe94e-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe94e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe94e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe94e-131">INPUTS</span></span>

### <span data-ttu-id="fe94e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fe94e-132">System.String</span></span>

## <span data-ttu-id="fe94e-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe94e-133">OUTPUTS</span></span>

### <span data-ttu-id="fe94e-134">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fe94e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fe94e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe94e-135">NOTES</span></span>

## <span data-ttu-id="fe94e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe94e-136">RELATED LINKS</span></span>

[<span data-ttu-id="fe94e-137">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe94e-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="fe94e-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe94e-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="fe94e-139">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe94e-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="fe94e-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe94e-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="fe94e-141">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe94e-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="fe94e-142">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe94e-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="fe94e-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe94e-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


