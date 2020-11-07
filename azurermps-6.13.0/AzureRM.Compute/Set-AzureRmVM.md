---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVM.md
ms.openlocfilehash: 18fd719662fbbe46276927fb05fbff021d8bcb96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757905"
---
# <span data-ttu-id="34075-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="34075-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="34075-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34075-102">SYNOPSIS</span></span>
<span data-ttu-id="34075-103">Markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="34075-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34075-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34075-104">SYNTAX</span></span>

### <span data-ttu-id="34075-105">GeneralizeResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="34075-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34075-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="34075-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34075-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="34075-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34075-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="34075-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34075-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34075-109">DESCRIPTION</span></span>
<span data-ttu-id="34075-110">Cmdleten **set-AzureRmVM** markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="34075-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="34075-111">Innan du kör denna cmdlet loggar du in på den virtuella datorn och använder Sysprep för att förbereda hård disken.</span><span class="sxs-lookup"><span data-stu-id="34075-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="34075-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34075-112">EXAMPLES</span></span>

### <span data-ttu-id="34075-113">Exempel 1: Markera en virtuell dator som allmänt</span><span class="sxs-lookup"><span data-stu-id="34075-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="34075-114">Det här kommandot anger den virtuella datorn med namnet VirtualMachine07 som allmänt.</span><span class="sxs-lookup"><span data-stu-id="34075-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="34075-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34075-115">PARAMETERS</span></span>

### <span data-ttu-id="34075-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34075-116">-AsJob</span></span>
<span data-ttu-id="34075-117">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="34075-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="34075-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34075-118">-DefaultProfile</span></span>
<span data-ttu-id="34075-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34075-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34075-120">-Allmänt</span><span class="sxs-lookup"><span data-stu-id="34075-120">-Generalized</span></span>
<span data-ttu-id="34075-121">Anger att denna cmdlet markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="34075-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="34075-122">-ID</span><span class="sxs-lookup"><span data-stu-id="34075-122">-Id</span></span>
<span data-ttu-id="34075-123">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="34075-123">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="34075-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="34075-124">-Name</span></span>
<span data-ttu-id="34075-125">Anger namnet på den virtuella dator där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="34075-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="34075-126">-Omdistribuera</span><span class="sxs-lookup"><span data-stu-id="34075-126">-Redeploy</span></span>
<span data-ttu-id="34075-127">Anger att denna cmdlet manuellt distribuerar den virtuella datorn till en annan Azure-värd för att åtgärda eventuella problem.</span><span class="sxs-lookup"><span data-stu-id="34075-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="34075-128">Om du återdistribuerar en virtuell dator startas den om, vilket leder till att tillfälliga data går förlorade.</span><span class="sxs-lookup"><span data-stu-id="34075-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="34075-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34075-129">-ResourceGroupName</span></span>
<span data-ttu-id="34075-130">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="34075-130">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="34075-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34075-131">CommonParameters</span></span>
<span data-ttu-id="34075-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34075-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34075-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34075-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34075-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34075-134">INPUTS</span></span>

### <span data-ttu-id="34075-135">System. String</span><span class="sxs-lookup"><span data-stu-id="34075-135">System.String</span></span>

## <span data-ttu-id="34075-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34075-136">OUTPUTS</span></span>

### <span data-ttu-id="34075-137">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="34075-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="34075-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34075-138">NOTES</span></span>

## <span data-ttu-id="34075-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34075-139">RELATED LINKS</span></span>

[<span data-ttu-id="34075-140">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="34075-140">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


