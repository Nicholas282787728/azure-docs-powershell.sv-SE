---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 08fa41232a6f473b371c0e44e22b21712f61f1b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744905"
---
# <span data-ttu-id="f248a-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="f248a-101">Start-AzVM</span></span>

## <span data-ttu-id="f248a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f248a-102">SYNOPSIS</span></span>
<span data-ttu-id="f248a-103">Startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="f248a-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="f248a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f248a-104">SYNTAX</span></span>

### <span data-ttu-id="f248a-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="f248a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f248a-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f248a-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f248a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f248a-107">DESCRIPTION</span></span>
<span data-ttu-id="f248a-108">Cmdleten **Start-AzVM** startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="f248a-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="f248a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f248a-109">EXAMPLES</span></span>

### <span data-ttu-id="f248a-110">Exempel 1: starta en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="f248a-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="f248a-111">Det här kommandot startar den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f248a-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="f248a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f248a-112">PARAMETERS</span></span>

### <span data-ttu-id="f248a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f248a-113">-AsJob</span></span>
<span data-ttu-id="f248a-114">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="f248a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f248a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f248a-115">-DefaultProfile</span></span>
<span data-ttu-id="f248a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f248a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f248a-117">-ID</span><span class="sxs-lookup"><span data-stu-id="f248a-117">-Id</span></span>
<span data-ttu-id="f248a-118">ID för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="f248a-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="f248a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="f248a-119">-Name</span></span>
<span data-ttu-id="f248a-120">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="f248a-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="f248a-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f248a-121">-NoWait</span></span>
<span data-ttu-id="f248a-122">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="f248a-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f248a-123">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="f248a-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f248a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f248a-124">-ResourceGroupName</span></span>
<span data-ttu-id="f248a-125">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f248a-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f248a-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f248a-126">-Confirm</span></span>
<span data-ttu-id="f248a-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f248a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f248a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f248a-128">-WhatIf</span></span>
<span data-ttu-id="f248a-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f248a-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f248a-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f248a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f248a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f248a-131">CommonParameters</span></span>
<span data-ttu-id="f248a-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f248a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f248a-133">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f248a-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f248a-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f248a-134">INPUTS</span></span>

### <span data-ttu-id="f248a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f248a-135">System.String</span></span>

## <span data-ttu-id="f248a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f248a-136">OUTPUTS</span></span>

### <span data-ttu-id="f248a-137">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="f248a-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="f248a-138">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f248a-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f248a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f248a-139">NOTES</span></span>

## <span data-ttu-id="f248a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f248a-140">RELATED LINKS</span></span>

[<span data-ttu-id="f248a-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f248a-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f248a-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f248a-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="f248a-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="f248a-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="f248a-144">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="f248a-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="f248a-145">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="f248a-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="f248a-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f248a-146">Update-AzVM</span></span>](./Update-AzVM.md)


