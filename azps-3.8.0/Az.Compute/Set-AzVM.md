---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: c9b7ce0c55ff917839ff8047454dcced42653b3d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088645"
---
# <span data-ttu-id="beece-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="beece-101">Set-AzVM</span></span>

## <span data-ttu-id="beece-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="beece-102">SYNOPSIS</span></span>
<span data-ttu-id="beece-103">Markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="beece-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="beece-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="beece-104">SYNTAX</span></span>

### <span data-ttu-id="beece-105">GeneralizeResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="beece-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="beece-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="beece-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="beece-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="beece-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="beece-108">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="beece-108">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="beece-109">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="beece-109">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="beece-110">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="beece-110">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="beece-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="beece-111">DESCRIPTION</span></span>
<span data-ttu-id="beece-112">Cmdleten **set-AzVM** markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="beece-112">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="beece-113">Innan du kör denna cmdlet loggar du in på den virtuella datorn och använder Sysprep för att förbereda hård disken.</span><span class="sxs-lookup"><span data-stu-id="beece-113">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="beece-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="beece-114">EXAMPLES</span></span>

### <span data-ttu-id="beece-115">Exempel 1: Markera en virtuell dator som allmänt</span><span class="sxs-lookup"><span data-stu-id="beece-115">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="beece-116">Det här kommandot anger den virtuella datorn med namnet VirtualMachine07 som allmänt.</span><span class="sxs-lookup"><span data-stu-id="beece-116">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="beece-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="beece-117">PARAMETERS</span></span>

### <span data-ttu-id="beece-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="beece-118">-AsJob</span></span>
<span data-ttu-id="beece-119">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="beece-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="beece-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beece-120">-DefaultProfile</span></span>
<span data-ttu-id="beece-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="beece-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="beece-122">-Allmänt</span><span class="sxs-lookup"><span data-stu-id="beece-122">-Generalized</span></span>
<span data-ttu-id="beece-123">Anger att denna cmdlet markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="beece-123">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beece-124">-ID</span><span class="sxs-lookup"><span data-stu-id="beece-124">-Id</span></span>
<span data-ttu-id="beece-125">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="beece-125">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beece-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="beece-126">-Name</span></span>
<span data-ttu-id="beece-127">Anger namnet på den virtuella dator där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="beece-127">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beece-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="beece-128">-NoWait</span></span>
<span data-ttu-id="beece-129">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="beece-129">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="beece-130">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="beece-130">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beece-131">-Omkoppla</span><span class="sxs-lookup"><span data-stu-id="beece-131">-Reapply</span></span>
<span data-ttu-id="beece-132">Om du vill återanvända en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="beece-132">To reapply virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReapplyResourceGroupNameParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beece-133">-Omdistribuera</span><span class="sxs-lookup"><span data-stu-id="beece-133">-Redeploy</span></span>
<span data-ttu-id="beece-134">Anger att denna cmdlet manuellt distribuerar den virtuella datorn till en annan Azure-värd för att åtgärda eventuella problem.</span><span class="sxs-lookup"><span data-stu-id="beece-134">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="beece-135">Om du återdistribuerar en virtuell dator startas den om, vilket leder till att tillfälliga data går förlorade.</span><span class="sxs-lookup"><span data-stu-id="beece-135">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beece-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beece-136">-ResourceGroupName</span></span>
<span data-ttu-id="beece-137">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="beece-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beece-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beece-138">CommonParameters</span></span>
<span data-ttu-id="beece-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beece-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beece-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="beece-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beece-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="beece-141">INPUTS</span></span>

### <span data-ttu-id="beece-142">System. String</span><span class="sxs-lookup"><span data-stu-id="beece-142">System.String</span></span>

## <span data-ttu-id="beece-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="beece-143">OUTPUTS</span></span>

### <span data-ttu-id="beece-144">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="beece-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="beece-145">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="beece-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="beece-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="beece-146">NOTES</span></span>

## <span data-ttu-id="beece-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="beece-147">RELATED LINKS</span></span>

[<span data-ttu-id="beece-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="beece-148">Get-AzVM</span></span>](./Get-AzVM.md)


