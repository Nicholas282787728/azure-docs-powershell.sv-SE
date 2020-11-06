---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 21d0b4f7feec5b32ff732f880924becddd84db73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571276"
---
# <span data-ttu-id="6a789-101">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="6a789-101">Get-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="6a789-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a789-102">SYNOPSIS</span></span>
<span data-ttu-id="6a789-103">Får en lansering.</span><span class="sxs-lookup"><span data-stu-id="6a789-103">Gets a rollout.</span></span>

## <span data-ttu-id="6a789-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a789-104">SYNTAX</span></span>

### <span data-ttu-id="6a789-105">Interaktivt (standard)</span><span class="sxs-lookup"><span data-stu-id="6a789-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [[-RetryAttempt] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a789-106">ID</span><span class="sxs-lookup"><span data-stu-id="6a789-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a789-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6a789-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a789-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a789-108">DESCRIPTION</span></span>
<span data-ttu-id="6a789-109">Cmdleten **Get-AzureRmDeploymentManagerRollout** hämtar en introduktion och returnerar ett objekt som representerar en installation med all detaljerad information om hur installationen fortskrider.</span><span class="sxs-lookup"><span data-stu-id="6a789-109">The **Get-AzureRmDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="6a789-110">Ange utgivningen med dess namn och resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6a789-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="6a789-111">Du kan också ange ett installations objekt eller ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6a789-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="6a789-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a789-112">EXAMPLES</span></span>

### <span data-ttu-id="6a789-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6a789-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="6a789-114">Det här kommandot får en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6a789-114">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6a789-115">Exempel 2: komma igång med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="6a789-115">Example 2: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="6a789-116">Det här kommandot får en installation med namnet ContosoRollout i ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6a789-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6a789-117">Exempel 3: kom igång med installations objekt.</span><span class="sxs-lookup"><span data-stu-id="6a789-117">Example 3: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="6a789-118">Det här kommandot får en installation vars namn och ResourceGroup matchar $rolloutObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6a789-118">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="6a789-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a789-119">PARAMETERS</span></span>

### <span data-ttu-id="6a789-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a789-120">-DefaultProfile</span></span>
<span data-ttu-id="6a789-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a789-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a789-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="6a789-122">-Name</span></span>
<span data-ttu-id="6a789-123">Namnet på installationen.</span><span class="sxs-lookup"><span data-stu-id="6a789-123">The name of the rollout.</span></span>

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

### <span data-ttu-id="6a789-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a789-124">-ResourceGroupName</span></span>
<span data-ttu-id="6a789-125">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6a789-125">The resource group.</span></span>

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

### <span data-ttu-id="6a789-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a789-126">-ResourceId</span></span>
<span data-ttu-id="6a789-127">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6a789-127">The resource identifier.</span></span>

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

### <span data-ttu-id="6a789-128">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="6a789-128">-RetryAttempt</span></span>
<span data-ttu-id="6a789-129">Försök igen.</span><span class="sxs-lookup"><span data-stu-id="6a789-129">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a789-130">-Lansering</span><span class="sxs-lookup"><span data-stu-id="6a789-130">-Rollout</span></span>
<span data-ttu-id="6a789-131">Introduktions objekt.</span><span class="sxs-lookup"><span data-stu-id="6a789-131">Rollout object.</span></span>

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

### <span data-ttu-id="6a789-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a789-132">CommonParameters</span></span>
<span data-ttu-id="6a789-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a789-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a789-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a789-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a789-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a789-135">INPUTS</span></span>

### <span data-ttu-id="6a789-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="6a789-136">None</span></span>

## <span data-ttu-id="6a789-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a789-137">OUTPUTS</span></span>

### <span data-ttu-id="6a789-138">Microsoft. Azure. commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="6a789-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="6a789-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a789-139">NOTES</span></span>

## <span data-ttu-id="6a789-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a789-140">RELATED LINKS</span></span>

[<span data-ttu-id="6a789-141">Stopp-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="6a789-141">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="6a789-142">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="6a789-142">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="6a789-143">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="6a789-143">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)