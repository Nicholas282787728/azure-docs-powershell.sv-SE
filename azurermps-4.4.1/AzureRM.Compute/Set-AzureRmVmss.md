---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: efb24aa4f8770e1911b9bf85a1fbf4dd366ea34d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573660"
---
# <span data-ttu-id="e9f2d-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9f2d-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="e9f2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f2d-103">Ställer in specifika åtgärder på ett angivet VMSS.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9f2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9f2d-104">SYNTAX</span></span>

### <span data-ttu-id="e9f2d-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="e9f2d-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9f2d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="e9f2d-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9f2d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9f2d-107">DESCRIPTION</span></span>
<span data-ttu-id="e9f2d-108">Cmdleten **set-AzureRmVmss** anger specifika åtgärder på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e9f2d-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e9f2d-109">Den enda åtgärden som stöds av denna cmdlet är att återanvända.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="e9f2d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9f2d-110">EXAMPLES</span></span>

### <span data-ttu-id="e9f2d-111">Exempel 1: ombilda en VMSS</span><span class="sxs-lookup"><span data-stu-id="e9f2d-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="e9f2d-112">Det här kommandot återbildar VMSS med namnet ContosoVMSS som tillhör resurs gruppen med namnet ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="e9f2d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9f2d-113">PARAMETERS</span></span>

### <span data-ttu-id="e9f2d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f2d-114">-DefaultProfile</span></span>
<span data-ttu-id="e9f2d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9f2d-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e9f2d-116">-InstanceId</span></span>
<span data-ttu-id="e9f2d-117">Instans-ID för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-117">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f2d-118">-Ombild</span><span class="sxs-lookup"><span data-stu-id="e9f2d-118">-Reimage</span></span>
<span data-ttu-id="e9f2d-119">Anger att cmdleten återska VMSS.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-119">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f2d-120">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="e9f2d-120">-ReimageAll</span></span>
<span data-ttu-id="e9f2d-121">Anger att cmdleten återavbildningar alla diskar i VMSS.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-121">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="e9f2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="e9f2d-123">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-123">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f2d-124">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e9f2d-124">-VMScaleSetName</span></span>
<span data-ttu-id="e9f2d-125">Arter namnet på den VMSS som cmdleten ställer in åtgärder för.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-125">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f2d-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e9f2d-126">-Confirm</span></span>
<span data-ttu-id="e9f2d-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9f2d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9f2d-128">-WhatIf</span></span>
<span data-ttu-id="e9f2d-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9f2d-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9f2d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f2d-131">CommonParameters</span></span>
<span data-ttu-id="e9f2d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f2d-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9f2d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f2d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9f2d-134">INPUTS</span></span>

## <span data-ttu-id="e9f2d-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9f2d-135">OUTPUTS</span></span>

### <span data-ttu-id="e9f2d-136">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e9f2d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9f2d-137">NOTES</span></span>

## <span data-ttu-id="e9f2d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9f2d-138">RELATED LINKS</span></span>

[<span data-ttu-id="e9f2d-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9f2d-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="e9f2d-140">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9f2d-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="e9f2d-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9f2d-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="e9f2d-142">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9f2d-142">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="e9f2d-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9f2d-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="e9f2d-144">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9f2d-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="e9f2d-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9f2d-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


