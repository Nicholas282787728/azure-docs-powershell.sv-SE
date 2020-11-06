---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: ff337ae0f5d0da86b035905bf83d2719edf1f4f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573539"
---
# <span data-ttu-id="c5ad0-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c5ad0-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="c5ad0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ad0-103">Skapar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5ad0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5ad0-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <ContainerService> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5ad0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5ad0-105">DESCRIPTION</span></span>
<span data-ttu-id="c5ad0-106">Cmdleten **New-AzureRmContainerService** skapar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="c5ad0-107">Ange ett behållar tjänst objekt som du kan skapa med hjälp av New-AzureRmContainerServiceConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="c5ad0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5ad0-108">EXAMPLES</span></span>

### <span data-ttu-id="c5ad0-109">Exempel 1: skapa en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="c5ad0-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="c5ad0-110">Det första kommandot skapar en resurs grupp med namnet ResourceGroup17 på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="c5ad0-111">Mer information finns i New-AzureRmResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="c5ad0-112">Det andra kommandot skapar en container och lagrar sedan den i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="c5ad0-113">Mer information finns i New-AzureRmContainerServiceConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="c5ad0-114">Med kommandot slut skapas en behållar tjänst för behållaren som lagras i $Container.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="c5ad0-115">Tjänsten heter csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="c5ad0-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5ad0-116">PARAMETERS</span></span>

### <span data-ttu-id="c5ad0-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="c5ad0-117">-ContainerService</span></span>
<span data-ttu-id="c5ad0-118">Anger ett Container Service-objekt som innehåller egenskaperna för den nya tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-118">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="c5ad0-119">För att hämta ett **ContainerService** -objekt, Använd cmdleten New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-119">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad0-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c5ad0-120">-Name</span></span>
<span data-ttu-id="c5ad0-121">Anger namnet på den behållar tjänst som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-121">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5ad0-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5ad0-123">Anger den resurs grupp i vilken denna cmdlet distribuerar behållar tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-123">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="c5ad0-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c5ad0-124">-Confirm</span></span>
<span data-ttu-id="c5ad0-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5ad0-126">-WhatIf</span></span>
<span data-ttu-id="c5ad0-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-127">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c5ad0-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ad0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ad0-129">CommonParameters</span></span>
<span data-ttu-id="c5ad0-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ad0-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5ad0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ad0-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5ad0-132">INPUTS</span></span>

### <span data-ttu-id="c5ad0-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="c5ad0-133">None</span></span>
<span data-ttu-id="c5ad0-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c5ad0-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c5ad0-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5ad0-135">OUTPUTS</span></span>

## <span data-ttu-id="c5ad0-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5ad0-136">NOTES</span></span>

## <span data-ttu-id="c5ad0-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5ad0-137">RELATED LINKS</span></span>

[<span data-ttu-id="c5ad0-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c5ad0-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="c5ad0-139">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="c5ad0-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="c5ad0-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c5ad0-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="c5ad0-141">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c5ad0-141">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


