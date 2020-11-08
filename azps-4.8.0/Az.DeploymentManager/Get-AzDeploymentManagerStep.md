---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 68bc2af69c3450f0c52c5613057ba4b2db211ee8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260009"
---
# <span data-ttu-id="c970d-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="c970d-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="c970d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c970d-102">SYNOPSIS</span></span>
<span data-ttu-id="c970d-103">Hämtar steget.</span><span class="sxs-lookup"><span data-stu-id="c970d-103">Gets the step.</span></span>

## <span data-ttu-id="c970d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c970d-104">SYNTAX</span></span>

### <span data-ttu-id="c970d-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="c970d-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c970d-106">ID</span><span class="sxs-lookup"><span data-stu-id="c970d-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c970d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c970d-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c970d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c970d-108">DESCRIPTION</span></span>
<span data-ttu-id="c970d-109">Cmdleten **Get-AzDeploymentManagerStep** får ett steg och returnerar ett objekt som representerar det steget.</span><span class="sxs-lookup"><span data-stu-id="c970d-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="c970d-110">Ange steget med dess namn och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c970d-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="c970d-111">Du kan också ange Step-ID eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c970d-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="c970d-112">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på artefakt källan med hjälp av Set-AzDeploymentManagerStep cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c970d-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="c970d-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c970d-113">EXAMPLES</span></span>

### <span data-ttu-id="c970d-114">Exempel 1: få ett steg</span><span class="sxs-lookup"><span data-stu-id="c970d-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="c970d-115">Det här kommandot får ett steg med namnet ContosoService1WaitStep i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c970d-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="c970d-116">Exempel 2: Hämta ett steg med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="c970d-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="c970d-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c970d-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="c970d-118">Det här kommandot får ett steg med namnet ContosoService1WaitStep i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c970d-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="c970d-119">Exempel 3: Hämta ett steg med ett objekt som returneras av New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="c970d-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="c970d-120">Det här kommandot får ett steg vars namn och ResourceGroup matchar $stepObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="c970d-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="c970d-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c970d-121">PARAMETERS</span></span>

### <span data-ttu-id="c970d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c970d-122">-DefaultProfile</span></span>
<span data-ttu-id="c970d-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c970d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c970d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c970d-124">-InputObject</span></span>
<span data-ttu-id="c970d-125">Jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="c970d-125">The step resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c970d-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="c970d-126">-Name</span></span>
<span data-ttu-id="c970d-127">Namnet på steget.</span><span class="sxs-lookup"><span data-stu-id="c970d-127">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c970d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c970d-128">-ResourceGroupName</span></span>
<span data-ttu-id="c970d-129">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c970d-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c970d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c970d-130">-ResourceId</span></span>
<span data-ttu-id="c970d-131">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c970d-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c970d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c970d-132">CommonParameters</span></span>
<span data-ttu-id="c970d-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c970d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c970d-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c970d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c970d-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c970d-135">INPUTS</span></span>

### <span data-ttu-id="c970d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c970d-136">System.String</span></span>

### <span data-ttu-id="c970d-137">Microsoft. Azure. commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="c970d-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="c970d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c970d-138">OUTPUTS</span></span>

### <span data-ttu-id="c970d-139">Microsoft. Azure. commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="c970d-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="c970d-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c970d-140">NOTES</span></span>

## <span data-ttu-id="c970d-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c970d-141">RELATED LINKS</span></span>
