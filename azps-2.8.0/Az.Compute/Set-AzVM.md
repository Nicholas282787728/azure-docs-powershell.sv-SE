---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: b3e060680ee5df25708f153b239ec6c13b4e8a35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744960"
---
# <span data-ttu-id="43c40-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="43c40-101">Set-AzVM</span></span>

## <span data-ttu-id="43c40-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43c40-102">SYNOPSIS</span></span>
<span data-ttu-id="43c40-103">Markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="43c40-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="43c40-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43c40-104">SYNTAX</span></span>

### <span data-ttu-id="43c40-105">GeneralizeResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="43c40-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43c40-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="43c40-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43c40-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="43c40-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43c40-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="43c40-108">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43c40-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43c40-109">DESCRIPTION</span></span>
<span data-ttu-id="43c40-110">Cmdleten **set-AzVM** markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="43c40-110">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="43c40-111">Innan du kör denna cmdlet loggar du in på den virtuella datorn och använder Sysprep för att förbereda hård disken.</span><span class="sxs-lookup"><span data-stu-id="43c40-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="43c40-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43c40-112">EXAMPLES</span></span>

### <span data-ttu-id="43c40-113">Exempel 1: Markera en virtuell dator som allmänt</span><span class="sxs-lookup"><span data-stu-id="43c40-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="43c40-114">Det här kommandot anger den virtuella datorn med namnet VirtualMachine07 som allmänt.</span><span class="sxs-lookup"><span data-stu-id="43c40-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="43c40-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43c40-115">PARAMETERS</span></span>

### <span data-ttu-id="43c40-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43c40-116">-AsJob</span></span>
<span data-ttu-id="43c40-117">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="43c40-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="43c40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c40-118">-DefaultProfile</span></span>
<span data-ttu-id="43c40-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43c40-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43c40-120">-Allmänt</span><span class="sxs-lookup"><span data-stu-id="43c40-120">-Generalized</span></span>
<span data-ttu-id="43c40-121">Anger att denna cmdlet markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="43c40-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="43c40-122">-ID</span><span class="sxs-lookup"><span data-stu-id="43c40-122">-Id</span></span>
<span data-ttu-id="43c40-123">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="43c40-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c40-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="43c40-124">-Name</span></span>
<span data-ttu-id="43c40-125">Anger namnet på den virtuella dator där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="43c40-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c40-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="43c40-126">-NoWait</span></span>
<span data-ttu-id="43c40-127">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="43c40-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="43c40-128">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="43c40-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c40-129">-Omdistribuera</span><span class="sxs-lookup"><span data-stu-id="43c40-129">-Redeploy</span></span>
<span data-ttu-id="43c40-130">Anger att denna cmdlet manuellt distribuerar den virtuella datorn till en annan Azure-värd för att åtgärda eventuella problem.</span><span class="sxs-lookup"><span data-stu-id="43c40-130">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="43c40-131">Om du återdistribuerar en virtuell dator startas den om, vilket leder till att tillfälliga data går förlorade.</span><span class="sxs-lookup"><span data-stu-id="43c40-131">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="43c40-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43c40-132">-ResourceGroupName</span></span>
<span data-ttu-id="43c40-133">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="43c40-133">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c40-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c40-134">CommonParameters</span></span>
<span data-ttu-id="43c40-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c40-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c40-136">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43c40-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c40-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43c40-137">INPUTS</span></span>

### <span data-ttu-id="43c40-138">System. String</span><span class="sxs-lookup"><span data-stu-id="43c40-138">System.String</span></span>

## <span data-ttu-id="43c40-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43c40-139">OUTPUTS</span></span>

### <span data-ttu-id="43c40-140">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="43c40-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="43c40-141">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="43c40-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="43c40-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43c40-142">NOTES</span></span>

## <span data-ttu-id="43c40-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43c40-143">RELATED LINKS</span></span>

[<span data-ttu-id="43c40-144">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="43c40-144">Get-AzVM</span></span>](./Get-AzVM.md)


