---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: b32734bbca2ec0fd554a073b2e0b5acf077874ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573696"
---
# <span data-ttu-id="d0e6c-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="d0e6c-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="d0e6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e6c-103">Tar bort en datadisk från VMSS.</span><span class="sxs-lookup"><span data-stu-id="d0e6c-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0e6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0e6c-104">SYNTAX</span></span>

### <span data-ttu-id="d0e6c-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0e6c-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0e6c-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0e6c-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0e6c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0e6c-107">DESCRIPTION</span></span>
<span data-ttu-id="d0e6c-108">Cmdleten **Remove-AzureRmVmssDataDisk** tar bort en datadisk från den virtuella datorns Scale set-instans (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d0e6c-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="d0e6c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0e6c-109">EXAMPLES</span></span>

### <span data-ttu-id="d0e6c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d0e6c-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="d0e6c-111">Det här kommandot tar bort data disken ' DataDisk1 ' från VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="d0e6c-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="d0e6c-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d0e6c-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="d0e6c-113">Det här kommandot tar bort data disken för LUN 0 från VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="d0e6c-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="d0e6c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0e6c-114">PARAMETERS</span></span>

### <span data-ttu-id="d0e6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e6c-115">-DefaultProfile</span></span>
<span data-ttu-id="d0e6c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0e6c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0e6c-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="d0e6c-117">-Lun</span></span>
<span data-ttu-id="d0e6c-118">Anger diskens logiska enhets nummer.</span><span class="sxs-lookup"><span data-stu-id="d0e6c-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e6c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0e6c-119">-Name</span></span>
<span data-ttu-id="d0e6c-120">Anger namnet på disken.</span><span class="sxs-lookup"><span data-stu-id="d0e6c-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="d0e6c-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d0e6c-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d0e6c-122">Ange VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="d0e6c-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="d0e6c-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0e6c-123">-Confirm</span></span>
<span data-ttu-id="d0e6c-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0e6c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0e6c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0e6c-125">-WhatIf</span></span>
<span data-ttu-id="d0e6c-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0e6c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0e6c-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0e6c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0e6c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e6c-128">CommonParameters</span></span>
<span data-ttu-id="d0e6c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e6c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e6c-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0e6c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e6c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0e6c-131">INPUTS</span></span>

### <span data-ttu-id="d0e6c-132">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d0e6c-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="d0e6c-133">System. String-system. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d0e6c-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d0e6c-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0e6c-134">OUTPUTS</span></span>

### <span data-ttu-id="d0e6c-135">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d0e6c-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="d0e6c-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0e6c-136">NOTES</span></span>

## <span data-ttu-id="d0e6c-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0e6c-137">RELATED LINKS</span></span>

