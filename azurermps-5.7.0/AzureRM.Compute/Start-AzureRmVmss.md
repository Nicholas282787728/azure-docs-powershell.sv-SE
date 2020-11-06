---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 4c1bc282b4a5aa0bf8c324ec523b5c823ce3cd14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578256"
---
# <span data-ttu-id="adbce-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="adbce-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="adbce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="adbce-102">SYNOPSIS</span></span>
<span data-ttu-id="adbce-103">Startar VMSS eller en uppsättning virtuella datorer i VMSS.</span><span class="sxs-lookup"><span data-stu-id="adbce-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adbce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="adbce-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adbce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="adbce-105">DESCRIPTION</span></span>
<span data-ttu-id="adbce-106">Cmdleten **Start-AzureRmVmss** startar alla virtuella datorer inom den virtuella datorns skal uppsättning (VMSS) eller en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="adbce-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="adbce-107">Du kan använda parametern *InstanceID* för att välja en uppsättning virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="adbce-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="adbce-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="adbce-108">EXAMPLES</span></span>

### <span data-ttu-id="adbce-109">Exempel 1: starta en specifik uppsättning virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="adbce-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="adbce-110">Det här kommandot startar en specifik uppsättning virtuella datorer som anges med den instans-ID-sträng mat ris som tillhör VMSS som heter ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="adbce-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="adbce-111">Exempel 2: starta alla virtuella datorer inom VMSS</span><span class="sxs-lookup"><span data-stu-id="adbce-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="adbce-112">Det här kommandot startar alla virtuella datorer som tillhör VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="adbce-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="adbce-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="adbce-113">PARAMETERS</span></span>

### <span data-ttu-id="adbce-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="adbce-114">-InstanceId</span></span>
<span data-ttu-id="adbce-115">Anger, som en sträng mat ris, ID: t för de instanser som cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="adbce-115">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="adbce-116">Till exempel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="adbce-116">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adbce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adbce-117">-ResourceGroupName</span></span>
<span data-ttu-id="adbce-118">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="adbce-118">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adbce-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="adbce-119">-VMScaleSetName</span></span>
<span data-ttu-id="adbce-120">Anger namnet på den VMSS som den här cmdleten startar för de virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="adbce-120">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adbce-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="adbce-121">-Confirm</span></span>
<span data-ttu-id="adbce-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="adbce-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adbce-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adbce-123">-WhatIf</span></span>
<span data-ttu-id="adbce-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="adbce-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adbce-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="adbce-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adbce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbce-126">CommonParameters</span></span>
<span data-ttu-id="adbce-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adbce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adbce-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adbce-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbce-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="adbce-129">INPUTS</span></span>

### <span data-ttu-id="adbce-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="adbce-130">None</span></span>
<span data-ttu-id="adbce-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="adbce-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="adbce-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="adbce-132">OUTPUTS</span></span>

###  
<span data-ttu-id="adbce-133">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="adbce-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="adbce-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="adbce-134">NOTES</span></span>

## <span data-ttu-id="adbce-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="adbce-135">RELATED LINKS</span></span>

[<span data-ttu-id="adbce-136">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="adbce-136">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="adbce-137">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="adbce-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="adbce-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="adbce-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="adbce-139">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="adbce-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="adbce-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="adbce-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="adbce-141">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="adbce-141">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="adbce-142">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="adbce-142">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


