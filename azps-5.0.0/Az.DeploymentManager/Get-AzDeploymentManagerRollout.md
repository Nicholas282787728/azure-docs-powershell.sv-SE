---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320160"
---
# <span data-ttu-id="144f8-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="144f8-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="144f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="144f8-102">SYNOPSIS</span></span>
<span data-ttu-id="144f8-103">Hämtar installationen.</span><span class="sxs-lookup"><span data-stu-id="144f8-103">Gets the rollout.</span></span>

## <span data-ttu-id="144f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="144f8-104">SYNTAX</span></span>

### <span data-ttu-id="144f8-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="144f8-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="144f8-106">ID</span><span class="sxs-lookup"><span data-stu-id="144f8-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="144f8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="144f8-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="144f8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="144f8-108">DESCRIPTION</span></span>
<span data-ttu-id="144f8-109">Cmdleten **Get-AzDeploymentManagerRollout** hämtar en introduktion och returnerar ett objekt som representerar en installation med all detaljerad information om hur installationen fortskrider.</span><span class="sxs-lookup"><span data-stu-id="144f8-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="144f8-110">Ange utgivningen med dess namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="144f8-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="144f8-111">Du kan också ange ett installations objekt eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="144f8-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="144f8-112">Det hämtade installations-objektet innehåller tjänster, tjänste enheter och steg som har distribuerats och de som pågår.</span><span class="sxs-lookup"><span data-stu-id="144f8-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="144f8-113">De som ännu inte ska distribueras är inte i svaret.</span><span class="sxs-lookup"><span data-stu-id="144f8-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="144f8-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="144f8-114">EXAMPLES</span></span>

### <span data-ttu-id="144f8-115">Exempel 1 kom igång</span><span class="sxs-lookup"><span data-stu-id="144f8-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="144f8-116">Det här kommandot får en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="144f8-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="144f8-117">Exempel 2 Hämta och Visa information om installationen</span><span class="sxs-lookup"><span data-stu-id="144f8-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="144f8-118">Det här kommandot får en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="144f8-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="144f8-119">Växeln-verbose visar alla utgivnings uppgifter hierarkiskt; visar tjänsterna, ServiceUnits och stegen under varje ServiceUnit och kontextuell information för varje steg i en helhets vy av lanseringen.</span><span class="sxs-lookup"><span data-stu-id="144f8-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="144f8-120">Exempel 3: komma igång med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="144f8-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="144f8-121">Det här kommandot får en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="144f8-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="144f8-122">Exempel 4: kom igång med installations objekt.</span><span class="sxs-lookup"><span data-stu-id="144f8-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="144f8-123">Det här kommandot får en installation vars namn och ResourceGroup matchar $rolloutObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="144f8-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="144f8-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="144f8-124">PARAMETERS</span></span>

### <span data-ttu-id="144f8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="144f8-125">-DefaultProfile</span></span>
<span data-ttu-id="144f8-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="144f8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="144f8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="144f8-127">-InputObject</span></span>
<span data-ttu-id="144f8-128">Introduktions objekt.</span><span class="sxs-lookup"><span data-stu-id="144f8-128">Rollout object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="144f8-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="144f8-129">-Name</span></span>
<span data-ttu-id="144f8-130">Namnet på installationen.</span><span class="sxs-lookup"><span data-stu-id="144f8-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="144f8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="144f8-131">-ResourceGroupName</span></span>
<span data-ttu-id="144f8-132">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="144f8-132">The resource group.</span></span>

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

### <span data-ttu-id="144f8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="144f8-133">-ResourceId</span></span>
<span data-ttu-id="144f8-134">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="144f8-134">The resource identifier.</span></span>

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

### <span data-ttu-id="144f8-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="144f8-135">-RetryAttempt</span></span>
<span data-ttu-id="144f8-136">Försök igen.</span><span class="sxs-lookup"><span data-stu-id="144f8-136">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="144f8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="144f8-137">CommonParameters</span></span>
<span data-ttu-id="144f8-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="144f8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="144f8-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="144f8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="144f8-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="144f8-140">INPUTS</span></span>

### <span data-ttu-id="144f8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="144f8-141">System.String</span></span>

### <span data-ttu-id="144f8-142">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="144f8-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="144f8-143">Microsoft. Azure. commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="144f8-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="144f8-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="144f8-144">OUTPUTS</span></span>

### <span data-ttu-id="144f8-145">Microsoft. Azure. commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="144f8-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="144f8-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="144f8-146">NOTES</span></span>

## <span data-ttu-id="144f8-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="144f8-147">RELATED LINKS</span></span>
