---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerService.md
ms.openlocfilehash: 9dd2018fe6f84ff4657da799fbcba720e8523bde
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93758446"
---
# <span data-ttu-id="4c32e-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4c32e-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="4c32e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c32e-102">SYNOPSIS</span></span>
<span data-ttu-id="4c32e-103">Skapar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="4c32e-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c32e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c32e-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c32e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c32e-105">DESCRIPTION</span></span>
<span data-ttu-id="4c32e-106">Cmdleten **New-AzureRmContainerService** skapar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="4c32e-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="4c32e-107">Ange ett behållar tjänst objekt som du kan skapa med hjälp av New-AzureRmContainerServiceConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c32e-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="4c32e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c32e-108">EXAMPLES</span></span>

### <span data-ttu-id="4c32e-109">Exempel 1: skapa en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="4c32e-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="4c32e-110">Det första kommandot skapar en resurs grupp med namnet ResourceGroup17 på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="4c32e-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="4c32e-111">Mer information finns i New-AzureRmResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c32e-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="4c32e-112">Det andra kommandot skapar en container och lagrar sedan den i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="4c32e-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="4c32e-113">Mer information finns i New-AzureRmContainerServiceConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c32e-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="4c32e-114">Med kommandot slut skapas en behållar tjänst för behållaren som lagras i $Container.</span><span class="sxs-lookup"><span data-stu-id="4c32e-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="4c32e-115">Tjänsten heter csResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="4c32e-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="4c32e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c32e-116">PARAMETERS</span></span>

### <span data-ttu-id="4c32e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c32e-117">-AsJob</span></span>
<span data-ttu-id="4c32e-118">RRun cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="4c32e-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4c32e-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="4c32e-119">-ContainerService</span></span>
<span data-ttu-id="4c32e-120">Anger ett Container Service-objekt som innehåller egenskaperna för den nya tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4c32e-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="4c32e-121">För att hämta ett **ContainerService** -objekt, Använd cmdleten New-AzureRmContainerServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="4c32e-121">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c32e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c32e-122">-DefaultProfile</span></span>
<span data-ttu-id="4c32e-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c32e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c32e-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="4c32e-124">-Name</span></span>
<span data-ttu-id="4c32e-125">Anger namnet på den behållar tjänst som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="4c32e-125">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c32e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c32e-126">-ResourceGroupName</span></span>
<span data-ttu-id="4c32e-127">Anger den resurs grupp i vilken denna cmdlet distribuerar behållar tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4c32e-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="4c32e-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4c32e-128">-Confirm</span></span>
<span data-ttu-id="4c32e-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4c32e-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c32e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c32e-130">-WhatIf</span></span>
<span data-ttu-id="4c32e-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4c32e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c32e-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4c32e-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c32e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c32e-133">CommonParameters</span></span>
<span data-ttu-id="4c32e-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c32e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c32e-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c32e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c32e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c32e-136">INPUTS</span></span>

### <span data-ttu-id="4c32e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4c32e-137">System.String</span></span>

### <span data-ttu-id="4c32e-138">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="4c32e-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>
<span data-ttu-id="4c32e-139">Parametrar: ContainerService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4c32e-139">Parameters: ContainerService (ByValue)</span></span>

## <span data-ttu-id="4c32e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c32e-140">OUTPUTS</span></span>

### <span data-ttu-id="4c32e-141">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="4c32e-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="4c32e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c32e-142">NOTES</span></span>

## <span data-ttu-id="4c32e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c32e-143">RELATED LINKS</span></span>

[<span data-ttu-id="4c32e-144">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4c32e-144">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="4c32e-145">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="4c32e-145">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="4c32e-146">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4c32e-146">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="4c32e-147">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4c32e-147">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


