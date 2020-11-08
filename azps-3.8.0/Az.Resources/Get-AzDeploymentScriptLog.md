---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 855127362fbcbf906755affde0bec6de5e7f2698
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092045"
---
# <span data-ttu-id="1f631-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="1f631-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="1f631-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f631-102">SYNOPSIS</span></span>
<span data-ttu-id="1f631-103">Hämtar loggen för ett distributions skript.</span><span class="sxs-lookup"><span data-stu-id="1f631-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="1f631-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f631-104">SYNTAX</span></span>

### <span data-ttu-id="1f631-105">GetDeploymentScriptLogByName (standard)</span><span class="sxs-lookup"><span data-stu-id="1f631-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f631-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f631-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f631-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="1f631-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f631-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f631-108">DESCRIPTION</span></span>
<span data-ttu-id="1f631-109">Cmdleten **Get-AzDeploymentScriptLog** hämtar loggen för en körning av distributions skript.</span><span class="sxs-lookup"><span data-stu-id="1f631-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="1f631-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f631-110">EXAMPLES</span></span>

### <span data-ttu-id="1f631-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1f631-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="1f631-112">Loggar in ett distributions skript med namnet MyDeploymentScript i resurs gruppen DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="1f631-112">Gets log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="1f631-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1f631-113">Example 2</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="1f631-114">Det första kommandot får ett distributions skript med namnet MyDeploymentScript i resurs gruppen DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="1f631-114">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="1f631-115">Det andra kommandot får loggen för det angivna distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="1f631-115">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="1f631-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f631-116">PARAMETERS</span></span>

### <span data-ttu-id="1f631-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f631-117">-DefaultProfile</span></span>
<span data-ttu-id="1f631-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f631-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f631-119">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="1f631-119">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="1f631-120">PowerShell-objektet distribution script.</span><span class="sxs-lookup"><span data-stu-id="1f631-120">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f631-121">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="1f631-121">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="1f631-122">Fullständigt resurs-ID för distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="1f631-122">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="1f631-123">Exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="1f631-123">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f631-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f631-124">-Name</span></span>
<span data-ttu-id="1f631-125">Namnet på distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="1f631-125">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f631-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f631-126">-ResourceGroupName</span></span>
<span data-ttu-id="1f631-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1f631-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f631-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f631-128">CommonParameters</span></span>
<span data-ttu-id="1f631-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f631-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1f631-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f631-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f631-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f631-131">INPUTS</span></span>

### <span data-ttu-id="1f631-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1f631-132">System.String</span></span>

### <span data-ttu-id="1f631-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="1f631-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="1f631-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f631-134">OUTPUTS</span></span>

### <span data-ttu-id="1f631-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="1f631-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="1f631-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f631-136">NOTES</span></span>

## <span data-ttu-id="1f631-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f631-137">RELATED LINKS</span></span>
