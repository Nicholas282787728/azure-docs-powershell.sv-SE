---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: b8f453200f2365272461373214ec92580212c4b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925093"
---
# <span data-ttu-id="a2c13-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a2c13-101">New-AzContainerService</span></span>

## <span data-ttu-id="a2c13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2c13-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c13-103">Skapar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="a2c13-103">Creates a container service.</span></span>

## <span data-ttu-id="a2c13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2c13-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2c13-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2c13-105">DESCRIPTION</span></span>
<span data-ttu-id="a2c13-106">Cmdleten **New-AzContainerService** skapar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="a2c13-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="a2c13-107">Ange ett behållar tjänst objekt som du kan skapa med hjälp av New-AzContainerServiceConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2c13-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="a2c13-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2c13-108">EXAMPLES</span></span>

### <span data-ttu-id="a2c13-109">Exempel 1: skapa en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="a2c13-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="a2c13-110">Det första kommandot skapar en resurs grupp med namnet ResourceGroup17 på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="a2c13-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="a2c13-111">Mer information finns i New-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2c13-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="a2c13-112">Det andra kommandot skapar en container och lagrar sedan den i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="a2c13-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="a2c13-113">Mer information finns i New-AzContainerServiceConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2c13-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="a2c13-114">Med kommandot slut skapas en behållar tjänst för behållaren som lagras i $Container.</span><span class="sxs-lookup"><span data-stu-id="a2c13-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="a2c13-115">Tjänsten heter csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="a2c13-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="a2c13-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2c13-116">PARAMETERS</span></span>

### <span data-ttu-id="a2c13-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2c13-117">-AsJob</span></span>
<span data-ttu-id="a2c13-118">RRun cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="a2c13-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a2c13-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="a2c13-119">-ContainerService</span></span>
<span data-ttu-id="a2c13-120">Anger ett Container Service-objekt som innehåller egenskaperna för den nya tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a2c13-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="a2c13-121">För att hämta ett **ContainerService** -objekt, Använd cmdleten New-AzContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="a2c13-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c13-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c13-122">-DefaultProfile</span></span>
<span data-ttu-id="a2c13-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c13-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2c13-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a2c13-124">-Name</span></span>
<span data-ttu-id="a2c13-125">Anger namnet på den behållar tjänst som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="a2c13-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a2c13-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c13-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2c13-127">Anger den resurs grupp i vilken denna cmdlet distribuerar behållar tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a2c13-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="a2c13-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a2c13-128">-Confirm</span></span>
<span data-ttu-id="a2c13-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a2c13-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2c13-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2c13-130">-WhatIf</span></span>
<span data-ttu-id="a2c13-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a2c13-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a2c13-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a2c13-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2c13-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c13-133">CommonParameters</span></span>
<span data-ttu-id="a2c13-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c13-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c13-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2c13-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c13-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2c13-136">INPUTS</span></span>

### <span data-ttu-id="a2c13-137">ContainerService</span><span class="sxs-lookup"><span data-stu-id="a2c13-137">ContainerService</span></span>
<span data-ttu-id="a2c13-138">Parametern ' ContainerService ' godkänner värdet av typen ' ContainerService ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a2c13-138">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="a2c13-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2c13-139">OUTPUTS</span></span>

### <span data-ttu-id="a2c13-140">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="a2c13-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="a2c13-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2c13-141">NOTES</span></span>

## <span data-ttu-id="a2c13-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2c13-142">RELATED LINKS</span></span>

[<span data-ttu-id="a2c13-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a2c13-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="a2c13-144">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="a2c13-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="a2c13-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a2c13-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="a2c13-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a2c13-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


