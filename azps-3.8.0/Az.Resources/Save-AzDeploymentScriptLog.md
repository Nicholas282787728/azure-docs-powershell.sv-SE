---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 4e32726b3e7af6608092d29fd52f7a41be042d42
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089513"
---
# <span data-ttu-id="c90ae-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="c90ae-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="c90ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c90ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c90ae-103">Sparar loggen för körning av distributions skript till disk.</span><span class="sxs-lookup"><span data-stu-id="c90ae-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="c90ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c90ae-104">SYNTAX</span></span>

### <span data-ttu-id="c90ae-105">SaveDeploymentScriptLogByName (standard)</span><span class="sxs-lookup"><span data-stu-id="c90ae-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c90ae-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="c90ae-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c90ae-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="c90ae-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c90ae-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c90ae-108">DESCRIPTION</span></span>
<span data-ttu-id="c90ae-109">Med funktionen **Spara-AzDeploymentScriptLog** sparas loggen för körning av distributions skript till disk.</span><span class="sxs-lookup"><span data-stu-id="c90ae-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="c90ae-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c90ae-110">EXAMPLES</span></span>

### <span data-ttu-id="c90ae-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c90ae-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="c90ae-112">Sparar loggen för ett distributions skript med det angivna namnet och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c90ae-112">Saves the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="c90ae-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c90ae-113">PARAMETERS</span></span>

### <span data-ttu-id="c90ae-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c90ae-114">-Confirm</span></span>
<span data-ttu-id="c90ae-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c90ae-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c90ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c90ae-116">-DefaultProfile</span></span>
<span data-ttu-id="c90ae-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c90ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c90ae-118">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="c90ae-118">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="c90ae-119">PowerShell-objektet distribution script.</span><span class="sxs-lookup"><span data-stu-id="c90ae-119">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c90ae-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="c90ae-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="c90ae-121">Fullständigt resurs-ID för distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="c90ae-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="c90ae-122">Exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="c90ae-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90ae-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c90ae-123">-Force</span></span>
<span data-ttu-id="c90ae-124">Framtvingar överskrivning av den befintliga filen.</span><span class="sxs-lookup"><span data-stu-id="c90ae-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="c90ae-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="c90ae-125">-Name</span></span>
<span data-ttu-id="c90ae-126">Namnet på distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="c90ae-126">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90ae-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="c90ae-127">-OutputPath</span></span>
<span data-ttu-id="c90ae-128">Katalog Sök vägen för att spara distributions skript loggen.</span><span class="sxs-lookup"><span data-stu-id="c90ae-128">The directory path to save deployment script log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c90ae-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c90ae-129">-ResourceGroupName</span></span>
<span data-ttu-id="c90ae-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c90ae-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90ae-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c90ae-131">-WhatIf</span></span>
<span data-ttu-id="c90ae-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c90ae-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c90ae-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c90ae-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c90ae-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c90ae-134">CommonParameters</span></span>
<span data-ttu-id="c90ae-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c90ae-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c90ae-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c90ae-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c90ae-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c90ae-137">INPUTS</span></span>

### <span data-ttu-id="c90ae-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c90ae-138">System.String</span></span>

## <span data-ttu-id="c90ae-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c90ae-139">OUTPUTS</span></span>

### <span data-ttu-id="c90ae-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="c90ae-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="c90ae-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c90ae-141">NOTES</span></span>

## <span data-ttu-id="c90ae-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c90ae-142">RELATED LINKS</span></span>
