---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: c3218141e495bb92216e254830ddaa7dd7a0a0c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102582"
---
# <span data-ttu-id="364e3-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="364e3-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="364e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="364e3-102">SYNOPSIS</span></span>
<span data-ttu-id="364e3-103">Gå med i klient omfattningen</span><span class="sxs-lookup"><span data-stu-id="364e3-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="364e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="364e3-104">SYNTAX</span></span>

### <span data-ttu-id="364e3-105">GetByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="364e3-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="364e3-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="364e3-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="364e3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="364e3-107">DESCRIPTION</span></span>
<span data-ttu-id="364e3-108">Cmdleten **Get-AzTenantDeployment** får distributionerna på klient området.</span><span class="sxs-lookup"><span data-stu-id="364e3-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="364e3-109">Ange parametern *namn* eller *ID* för att filtrera resultaten.</span><span class="sxs-lookup"><span data-stu-id="364e3-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="364e3-110">Som standard får **Get-AzTenantDeployment** alla distributioner på klient omfattningen.</span><span class="sxs-lookup"><span data-stu-id="364e3-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="364e3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="364e3-111">EXAMPLES</span></span>

### <span data-ttu-id="364e3-112">Exempel 1: Hämta alla distributioner på klient området</span><span class="sxs-lookup"><span data-stu-id="364e3-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="364e3-113">Det här kommandot får alla distributioner i det aktuella klient scopet.</span><span class="sxs-lookup"><span data-stu-id="364e3-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="364e3-114">Exempel 2: skaffa en distribution utifrån namn</span><span class="sxs-lookup"><span data-stu-id="364e3-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="364e3-115">Det här kommandot får distributionen "Deploy01" till den aktuella klient organisations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="364e3-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="364e3-116">Du kan tilldela ett namn till en distribution när du skapar det med hjälp av cmdleten **New-AzTenantDeployment** .</span><span class="sxs-lookup"><span data-stu-id="364e3-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="364e3-117">Om du inte tilldelar ett namn anger cmdletarna ett standard namn baserat på mallen som används för att skapa distributionen.</span><span class="sxs-lookup"><span data-stu-id="364e3-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="364e3-118">Exempel 3: skaffa en distribution utifrån ID</span><span class="sxs-lookup"><span data-stu-id="364e3-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="364e3-119">Med det här kommandot får du "Deploy01"-distributionen hos klient området.</span><span class="sxs-lookup"><span data-stu-id="364e3-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="364e3-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="364e3-120">PARAMETERS</span></span>

### <span data-ttu-id="364e3-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="364e3-121">-ApiVersion</span></span>
<span data-ttu-id="364e3-122">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="364e3-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="364e3-123">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="364e3-123">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="364e3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364e3-124">-DefaultProfile</span></span>
<span data-ttu-id="364e3-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="364e3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="364e3-126">-ID</span><span class="sxs-lookup"><span data-stu-id="364e3-126">-Id</span></span>
<span data-ttu-id="364e3-127">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="364e3-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="364e3-128">exempel:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="364e3-128">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="364e3-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="364e3-129">-Name</span></span>
<span data-ttu-id="364e3-130">Distributionens namn.</span><span class="sxs-lookup"><span data-stu-id="364e3-130">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="364e3-131">-För</span><span class="sxs-lookup"><span data-stu-id="364e3-131">-Pre</span></span>
<span data-ttu-id="364e3-132">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="364e3-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="364e3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364e3-133">CommonParameters</span></span>
<span data-ttu-id="364e3-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="364e3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364e3-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="364e3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364e3-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="364e3-136">INPUTS</span></span>

### <span data-ttu-id="364e3-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="364e3-137">None</span></span>

## <span data-ttu-id="364e3-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="364e3-138">OUTPUTS</span></span>

### <span data-ttu-id="364e3-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="364e3-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="364e3-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="364e3-140">NOTES</span></span>

## <span data-ttu-id="364e3-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="364e3-141">RELATED LINKS</span></span>
