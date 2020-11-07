---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: 61bd867f7790f47599ac10ebd6523327e4e1868a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754492"
---
# <span data-ttu-id="9f232-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f232-101">Restart-AzVmss</span></span>

## <span data-ttu-id="9f232-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f232-102">SYNOPSIS</span></span>
<span data-ttu-id="9f232-103">Startar om VMSS eller en virtuell dator i VMSS.</span><span class="sxs-lookup"><span data-stu-id="9f232-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="9f232-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f232-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f232-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f232-105">DESCRIPTION</span></span>
<span data-ttu-id="9f232-106">Cmdleten **restart-AzVmss** startar om den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9f232-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="9f232-107">Denna cmdlet kan också användas för att starta om en specifik virtuell dator i VMSS med hjälp av *InstanceID* -parametern.</span><span class="sxs-lookup"><span data-stu-id="9f232-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="9f232-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f232-108">EXAMPLES</span></span>

### <span data-ttu-id="9f232-109">Exempel 1: starta om VMSS</span><span class="sxs-lookup"><span data-stu-id="9f232-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="9f232-110">Det här kommandot startar om VMSS med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="9f232-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="9f232-111">Exempel 2: starta om en specifik virtuell dator inom VMSS</span><span class="sxs-lookup"><span data-stu-id="9f232-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="9f232-112">Det här kommandot startar om en virtuell dator som har instans-ID 1 i VMSS med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="9f232-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="9f232-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f232-113">PARAMETERS</span></span>

### <span data-ttu-id="9f232-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f232-114">-AsJob</span></span>
<span data-ttu-id="9f232-115">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="9f232-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9f232-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f232-116">-DefaultProfile</span></span>
<span data-ttu-id="9f232-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f232-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f232-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="9f232-118">-InstanceId</span></span>
<span data-ttu-id="9f232-119">Anger ID för de instanser som behöver startas om.</span><span class="sxs-lookup"><span data-stu-id="9f232-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f232-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f232-120">-ResourceGroupName</span></span>
<span data-ttu-id="9f232-121">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="9f232-121">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f232-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9f232-122">-VMScaleSetName</span></span>
<span data-ttu-id="9f232-123">Arter namnet på den VMSS som denna cmdlet startar om.</span><span class="sxs-lookup"><span data-stu-id="9f232-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f232-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9f232-124">-Confirm</span></span>
<span data-ttu-id="9f232-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9f232-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f232-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f232-126">-WhatIf</span></span>
<span data-ttu-id="9f232-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9f232-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f232-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9f232-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f232-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f232-129">CommonParameters</span></span>
<span data-ttu-id="9f232-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f232-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f232-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f232-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f232-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f232-132">INPUTS</span></span>

### <span data-ttu-id="9f232-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9f232-133">System.String</span></span>

### <span data-ttu-id="9f232-134">System. string []</span><span class="sxs-lookup"><span data-stu-id="9f232-134">System.String[]</span></span>

## <span data-ttu-id="9f232-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f232-135">OUTPUTS</span></span>

### <span data-ttu-id="9f232-136">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9f232-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9f232-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f232-137">NOTES</span></span>

## <span data-ttu-id="9f232-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f232-138">RELATED LINKS</span></span>

[<span data-ttu-id="9f232-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f232-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="9f232-140">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f232-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="9f232-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f232-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="9f232-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f232-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="9f232-143">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f232-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="9f232-144">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f232-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="9f232-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9f232-145">Update-AzVmss</span></span>](./Update-AzVmss.md)

