---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeployment.md
ms.openlocfilehash: 6d25bcf98adb740ec695152eb5b27ec9402082c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755814"
---
# <span data-ttu-id="d55a8-101">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="d55a8-101">Get-AzureRmDeployment</span></span>

## <span data-ttu-id="d55a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d55a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d55a8-103">Skaffa distribution</span><span class="sxs-lookup"><span data-stu-id="d55a8-103">Get deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d55a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d55a8-104">SYNTAX</span></span>

### <span data-ttu-id="d55a8-105">GetByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="d55a8-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d55a8-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d55a8-106">GetByDeploymentId</span></span>
```
Get-AzureRmDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d55a8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d55a8-107">DESCRIPTION</span></span>
<span data-ttu-id="d55a8-108">Cmdleten **Get-AzureRmDeployment** får distributionerna med den aktuella prenumerations omfattningen.</span><span class="sxs-lookup"><span data-stu-id="d55a8-108">The **Get-AzureRmDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="d55a8-109">Ange parametern *namn* eller *ID* för att filtrera resultaten.</span><span class="sxs-lookup"><span data-stu-id="d55a8-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="d55a8-110">Som standard får **Get-AzureRmDeployment** alla distributioner vid aktuell prenumerations omfattning.</span><span class="sxs-lookup"><span data-stu-id="d55a8-110">By default, **Get-AzureRmDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="d55a8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d55a8-111">EXAMPLES</span></span>

### <span data-ttu-id="d55a8-112">Exempel 1: Hämta alla distributioner i prenumerations omfattning</span><span class="sxs-lookup"><span data-stu-id="d55a8-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzureRmDeployment
```

<span data-ttu-id="d55a8-113">Det här kommandot får alla distributioner vid aktuell prenumeration.</span><span class="sxs-lookup"><span data-stu-id="d55a8-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="d55a8-114">Exempel 2: skaffa en distribution utifrån namn</span><span class="sxs-lookup"><span data-stu-id="d55a8-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "DeployRoles01"
```

<span data-ttu-id="d55a8-115">Det här kommandot hämtar DeployRoles01-distributionen för den aktuella prenumerationens omfattning.</span><span class="sxs-lookup"><span data-stu-id="d55a8-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="d55a8-116">Du kan tilldela ett namn till en distribution när du skapar det med hjälp av cmdleten **New-AzureRmDeployment** .</span><span class="sxs-lookup"><span data-stu-id="d55a8-116">You can assign a name to a deployment when you create it by using the **New-AzureRmDeployment** cmdlets.</span></span>
<span data-ttu-id="d55a8-117">Om du inte tilldelar ett namn anger cmdletarna ett standard namn baserat på mallen som används för att skapa distributionen.</span><span class="sxs-lookup"><span data-stu-id="d55a8-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="d55a8-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d55a8-118">PARAMETERS</span></span>

### <span data-ttu-id="d55a8-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d55a8-119">-ApiVersion</span></span>
<span data-ttu-id="d55a8-120">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d55a8-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d55a8-121">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="d55a8-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d55a8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d55a8-122">-DefaultProfile</span></span>
<span data-ttu-id="d55a8-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d55a8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d55a8-124">-ID</span><span class="sxs-lookup"><span data-stu-id="d55a8-124">-Id</span></span>
<span data-ttu-id="d55a8-125">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="d55a8-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d55a8-126">exempel:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="d55a8-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d55a8-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="d55a8-127">-Name</span></span>
<span data-ttu-id="d55a8-128">Distributionens namn.</span><span class="sxs-lookup"><span data-stu-id="d55a8-128">The name of deployment.</span></span>

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

### <span data-ttu-id="d55a8-129">-För</span><span class="sxs-lookup"><span data-stu-id="d55a8-129">-Pre</span></span>
<span data-ttu-id="d55a8-130">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d55a8-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d55a8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d55a8-131">CommonParameters</span></span>
<span data-ttu-id="d55a8-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d55a8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d55a8-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d55a8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d55a8-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d55a8-134">INPUTS</span></span>

### <span data-ttu-id="d55a8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d55a8-135">System.String</span></span>

## <span data-ttu-id="d55a8-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d55a8-136">OUTPUTS</span></span>

### <span data-ttu-id="d55a8-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d55a8-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d55a8-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d55a8-138">NOTES</span></span>

## <span data-ttu-id="d55a8-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d55a8-139">RELATED LINKS</span></span>
