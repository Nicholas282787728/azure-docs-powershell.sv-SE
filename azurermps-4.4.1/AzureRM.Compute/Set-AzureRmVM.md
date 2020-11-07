---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
ms.openlocfilehash: 6fa67a039599ab066b82ad923f5a2f896b0db519
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757308"
---
# <span data-ttu-id="1b9b7-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1b9b7-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="1b9b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b9b7-102">SYNOPSIS</span></span>
<span data-ttu-id="1b9b7-103">Markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b9b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b9b7-104">SYNTAX</span></span>

### <span data-ttu-id="1b9b7-105">GeneralizeResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="1b9b7-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b9b7-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1b9b7-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b9b7-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1b9b7-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b9b7-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1b9b7-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b9b7-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b9b7-109">DESCRIPTION</span></span>
<span data-ttu-id="1b9b7-110">Cmdleten **set-AzureRmVM** markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="1b9b7-111">Innan du kör denna cmdlet loggar du in på den virtuella datorn och använder Sysprep för att förbereda hård disken.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="1b9b7-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b9b7-112">EXAMPLES</span></span>

### <span data-ttu-id="1b9b7-113">Exempel 1: Markera en virtuell dator som allmänt</span><span class="sxs-lookup"><span data-stu-id="1b9b7-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="1b9b7-114">Det här kommandot anger den virtuella datorn med namnet VirtualMachine07 som allmänt.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="1b9b7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b9b7-115">PARAMETERS</span></span>

### <span data-ttu-id="1b9b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b9b7-116">-DefaultProfile</span></span>
<span data-ttu-id="1b9b7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b9b7-118">-Allmänt</span><span class="sxs-lookup"><span data-stu-id="1b9b7-118">-Generalized</span></span>
<span data-ttu-id="1b9b7-119">Anger att denna cmdlet markerar en virtuell dator som allmänt.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-119">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b9b7-120">-ID</span><span class="sxs-lookup"><span data-stu-id="1b9b7-120">-Id</span></span>
<span data-ttu-id="1b9b7-121">Anger den virtuella datorns resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-121">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="1b9b7-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b9b7-122">-Name</span></span>
<span data-ttu-id="1b9b7-123">Anger namnet på den virtuella dator där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-123">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1b9b7-124">-Omdistribuera</span><span class="sxs-lookup"><span data-stu-id="1b9b7-124">-Redeploy</span></span>
<span data-ttu-id="1b9b7-125">Anger att denna cmdlet manuellt distribuerar den virtuella datorn till en annan Azure-värd för att åtgärda eventuella problem.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-125">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="1b9b7-126">Om du återdistribuerar en virtuell dator startas den om, vilket leder till att tillfälliga data går förlorade.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-126">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b9b7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b9b7-127">-ResourceGroupName</span></span>
<span data-ttu-id="1b9b7-128">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-128">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1b9b7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b9b7-129">CommonParameters</span></span>
<span data-ttu-id="1b9b7-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b9b7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b9b7-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b9b7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b9b7-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b9b7-132">INPUTS</span></span>

## <span data-ttu-id="1b9b7-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b9b7-133">OUTPUTS</span></span>

## <span data-ttu-id="1b9b7-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b9b7-134">NOTES</span></span>

## <span data-ttu-id="1b9b7-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b9b7-135">RELATED LINKS</span></span>

[<span data-ttu-id="1b9b7-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1b9b7-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


