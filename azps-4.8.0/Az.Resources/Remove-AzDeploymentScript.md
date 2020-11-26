---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 9904dc21f4c37c36684d2c74e97486c1a516aa88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260408"
---
# <span data-ttu-id="447da-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="447da-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="447da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="447da-102">SYNOPSIS</span></span>
<span data-ttu-id="447da-103">Tar bort ett distributions skript och dess associerade resurser.</span><span class="sxs-lookup"><span data-stu-id="447da-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="447da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="447da-104">SYNTAX</span></span>

### <span data-ttu-id="447da-105">RemoveDeploymentScriptLogByName (standard)</span><span class="sxs-lookup"><span data-stu-id="447da-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="447da-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="447da-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="447da-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="447da-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="447da-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="447da-108">DESCRIPTION</span></span>
<span data-ttu-id="447da-109">Cmdleten **Remove-AzDeploymentScript** tar bort ett distributions skript och dess associerade resurser.</span><span class="sxs-lookup"><span data-stu-id="447da-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="447da-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="447da-110">EXAMPLES</span></span>

### <span data-ttu-id="447da-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="447da-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="447da-112">Tar bort ett distributions skript med namnet MyDeploymentScript i resurs gruppen DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="447da-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="447da-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="447da-113">PARAMETERS</span></span>

### <span data-ttu-id="447da-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="447da-114">-Confirm</span></span>
<span data-ttu-id="447da-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="447da-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="447da-116">-DefaultProfile</span></span>
<span data-ttu-id="447da-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="447da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="447da-118">-ID</span><span class="sxs-lookup"><span data-stu-id="447da-118">-Id</span></span>
<span data-ttu-id="447da-119">Fullständigt resurs-ID för distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="447da-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="447da-120">Exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="447da-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="447da-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="447da-121">-InputObject</span></span>
<span data-ttu-id="447da-122">PowerShell-objektet distribution script.</span><span class="sxs-lookup"><span data-stu-id="447da-122">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: RemoveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="447da-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="447da-123">-Name</span></span>
<span data-ttu-id="447da-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="447da-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="447da-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="447da-125">-PassThru</span></span>
<span data-ttu-id="447da-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="447da-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="447da-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="447da-127">-ResourceGroupName</span></span>
<span data-ttu-id="447da-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="447da-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="447da-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="447da-129">-WhatIf</span></span>
<span data-ttu-id="447da-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="447da-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="447da-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="447da-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447da-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="447da-132">CommonParameters</span></span>
<span data-ttu-id="447da-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="447da-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="447da-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="447da-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="447da-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="447da-135">INPUTS</span></span>

### <span data-ttu-id="447da-136">System. String</span><span class="sxs-lookup"><span data-stu-id="447da-136">System.String</span></span>

### <span data-ttu-id="447da-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="447da-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="447da-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="447da-138">OUTPUTS</span></span>

### <span data-ttu-id="447da-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="447da-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="447da-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="447da-140">NOTES</span></span>

## <span data-ttu-id="447da-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="447da-141">RELATED LINKS</span></span>