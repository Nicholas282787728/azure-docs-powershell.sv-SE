---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 1ac0ab153177caaf080e5aa9144020ea253b8438
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521504"
---
# <span data-ttu-id="e4af1-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e4af1-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="e4af1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4af1-102">SYNOPSIS</span></span>
<span data-ttu-id="e4af1-103">Får distributions åtgärden för resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e4af1-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="e4af1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4af1-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4af1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4af1-105">DESCRIPTION</span></span>
<span data-ttu-id="e4af1-106">Cmdleten **Get-AzResourceGroupDeploymentOperation** innehåller alla åtgärder som ingick i en distribution för att hjälpa dig att identifiera och ge mer information om de exakta operationer som misslyckats för en viss distribution.</span><span class="sxs-lookup"><span data-stu-id="e4af1-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="e4af1-107">Den kan också Visa svaret och innehållet i begäran för varje distributions åtgärd.</span><span class="sxs-lookup"><span data-stu-id="e4af1-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="e4af1-108">Det här är samma information som anges i distributions informationen på portalen.</span><span class="sxs-lookup"><span data-stu-id="e4af1-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="e4af1-109">För att få begäran och svars innehållet aktiverar du inställningen när du skickar en distribution via **New-AzResourceGroupDeployment**.</span><span class="sxs-lookup"><span data-stu-id="e4af1-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="e4af1-110">Det kan vara möjligt att logga in och Visa hemligheter som lösen ord som används i resurs egenskapen eller **listKeys** operationer och sedan returneras när du hämtar distributions åtgärderna.</span><span class="sxs-lookup"><span data-stu-id="e4af1-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="e4af1-111">Om du vill ha mer information om den här inställningen och hur du aktiverar den kan du läsa distribuera mallar för New-AzResourceGroupDeployment och fel söknings verktyg</span><span class="sxs-lookup"><span data-stu-id="e4af1-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="e4af1-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4af1-112">EXAMPLES</span></span>

### <span data-ttu-id="e4af1-113">Exempel 1: Get1</span><span class="sxs-lookup"><span data-stu-id="e4af1-113">Example 1: Get1</span></span>
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="e4af1-114">Får distributions åtgärd med namnet "test" under resurs gruppen "test"</span><span class="sxs-lookup"><span data-stu-id="e4af1-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="e4af1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4af1-115">PARAMETERS</span></span>

### <span data-ttu-id="e4af1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4af1-116">-DefaultProfile</span></span>
<span data-ttu-id="e4af1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4af1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4af1-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="e4af1-118">-DeploymentName</span></span>
<span data-ttu-id="e4af1-119">Distributions namn.</span><span class="sxs-lookup"><span data-stu-id="e4af1-119">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4af1-120">-För</span><span class="sxs-lookup"><span data-stu-id="e4af1-120">-Pre</span></span>
<span data-ttu-id="e4af1-121">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e4af1-121">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e4af1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4af1-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4af1-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e4af1-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4af1-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4af1-124">-SubscriptionId</span></span>
<span data-ttu-id="e4af1-125">Abonnemanget som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e4af1-125">The subscription to use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4af1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4af1-126">CommonParameters</span></span>
<span data-ttu-id="e4af1-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4af1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4af1-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4af1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4af1-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4af1-129">INPUTS</span></span>

### <span data-ttu-id="e4af1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e4af1-130">System.String</span></span>

### <span data-ttu-id="e4af1-131">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e4af1-131">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e4af1-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4af1-132">OUTPUTS</span></span>

### <span data-ttu-id="e4af1-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e4af1-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="e4af1-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4af1-134">NOTES</span></span>

## <span data-ttu-id="e4af1-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4af1-135">RELATED LINKS</span></span>
