---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260814"
---
# <span data-ttu-id="2b59f-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="2b59f-101">Set-AzVM</span></span>

## <span data-ttu-id="2b59f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b59f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b59f-103">Markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="2b59f-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="2b59f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b59f-104">SYNTAX</span></span>

### <span data-ttu-id="2b59f-105">GeneralizeResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="2b59f-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b59f-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2b59f-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b59f-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2b59f-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b59f-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2b59f-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b59f-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2b59f-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b59f-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2b59f-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b59f-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2b59f-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b59f-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2b59f-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b59f-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b59f-113">DESCRIPTION</span></span>
<span data-ttu-id="2b59f-114">Cmdleten **set-AzVM** markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="2b59f-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="2b59f-115">Innan du kör denna cmdlet loggar du in på den virtuella datorn och använder Sysprep för att förbereda hård disken.</span><span class="sxs-lookup"><span data-stu-id="2b59f-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="2b59f-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b59f-116">EXAMPLES</span></span>

### <span data-ttu-id="2b59f-117">Exempel 1: Markera en virtuell dator som allmänt</span><span class="sxs-lookup"><span data-stu-id="2b59f-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="2b59f-118">Det här kommandot anger den virtuella datorn med namnet VirtualMachine07 som allmänt.</span><span class="sxs-lookup"><span data-stu-id="2b59f-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="2b59f-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b59f-119">PARAMETERS</span></span>

### <span data-ttu-id="2b59f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b59f-120">-AsJob</span></span>
<span data-ttu-id="2b59f-121">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="2b59f-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2b59f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b59f-122">-DefaultProfile</span></span>
<span data-ttu-id="2b59f-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2b59f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b59f-124">-Allmänt</span><span class="sxs-lookup"><span data-stu-id="2b59f-124">-Generalized</span></span>
<span data-ttu-id="2b59f-125">Anger att denna cmdlet markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="2b59f-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="2b59f-126">-ID</span><span class="sxs-lookup"><span data-stu-id="2b59f-126">-Id</span></span>
<span data-ttu-id="2b59f-127">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2b59f-127">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b59f-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="2b59f-128">-Name</span></span>
<span data-ttu-id="2b59f-129">Anger namnet på den virtuella dator där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2b59f-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b59f-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2b59f-130">-NoWait</span></span>
<span data-ttu-id="2b59f-131">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="2b59f-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2b59f-132">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="2b59f-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2b59f-133">-Omkoppla</span><span class="sxs-lookup"><span data-stu-id="2b59f-133">-Reapply</span></span>
<span data-ttu-id="2b59f-134">Om du vill återanvända en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2b59f-134">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="2b59f-135">-Omdistribuera</span><span class="sxs-lookup"><span data-stu-id="2b59f-135">-Redeploy</span></span>
<span data-ttu-id="2b59f-136">Anger att denna cmdlet manuellt distribuerar den virtuella datorn till en annan Azure-värd för att åtgärda eventuella problem.</span><span class="sxs-lookup"><span data-stu-id="2b59f-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="2b59f-137">Om du återdistribuerar en virtuell dator startas den om, vilket leder till att tillfälliga data går förlorade.</span><span class="sxs-lookup"><span data-stu-id="2b59f-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="2b59f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b59f-138">-ResourceGroupName</span></span>
<span data-ttu-id="2b59f-139">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2b59f-139">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b59f-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="2b59f-140">-SimulateEviction</span></span>
<span data-ttu-id="2b59f-141">Anger att denna cmdlet simulerar avlägsnande av en virtuell dator i datorn.</span><span class="sxs-lookup"><span data-stu-id="2b59f-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="2b59f-142">Avlägsnandet sker inom 30 minuter från API-anropet.</span><span class="sxs-lookup"><span data-stu-id="2b59f-142">The eviction will occur within 30 minutes of calling the API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimulateEvictionResourceGroupNameParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b59f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b59f-143">CommonParameters</span></span>
<span data-ttu-id="2b59f-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b59f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b59f-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b59f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b59f-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b59f-146">INPUTS</span></span>

### <span data-ttu-id="2b59f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2b59f-147">System.String</span></span>

## <span data-ttu-id="2b59f-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b59f-148">OUTPUTS</span></span>

### <span data-ttu-id="2b59f-149">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="2b59f-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="2b59f-150">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2b59f-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2b59f-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b59f-151">NOTES</span></span>

## <span data-ttu-id="2b59f-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b59f-152">RELATED LINKS</span></span>

[<span data-ttu-id="2b59f-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2b59f-153">Get-AzVM</span></span>](./Get-AzVM.md)


