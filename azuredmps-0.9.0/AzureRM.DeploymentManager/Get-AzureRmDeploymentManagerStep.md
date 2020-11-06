---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571531"
---
# <span data-ttu-id="32e6f-101">Get-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="32e6f-101">Get-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="32e6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="32e6f-103">Hämtar distributions steget.</span><span class="sxs-lookup"><span data-stu-id="32e6f-103">Gets the deployment step.</span></span>

## <span data-ttu-id="32e6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32e6f-104">SYNTAX</span></span>

### <span data-ttu-id="32e6f-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="32e6f-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32e6f-106">ID</span><span class="sxs-lookup"><span data-stu-id="32e6f-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32e6f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="32e6f-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32e6f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32e6f-108">DESCRIPTION</span></span>
<span data-ttu-id="32e6f-109">Cmdleten **Get-AzureRmDeploymentManagerStep** får ett steg och returnerar ett objekt som representerar det steget.</span><span class="sxs-lookup"><span data-stu-id="32e6f-109">The **Get-AzureRmDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="32e6f-110">Ange steget med dess namn och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="32e6f-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="32e6f-111">Du kan också ange Step-ID eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="32e6f-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="32e6f-112">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på artefakt källan med hjälp av Set-AzureRmDeploymentManagerStep cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32e6f-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="32e6f-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32e6f-113">EXAMPLES</span></span>

### <span data-ttu-id="32e6f-114">Exempel 1: få ett steg</span><span class="sxs-lookup"><span data-stu-id="32e6f-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="32e6f-115">Det här kommandot får ett steg med namnet ContosoService1WaitStep i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="32e6f-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="32e6f-116">Exempel 2: Hämta ett steg med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="32e6f-116">Example 2: Get a step using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="32e6f-117">Det här kommandot får ett steg med namnet ContosoService1WaitStep i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="32e6f-117">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="32e6f-118">Exempel 3: Hämta ett steg med ett objekt som returneras av New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="32e6f-118">Example 3: Get a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="32e6f-119">Det här kommandot får ett steg vars namn och ResourceGroup matchar $stepObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="32e6f-119">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>


## <span data-ttu-id="32e6f-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32e6f-120">PARAMETERS</span></span>

### <span data-ttu-id="32e6f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e6f-121">-DefaultProfile</span></span>
<span data-ttu-id="32e6f-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="32e6f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32e6f-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="32e6f-123">-Name</span></span>
<span data-ttu-id="32e6f-124">Namnet på steget.</span><span class="sxs-lookup"><span data-stu-id="32e6f-124">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32e6f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32e6f-125">-ResourceGroupName</span></span>
<span data-ttu-id="32e6f-126">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="32e6f-126">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32e6f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32e6f-127">-ResourceId</span></span>
<span data-ttu-id="32e6f-128">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="32e6f-128">The resource identifier.</span></span>

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

### <span data-ttu-id="32e6f-129">-Steg</span><span class="sxs-lookup"><span data-stu-id="32e6f-129">-Step</span></span>
<span data-ttu-id="32e6f-130">Jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="32e6f-130">The step resource object.</span></span>

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

### <span data-ttu-id="32e6f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e6f-131">CommonParameters</span></span>
<span data-ttu-id="32e6f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32e6f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="32e6f-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e6f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e6f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32e6f-134">INPUTS</span></span>

### <span data-ttu-id="32e6f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="32e6f-135">System.String</span></span>

### <span data-ttu-id="32e6f-136">Microsoft. Azure. commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="32e6f-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="32e6f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32e6f-137">OUTPUTS</span></span>

### <span data-ttu-id="32e6f-138">Microsoft. Azure. commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="32e6f-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="32e6f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32e6f-139">NOTES</span></span>

## <span data-ttu-id="32e6f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32e6f-140">RELATED LINKS</span></span>
