---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258660"
---
# <span data-ttu-id="c0620-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="c0620-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="c0620-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0620-102">SYNOPSIS</span></span>
<span data-ttu-id="c0620-103">Sparar loggen för körning av distributions skript till disk.</span><span class="sxs-lookup"><span data-stu-id="c0620-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="c0620-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0620-104">SYNTAX</span></span>

### <span data-ttu-id="c0620-105">SaveDeploymentScriptLogByName (standard)</span><span class="sxs-lookup"><span data-stu-id="c0620-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0620-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0620-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0620-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0620-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0620-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0620-108">DESCRIPTION</span></span>
<span data-ttu-id="c0620-109">Med funktionen **Spara-AzDeploymentScriptLog** sparas loggen för körning av distributions skript till disk.</span><span class="sxs-lookup"><span data-stu-id="c0620-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="c0620-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0620-110">EXAMPLES</span></span>

### <span data-ttu-id="c0620-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c0620-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="c0620-112">Sparar loggen för ett distributions skript med det angivna namnet och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c0620-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="c0620-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c0620-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="c0620-114">Sparar de 3 senaste raderna i loggen för ett distributions skript med det angivna namnet och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c0620-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="c0620-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0620-115">PARAMETERS</span></span>

### <span data-ttu-id="c0620-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0620-116">-DefaultProfile</span></span>
<span data-ttu-id="c0620-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0620-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0620-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="c0620-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="c0620-119">PowerShell-objektet distribution script.</span><span class="sxs-lookup"><span data-stu-id="c0620-119">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0620-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="c0620-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="c0620-121">Fullständigt resurs-ID för distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="c0620-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="c0620-122">Exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="c0620-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0620-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c0620-123">-Force</span></span>
<span data-ttu-id="c0620-124">Framtvingar överskrivning av den befintliga filen.</span><span class="sxs-lookup"><span data-stu-id="c0620-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="c0620-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0620-125">-Name</span></span>
<span data-ttu-id="c0620-126">Namnet på distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="c0620-126">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0620-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="c0620-127">-OutputPath</span></span>
<span data-ttu-id="c0620-128">Katalog Sök vägen för att spara distributions skript loggen.</span><span class="sxs-lookup"><span data-stu-id="c0620-128">The directory path to save deployment script log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0620-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0620-129">-ResourceGroupName</span></span>
<span data-ttu-id="c0620-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c0620-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0620-131">-Pilslut</span><span class="sxs-lookup"><span data-stu-id="c0620-131">-Tail</span></span>
<span data-ttu-id="c0620-132">Begränsa utdata till de senaste n raderna</span><span class="sxs-lookup"><span data-stu-id="c0620-132">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0620-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0620-133">-Confirm</span></span>
<span data-ttu-id="c0620-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0620-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0620-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0620-135">-WhatIf</span></span>
<span data-ttu-id="c0620-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0620-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0620-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0620-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0620-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0620-138">CommonParameters</span></span>
<span data-ttu-id="c0620-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0620-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0620-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0620-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0620-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0620-141">INPUTS</span></span>

### <span data-ttu-id="c0620-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c0620-142">System.String</span></span>

## <span data-ttu-id="c0620-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0620-143">OUTPUTS</span></span>

### <span data-ttu-id="c0620-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="c0620-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="c0620-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0620-145">NOTES</span></span>

## <span data-ttu-id="c0620-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0620-146">RELATED LINKS</span></span>
