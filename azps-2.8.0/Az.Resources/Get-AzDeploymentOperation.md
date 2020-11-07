---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 809e7e82948d155ad73a80cbd430499d5372b644
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919336"
---
# <span data-ttu-id="a20f4-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a20f4-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="a20f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a20f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a20f4-103">Skaffa distributions åtgärd</span><span class="sxs-lookup"><span data-stu-id="a20f4-103">Get deployment operation</span></span>

## <span data-ttu-id="a20f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a20f4-104">SYNTAX</span></span>

### <span data-ttu-id="a20f4-105">GetByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="a20f4-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a20f4-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a20f4-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a20f4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a20f4-107">DESCRIPTION</span></span>
<span data-ttu-id="a20f4-108">Cmdleten **Get-AzDeploymentOperation** innehåller alla åtgärder som ingick i en distribution för att hjälpa dig att identifiera och ge mer information om de exakta operationer som misslyckats för en viss distribution.</span><span class="sxs-lookup"><span data-stu-id="a20f4-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="a20f4-109">Den kan också Visa svaret och innehållet i begäran för varje distributions åtgärd.</span><span class="sxs-lookup"><span data-stu-id="a20f4-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="a20f4-110">Det här är samma information som anges i distributions informationen på portalen.</span><span class="sxs-lookup"><span data-stu-id="a20f4-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="a20f4-111">För att få begäran och svars innehållet aktiverar du inställningen när du skickar en distribution via **New-AzDeployment**.</span><span class="sxs-lookup"><span data-stu-id="a20f4-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="a20f4-112">Det kan vara möjligt att logga in och Visa hemligheter som lösen ord som används i resurs egenskapen eller **listKeys** operationer och sedan returneras när du hämtar distributions åtgärderna.</span><span class="sxs-lookup"><span data-stu-id="a20f4-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="a20f4-113">Om du vill ha mer information om den här inställningen och hur du aktiverar den kan du läsa distribuera mallar för New-AzDeployment och fel söknings verktyg</span><span class="sxs-lookup"><span data-stu-id="a20f4-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="a20f4-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a20f4-114">EXAMPLES</span></span>

### <span data-ttu-id="a20f4-115">Skaffa distributions åtgärder som fått ett distributions namn</span><span class="sxs-lookup"><span data-stu-id="a20f4-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="a20f4-116">Får distributions åtgärd med namnet "test" i den aktuella prenumerationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="a20f4-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="a20f4-117">Skaffa en distribution och få drift sättnings åtgärder</span><span class="sxs-lookup"><span data-stu-id="a20f4-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="a20f4-118">Det här kommandot får distributionen "test" vid den aktuella prenumerationens omfattning och får drift sättnings åtgärder.</span><span class="sxs-lookup"><span data-stu-id="a20f4-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="a20f4-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a20f4-119">PARAMETERS</span></span>

### <span data-ttu-id="a20f4-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a20f4-120">-ApiVersion</span></span>
<span data-ttu-id="a20f4-121">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a20f4-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a20f4-122">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="a20f4-122">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a20f4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a20f4-123">-DefaultProfile</span></span>
<span data-ttu-id="a20f4-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a20f4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a20f4-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="a20f4-125">-DeploymentName</span></span>
<span data-ttu-id="a20f4-126">Distributions namn.</span><span class="sxs-lookup"><span data-stu-id="a20f4-126">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a20f4-127">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a20f4-127">-DeploymentObject</span></span>
<span data-ttu-id="a20f4-128">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="a20f4-128">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a20f4-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a20f4-129">-OperationId</span></span>
<span data-ttu-id="a20f4-130">Distributions åtgärdens ID.</span><span class="sxs-lookup"><span data-stu-id="a20f4-130">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a20f4-131">-För</span><span class="sxs-lookup"><span data-stu-id="a20f4-131">-Pre</span></span>
<span data-ttu-id="a20f4-132">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a20f4-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a20f4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20f4-133">CommonParameters</span></span>
<span data-ttu-id="a20f4-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a20f4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20f4-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a20f4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20f4-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a20f4-136">INPUTS</span></span>

### <span data-ttu-id="a20f4-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="a20f4-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a20f4-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a20f4-138">OUTPUTS</span></span>

### <span data-ttu-id="a20f4-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a20f4-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="a20f4-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a20f4-140">NOTES</span></span>

## <span data-ttu-id="a20f4-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a20f4-141">RELATED LINKS</span></span>
