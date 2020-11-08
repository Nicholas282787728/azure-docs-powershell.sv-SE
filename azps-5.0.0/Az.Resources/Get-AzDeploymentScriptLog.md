---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 608450112b7cd4f54ee0f08f0f29c3aa707fff9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269132"
---
# <span data-ttu-id="a2488-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="a2488-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="a2488-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2488-102">SYNOPSIS</span></span>
<span data-ttu-id="a2488-103">Hämtar loggen för ett distributions skript.</span><span class="sxs-lookup"><span data-stu-id="a2488-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="a2488-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2488-104">SYNTAX</span></span>

### <span data-ttu-id="a2488-105">GetDeploymentScriptLogByName (standard)</span><span class="sxs-lookup"><span data-stu-id="a2488-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2488-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2488-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2488-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="a2488-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2488-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2488-108">DESCRIPTION</span></span>
<span data-ttu-id="a2488-109">Cmdleten **Get-AzDeploymentScriptLog** hämtar loggen för en körning av distributions skript.</span><span class="sxs-lookup"><span data-stu-id="a2488-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="a2488-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2488-110">EXAMPLES</span></span>

### <span data-ttu-id="a2488-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a2488-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="a2488-112">Hämtar loggen för ett distributions skript med namnet MyDeploymentScript i resurs gruppen DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="a2488-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="a2488-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a2488-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="a2488-114">Hämtar de sista 3 raderna i loggen för ett distributions skript med namnet MyDeploymentScript i resurs gruppen DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="a2488-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="a2488-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a2488-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="a2488-116">Det första kommandot får ett distributions skript med namnet MyDeploymentScript i resurs gruppen DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="a2488-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="a2488-117">Det andra kommandot får loggen för det angivna distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="a2488-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="a2488-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2488-118">PARAMETERS</span></span>

### <span data-ttu-id="a2488-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2488-119">-DefaultProfile</span></span>
<span data-ttu-id="a2488-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2488-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2488-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="a2488-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="a2488-122">PowerShell-objektet distribution script.</span><span class="sxs-lookup"><span data-stu-id="a2488-122">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2488-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="a2488-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="a2488-124">Fullständigt resurs-ID för distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="a2488-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="a2488-125">Exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="a2488-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2488-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="a2488-126">-Name</span></span>
<span data-ttu-id="a2488-127">Namnet på distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="a2488-127">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2488-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2488-128">-ResourceGroupName</span></span>
<span data-ttu-id="a2488-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a2488-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2488-130">-Pilslut</span><span class="sxs-lookup"><span data-stu-id="a2488-130">-Tail</span></span>
<span data-ttu-id="a2488-131">Begränsa utdata till de senaste n raderna</span><span class="sxs-lookup"><span data-stu-id="a2488-131">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2488-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2488-132">CommonParameters</span></span>
<span data-ttu-id="a2488-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2488-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2488-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2488-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2488-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2488-135">INPUTS</span></span>

### <span data-ttu-id="a2488-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a2488-136">System.String</span></span>

### <span data-ttu-id="a2488-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="a2488-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="a2488-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2488-138">OUTPUTS</span></span>

### <span data-ttu-id="a2488-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="a2488-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="a2488-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2488-140">NOTES</span></span>

## <span data-ttu-id="a2488-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2488-141">RELATED LINKS</span></span>
