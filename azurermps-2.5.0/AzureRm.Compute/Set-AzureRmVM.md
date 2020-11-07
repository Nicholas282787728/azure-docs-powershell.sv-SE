---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvm
schema: 2.0.0
ms.openlocfilehash: 030e1dfc05354cded24ac76a379707edd0f07c34
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929070"
---
# <span data-ttu-id="753bf-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="753bf-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="753bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="753bf-102">SYNOPSIS</span></span>
<span data-ttu-id="753bf-103">Markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="753bf-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="753bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="753bf-104">SYNTAX</span></span>

### <span data-ttu-id="753bf-105">GeneralizeResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="753bf-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="753bf-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="753bf-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="753bf-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="753bf-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="753bf-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="753bf-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="753bf-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="753bf-109">DESCRIPTION</span></span>
<span data-ttu-id="753bf-110">Cmdleten **set-AzureRmVM** markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="753bf-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="753bf-111">Innan du kör denna cmdlet loggar du in på den virtuella datorn och använder Sysprep för att förbereda hård disken.</span><span class="sxs-lookup"><span data-stu-id="753bf-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="753bf-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="753bf-112">EXAMPLES</span></span>

### <span data-ttu-id="753bf-113">Exempel 1: Markera en virtuell dator som allmänt</span><span class="sxs-lookup"><span data-stu-id="753bf-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="753bf-114">Det här kommandot anger den virtuella datorn med namnet VirtualMachine07 som allmänt.</span><span class="sxs-lookup"><span data-stu-id="753bf-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="753bf-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="753bf-115">PARAMETERS</span></span>

### <span data-ttu-id="753bf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="753bf-116">-AsJob</span></span>
<span data-ttu-id="753bf-117">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="753bf-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="753bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="753bf-118">-DefaultProfile</span></span>
<span data-ttu-id="753bf-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="753bf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="753bf-120">-Allmänt</span><span class="sxs-lookup"><span data-stu-id="753bf-120">-Generalized</span></span>
<span data-ttu-id="753bf-121">Anger att denna cmdlet markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="753bf-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="753bf-122">-ID</span><span class="sxs-lookup"><span data-stu-id="753bf-122">-Id</span></span>
<span data-ttu-id="753bf-123">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="753bf-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="753bf-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="753bf-124">-Name</span></span>
<span data-ttu-id="753bf-125">Anger namnet på den virtuella dator där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="753bf-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="753bf-126">-Omdistribuera</span><span class="sxs-lookup"><span data-stu-id="753bf-126">-Redeploy</span></span>
<span data-ttu-id="753bf-127">Anger att denna cmdlet manuellt distribuerar den virtuella datorn till en annan Azure-värd för att åtgärda eventuella problem.</span><span class="sxs-lookup"><span data-stu-id="753bf-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="753bf-128">Om du återdistribuerar en virtuell dator startas den om, vilket leder till att tillfälliga data går förlorade.</span><span class="sxs-lookup"><span data-stu-id="753bf-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="753bf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="753bf-129">-ResourceGroupName</span></span>
<span data-ttu-id="753bf-130">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="753bf-130">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="753bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="753bf-131">CommonParameters</span></span>
<span data-ttu-id="753bf-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="753bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="753bf-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="753bf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="753bf-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="753bf-134">INPUTS</span></span>

### <span data-ttu-id="753bf-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="753bf-135">None</span></span>
<span data-ttu-id="753bf-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="753bf-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="753bf-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="753bf-137">OUTPUTS</span></span>

### <span data-ttu-id="753bf-138">Microsoft. Azure. commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="753bf-138">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="753bf-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="753bf-139">NOTES</span></span>

## <span data-ttu-id="753bf-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="753bf-140">RELATED LINKS</span></span>

[<span data-ttu-id="753bf-141">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="753bf-141">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


