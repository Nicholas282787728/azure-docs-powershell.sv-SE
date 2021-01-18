---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521468"
---
# <span data-ttu-id="d1933-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d1933-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="d1933-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1933-102">SYNOPSIS</span></span>
<span data-ttu-id="d1933-103">Skaffa distributions åtgärd för distribution med klient-scope</span><span class="sxs-lookup"><span data-stu-id="d1933-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="d1933-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1933-104">SYNTAX</span></span>

### <span data-ttu-id="d1933-105">GetByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="d1933-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1933-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d1933-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1933-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1933-107">DESCRIPTION</span></span>
<span data-ttu-id="d1933-108">Cmdleten **Get-AzTenantDeploymentOperation** innehåller alla åtgärder som ingick i distributionen i den aktuella klient omfattningen för att hjälpa dig att identifiera och ge mer information om de exakta operationer som misslyckats för en viss distribution.</span><span class="sxs-lookup"><span data-stu-id="d1933-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="d1933-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1933-109">EXAMPLES</span></span>

### <span data-ttu-id="d1933-110">Exempel 1: skaffa distributions åtgärder som fått ett distributions namn</span><span class="sxs-lookup"><span data-stu-id="d1933-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="d1933-111">Hämtar distributions åtgärder med namnet "Deploy01" i det aktuella klient scopet.</span><span class="sxs-lookup"><span data-stu-id="d1933-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="d1933-112">Exempel 2: skaffa en distribution och få drift sättnings åtgärder</span><span class="sxs-lookup"><span data-stu-id="d1933-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="d1933-113">Det här kommandot får distributionen "Deploy01" vid den aktuella klient omfattningen och får drift sättnings åtgärder.</span><span class="sxs-lookup"><span data-stu-id="d1933-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="d1933-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1933-114">PARAMETERS</span></span>

### <span data-ttu-id="d1933-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1933-115">-DefaultProfile</span></span>
<span data-ttu-id="d1933-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1933-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1933-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d1933-117">-DeploymentName</span></span>
<span data-ttu-id="d1933-118">Distributions namn.</span><span class="sxs-lookup"><span data-stu-id="d1933-118">The deployment name.</span></span>

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

### <span data-ttu-id="d1933-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d1933-119">-DeploymentObject</span></span>
<span data-ttu-id="d1933-120">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="d1933-120">The deployment object.</span></span>

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

### <span data-ttu-id="d1933-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d1933-121">-OperationId</span></span>
<span data-ttu-id="d1933-122">Distributions åtgärdens ID.</span><span class="sxs-lookup"><span data-stu-id="d1933-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="d1933-123">-För</span><span class="sxs-lookup"><span data-stu-id="d1933-123">-Pre</span></span>
<span data-ttu-id="d1933-124">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d1933-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d1933-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1933-125">CommonParameters</span></span>
<span data-ttu-id="d1933-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1933-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1933-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1933-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1933-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1933-128">INPUTS</span></span>

### <span data-ttu-id="d1933-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d1933-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d1933-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1933-130">OUTPUTS</span></span>

### <span data-ttu-id="d1933-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d1933-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="d1933-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1933-132">NOTES</span></span>

## <span data-ttu-id="d1933-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1933-133">RELATED LINKS</span></span>
