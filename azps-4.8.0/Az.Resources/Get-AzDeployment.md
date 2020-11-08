---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 5ea6e36adeb1c0b220b87d516e9c236907bc2c63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258711"
---
# <span data-ttu-id="de760-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="de760-101">Get-AzDeployment</span></span>

## <span data-ttu-id="de760-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de760-102">SYNOPSIS</span></span>
<span data-ttu-id="de760-103">Skaffa distribution</span><span class="sxs-lookup"><span data-stu-id="de760-103">Get deployment</span></span>

## <span data-ttu-id="de760-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de760-104">SYNTAX</span></span>

### <span data-ttu-id="de760-105">GetByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="de760-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de760-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="de760-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de760-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de760-107">DESCRIPTION</span></span>
<span data-ttu-id="de760-108">Cmdleten **Get-AzDeployment** får distributionerna med den aktuella prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="de760-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="de760-109">Ange parametern *namn* eller *ID* för att filtrera resultaten.</span><span class="sxs-lookup"><span data-stu-id="de760-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="de760-110">Som standard får **Get-AzDeployment** alla distributioner vid aktuell prenumerations omfattning.</span><span class="sxs-lookup"><span data-stu-id="de760-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="de760-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de760-111">EXAMPLES</span></span>

### <span data-ttu-id="de760-112">Exempel 1: Hämta alla distributioner i prenumerations omfattning</span><span class="sxs-lookup"><span data-stu-id="de760-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="de760-113">Det här kommandot får alla distributioner vid aktuell prenumeration.</span><span class="sxs-lookup"><span data-stu-id="de760-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="de760-114">Exempel 2: skaffa en distribution utifrån namn</span><span class="sxs-lookup"><span data-stu-id="de760-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="de760-115">Det här kommandot hämtar DeployRoles01-distributionen för den aktuella prenumerationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="de760-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="de760-116">Du kan tilldela ett namn till en distribution när du skapar det med hjälp av cmdleten **New-AzDeployment** .</span><span class="sxs-lookup"><span data-stu-id="de760-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="de760-117">Om du inte tilldelar ett namn anger cmdletarna ett standard namn baserat på mallen som används för att skapa distributionen.</span><span class="sxs-lookup"><span data-stu-id="de760-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="de760-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de760-118">PARAMETERS</span></span>

### <span data-ttu-id="de760-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="de760-119">-ApiVersion</span></span>
<span data-ttu-id="de760-120">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="de760-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="de760-121">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="de760-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="de760-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de760-122">-DefaultProfile</span></span>
<span data-ttu-id="de760-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de760-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de760-124">-ID</span><span class="sxs-lookup"><span data-stu-id="de760-124">-Id</span></span>
<span data-ttu-id="de760-125">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="de760-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="de760-126">exempel:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="de760-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de760-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="de760-127">-Name</span></span>
<span data-ttu-id="de760-128">Distributionens namn.</span><span class="sxs-lookup"><span data-stu-id="de760-128">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de760-129">-För</span><span class="sxs-lookup"><span data-stu-id="de760-129">-Pre</span></span>
<span data-ttu-id="de760-130">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="de760-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="de760-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de760-131">CommonParameters</span></span>
<span data-ttu-id="de760-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de760-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de760-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de760-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de760-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de760-134">INPUTS</span></span>

### <span data-ttu-id="de760-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="de760-135">None</span></span>

## <span data-ttu-id="de760-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de760-136">OUTPUTS</span></span>

### <span data-ttu-id="de760-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="de760-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="de760-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de760-138">NOTES</span></span>

## <span data-ttu-id="de760-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de760-139">RELATED LINKS</span></span>
