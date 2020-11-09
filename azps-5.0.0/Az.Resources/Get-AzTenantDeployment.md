---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322889"
---
# <span data-ttu-id="545eb-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="545eb-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="545eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="545eb-102">SYNOPSIS</span></span>
<span data-ttu-id="545eb-103">Gå med i klient omfattningen</span><span class="sxs-lookup"><span data-stu-id="545eb-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="545eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="545eb-104">SYNTAX</span></span>

### <span data-ttu-id="545eb-105">GetByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="545eb-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="545eb-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="545eb-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="545eb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="545eb-107">DESCRIPTION</span></span>
<span data-ttu-id="545eb-108">Cmdleten **Get-AzTenantDeployment** får distributionerna på klient området.</span><span class="sxs-lookup"><span data-stu-id="545eb-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="545eb-109">Ange parametern *namn* eller *ID* för att filtrera resultaten.</span><span class="sxs-lookup"><span data-stu-id="545eb-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="545eb-110">Som standard får **Get-AzTenantDeployment** alla distributioner på klient omfattningen.</span><span class="sxs-lookup"><span data-stu-id="545eb-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="545eb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="545eb-111">EXAMPLES</span></span>

### <span data-ttu-id="545eb-112">Exempel 1: Hämta alla distributioner på klient området</span><span class="sxs-lookup"><span data-stu-id="545eb-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="545eb-113">Det här kommandot får alla distributioner i det aktuella klient scopet.</span><span class="sxs-lookup"><span data-stu-id="545eb-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="545eb-114">Exempel 2: skaffa en distribution utifrån namn</span><span class="sxs-lookup"><span data-stu-id="545eb-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="545eb-115">Det här kommandot får distributionen "Deploy01" till den aktuella klient organisations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="545eb-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="545eb-116">Du kan tilldela ett namn till en distribution när du skapar det med hjälp av cmdleten **New-AzTenantDeployment** .</span><span class="sxs-lookup"><span data-stu-id="545eb-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="545eb-117">Om du inte tilldelar ett namn anger cmdletarna ett standard namn baserat på mallen som används för att skapa distributionen.</span><span class="sxs-lookup"><span data-stu-id="545eb-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="545eb-118">Exempel 3: skaffa en distribution utifrån ID</span><span class="sxs-lookup"><span data-stu-id="545eb-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="545eb-119">Med det här kommandot får du "Deploy01"-distributionen hos klient området.</span><span class="sxs-lookup"><span data-stu-id="545eb-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="545eb-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="545eb-120">PARAMETERS</span></span>

### <span data-ttu-id="545eb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545eb-121">-DefaultProfile</span></span>
<span data-ttu-id="545eb-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="545eb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="545eb-123">-ID</span><span class="sxs-lookup"><span data-stu-id="545eb-123">-Id</span></span>
<span data-ttu-id="545eb-124">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="545eb-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="545eb-125">exempel:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="545eb-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="545eb-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="545eb-126">-Name</span></span>
<span data-ttu-id="545eb-127">Distributionens namn.</span><span class="sxs-lookup"><span data-stu-id="545eb-127">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545eb-128">-För</span><span class="sxs-lookup"><span data-stu-id="545eb-128">-Pre</span></span>
<span data-ttu-id="545eb-129">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="545eb-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="545eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545eb-130">CommonParameters</span></span>
<span data-ttu-id="545eb-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="545eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545eb-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="545eb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545eb-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="545eb-133">INPUTS</span></span>

### <span data-ttu-id="545eb-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="545eb-134">None</span></span>

## <span data-ttu-id="545eb-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="545eb-135">OUTPUTS</span></span>

### <span data-ttu-id="545eb-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="545eb-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="545eb-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="545eb-137">NOTES</span></span>

## <span data-ttu-id="545eb-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="545eb-138">RELATED LINKS</span></span>
