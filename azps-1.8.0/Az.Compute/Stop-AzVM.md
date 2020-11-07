---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 393f2a75217b95b6c1c5366326735ac0f78ac294
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917201"
---
# <span data-ttu-id="2d9f6-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d9f6-101">Stop-AzVM</span></span>

## <span data-ttu-id="2d9f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d9f6-102">SYNOPSIS</span></span>
<span data-ttu-id="2d9f6-103">Stoppar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="2d9f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d9f6-104">SYNTAX</span></span>

### <span data-ttu-id="2d9f6-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="2d9f6-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d9f6-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2d9f6-106">IdParameterSetName</span></span>
```
Stop-AzVM [[-Name] <String>] [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d9f6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d9f6-107">DESCRIPTION</span></span>
<span data-ttu-id="2d9f6-108">Cmdleten **Stop-AzVM** stoppar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="2d9f6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d9f6-109">EXAMPLES</span></span>

### <span data-ttu-id="2d9f6-110">Exempel 1: stoppa en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="2d9f6-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="2d9f6-111">Det här kommandot stoppar den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="2d9f6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d9f6-112">PARAMETERS</span></span>

### <span data-ttu-id="2d9f6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d9f6-113">-AsJob</span></span>
<span data-ttu-id="2d9f6-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2d9f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d9f6-115">-DefaultProfile</span></span>
<span data-ttu-id="2d9f6-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d9f6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2d9f6-117">-Force</span></span>
<span data-ttu-id="2d9f6-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d9f6-119">-ID</span><span class="sxs-lookup"><span data-stu-id="2d9f6-119">-Id</span></span>
<span data-ttu-id="2d9f6-120">ID för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9f6-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="2d9f6-121">-Name</span></span>
<span data-ttu-id="2d9f6-122">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9f6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d9f6-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d9f6-124">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9f6-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="2d9f6-125">-StayProvisioned</span></span>
<span data-ttu-id="2d9f6-126">Cmdleten stoppar alla virtuella datorer i VMSS, men avdelar dem inte.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="2d9f6-127">Kontot debiteras för de stoppade virtuella datorerna.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="2d9f6-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2d9f6-128">-Confirm</span></span>
<span data-ttu-id="2d9f6-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d9f6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d9f6-130">-WhatIf</span></span>
<span data-ttu-id="2d9f6-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d9f6-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d9f6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d9f6-133">CommonParameters</span></span>
<span data-ttu-id="2d9f6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d9f6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d9f6-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d9f6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d9f6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d9f6-136">INPUTS</span></span>

### <span data-ttu-id="2d9f6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2d9f6-137">System.String</span></span>

## <span data-ttu-id="2d9f6-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d9f6-138">OUTPUTS</span></span>

### <span data-ttu-id="2d9f6-139">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="2d9f6-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="2d9f6-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d9f6-140">NOTES</span></span>

## <span data-ttu-id="2d9f6-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d9f6-141">RELATED LINKS</span></span>

[<span data-ttu-id="2d9f6-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d9f6-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2d9f6-143">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d9f6-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="2d9f6-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d9f6-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="2d9f6-145">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d9f6-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="2d9f6-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d9f6-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="2d9f6-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d9f6-147">Update-AzVM</span></span>](./Update-AzVM.md)


