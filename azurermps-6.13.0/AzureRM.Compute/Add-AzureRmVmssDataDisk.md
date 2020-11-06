---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: 0ef680f60f48451e5d5dd9bff730cbfe4ebc9aae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578928"
---
# <span data-ttu-id="de958-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="de958-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="de958-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de958-102">SYNOPSIS</span></span>
<span data-ttu-id="de958-103">Lägger till en datadisk till VMSS.</span><span class="sxs-lookup"><span data-stu-id="de958-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de958-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de958-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de958-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de958-105">DESCRIPTION</span></span>
<span data-ttu-id="de958-106">Cmdleten **Add-AzureRmVmssDataDisk** lägger till en datadisk till instansen för virtuell dator Scale set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="de958-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="de958-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de958-107">EXAMPLES</span></span>

### <span data-ttu-id="de958-108">Exempel 1: lägga till en data disk</span><span class="sxs-lookup"><span data-stu-id="de958-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="de958-109">Det här kommandot lägger till en tom datadisk till VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="de958-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="de958-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de958-110">PARAMETERS</span></span>

### <span data-ttu-id="de958-111">-Cachning</span><span class="sxs-lookup"><span data-stu-id="de958-111">-Caching</span></span>
<span data-ttu-id="de958-112">Anger diskens cachelagringsalternativ.</span><span class="sxs-lookup"><span data-stu-id="de958-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de958-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="de958-113">-CreateOption</span></span>
<span data-ttu-id="de958-114">Anger diskens skapande alternativ.</span><span class="sxs-lookup"><span data-stu-id="de958-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="de958-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de958-115">-DefaultProfile</span></span>
<span data-ttu-id="de958-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de958-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de958-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="de958-117">-DiskSizeGB</span></span>
<span data-ttu-id="de958-118">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="de958-118">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de958-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="de958-119">-Lun</span></span>
<span data-ttu-id="de958-120">Anger diskens logiska enhets nummer.</span><span class="sxs-lookup"><span data-stu-id="de958-120">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de958-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="de958-121">-Name</span></span>
<span data-ttu-id="de958-122">Anger namnet på disken.</span><span class="sxs-lookup"><span data-stu-id="de958-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="de958-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="de958-123">-StorageAccountType</span></span>
<span data-ttu-id="de958-124">Anger diskens lagrings kontotyp.</span><span class="sxs-lookup"><span data-stu-id="de958-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="de958-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="de958-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="de958-126">Ange VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="de958-126">Specify the VMSS object.</span></span>
<span data-ttu-id="de958-127">Du kan använda cmdleten [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="de958-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="de958-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="de958-128">-WriteAccelerator</span></span>
<span data-ttu-id="de958-129">Anger om WriteAccelerator ska aktive ras eller inaktive ras på data disken.</span><span class="sxs-lookup"><span data-stu-id="de958-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="de958-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de958-130">-Confirm</span></span>
<span data-ttu-id="de958-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de958-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de958-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de958-132">-WhatIf</span></span>
<span data-ttu-id="de958-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de958-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de958-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de958-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de958-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de958-135">CommonParameters</span></span>
<span data-ttu-id="de958-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de958-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de958-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de958-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de958-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de958-138">INPUTS</span></span>

### <span data-ttu-id="de958-139">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="de958-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="de958-140">System. String</span><span class="sxs-lookup"><span data-stu-id="de958-140">System.String</span></span>

### <span data-ttu-id="de958-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="de958-141">System.Int32</span></span>

### <span data-ttu-id="de958-142">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, version = 21.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="de958-142">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="de958-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de958-143">OUTPUTS</span></span>

### <span data-ttu-id="de958-144">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="de958-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="de958-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de958-145">NOTES</span></span>

## <span data-ttu-id="de958-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de958-146">RELATED LINKS</span></span>
