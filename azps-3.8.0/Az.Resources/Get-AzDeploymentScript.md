---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 761969eea685c21bc513efdfde9ea79a9e1e4a70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090050"
---
# <span data-ttu-id="13e08-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="13e08-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="13e08-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13e08-102">SYNOPSIS</span></span>
<span data-ttu-id="13e08-103">Hämtar eller visar distributions skript.</span><span class="sxs-lookup"><span data-stu-id="13e08-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="13e08-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13e08-104">SYNTAX</span></span>

### <span data-ttu-id="13e08-105">ListDeploymentScript (standard)</span><span class="sxs-lookup"><span data-stu-id="13e08-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13e08-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="13e08-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13e08-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="13e08-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13e08-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13e08-108">DESCRIPTION</span></span>
<span data-ttu-id="13e08-109">Cmdleten **Get-AzDeploymentScript** hämtar ett enskilt distributions skript eller en lista med distributions skript.</span><span class="sxs-lookup"><span data-stu-id="13e08-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="13e08-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13e08-110">EXAMPLES</span></span>

### <span data-ttu-id="13e08-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="13e08-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="13e08-112">Visar en lista över distributions skript i prenumerationen i den aktuella användarens kontext.</span><span class="sxs-lookup"><span data-stu-id="13e08-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="13e08-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="13e08-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="13e08-114">Visar distributions skript i resurs gruppen DS-TestRg.</span><span class="sxs-lookup"><span data-stu-id="13e08-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="13e08-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="13e08-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="13e08-116">Hämtar ett distributions skript med namnet MyDeploymentScript i resurs gruppen DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="13e08-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="13e08-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="13e08-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="13e08-118">Hämtar ett distributions skript med angivet resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="13e08-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="13e08-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13e08-119">PARAMETERS</span></span>

### <span data-ttu-id="13e08-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13e08-120">-DefaultProfile</span></span>
<span data-ttu-id="13e08-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13e08-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13e08-122">-ID</span><span class="sxs-lookup"><span data-stu-id="13e08-122">-Id</span></span>
<span data-ttu-id="13e08-123">Fullständigt resurs-ID för distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="13e08-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="13e08-124">Exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="13e08-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13e08-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="13e08-125">-Name</span></span>
<span data-ttu-id="13e08-126">Namnet på distributions skriptet</span><span class="sxs-lookup"><span data-stu-id="13e08-126">The name of the deployment script</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13e08-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13e08-127">-ResourceGroupName</span></span>
<span data-ttu-id="13e08-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="13e08-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListDeploymentScript
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13e08-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e08-129">CommonParameters</span></span>
<span data-ttu-id="13e08-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13e08-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="13e08-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13e08-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e08-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13e08-132">INPUTS</span></span>

### <span data-ttu-id="13e08-133">System. String</span><span class="sxs-lookup"><span data-stu-id="13e08-133">System.String</span></span>

## <span data-ttu-id="13e08-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13e08-134">OUTPUTS</span></span>

### <span data-ttu-id="13e08-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="13e08-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="13e08-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13e08-136">NOTES</span></span>

## <span data-ttu-id="13e08-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13e08-137">RELATED LINKS</span></span>
