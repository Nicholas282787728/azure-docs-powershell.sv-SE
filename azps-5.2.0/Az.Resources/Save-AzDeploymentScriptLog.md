---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410067"
---
# <span data-ttu-id="9bf2b-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="9bf2b-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="9bf2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9bf2b-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf2b-103">Sparar loggen för körning av distributions skript till disk.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="9bf2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9bf2b-104">SYNTAX</span></span>

### <span data-ttu-id="9bf2b-105">SaveDeploymentScriptLogByName (standard)</span><span class="sxs-lookup"><span data-stu-id="9bf2b-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bf2b-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="9bf2b-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bf2b-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="9bf2b-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9bf2b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9bf2b-108">DESCRIPTION</span></span>
<span data-ttu-id="9bf2b-109">Med funktionen **Spara-AzDeploymentScriptLog** sparas loggen för körning av distributions skript till disk.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="9bf2b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9bf2b-110">EXAMPLES</span></span>

### <span data-ttu-id="9bf2b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9bf2b-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="9bf2b-112">Sparar loggen för ett distributions skript med det angivna namnet och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="9bf2b-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9bf2b-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="9bf2b-114">Sparar de 3 senaste raderna i loggen för ett distributions skript med det angivna namnet och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="9bf2b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9bf2b-115">PARAMETERS</span></span>

### <span data-ttu-id="9bf2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf2b-116">-DefaultProfile</span></span>
<span data-ttu-id="9bf2b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bf2b-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="9bf2b-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="9bf2b-119">PowerShell-objektet distribution script.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-119">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="9bf2b-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="9bf2b-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="9bf2b-121">Fullständigt resurs-ID för distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="9bf2b-122">Exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="9bf2b-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="9bf2b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9bf2b-123">-Force</span></span>
<span data-ttu-id="9bf2b-124">Framtvingar överskrivning av den befintliga filen.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="9bf2b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="9bf2b-125">-Name</span></span>
<span data-ttu-id="9bf2b-126">Namnet på distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-126">The name of the deployment script.</span></span>

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

### <span data-ttu-id="9bf2b-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="9bf2b-127">-OutputPath</span></span>
<span data-ttu-id="9bf2b-128">Katalog Sök vägen för att spara distributions skript loggen.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-128">The directory path to save deployment script log.</span></span>

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

### <span data-ttu-id="9bf2b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf2b-129">-ResourceGroupName</span></span>
<span data-ttu-id="9bf2b-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="9bf2b-131">-Pilslut</span><span class="sxs-lookup"><span data-stu-id="9bf2b-131">-Tail</span></span>
<span data-ttu-id="9bf2b-132">Begränsa utdata till de senaste n raderna</span><span class="sxs-lookup"><span data-stu-id="9bf2b-132">Limit output to last n lines</span></span>

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

### <span data-ttu-id="9bf2b-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9bf2b-133">-Confirm</span></span>
<span data-ttu-id="9bf2b-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bf2b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bf2b-135">-WhatIf</span></span>
<span data-ttu-id="9bf2b-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bf2b-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bf2b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf2b-138">CommonParameters</span></span>
<span data-ttu-id="9bf2b-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf2b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf2b-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bf2b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf2b-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9bf2b-141">INPUTS</span></span>

### <span data-ttu-id="9bf2b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9bf2b-142">System.String</span></span>

## <span data-ttu-id="9bf2b-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9bf2b-143">OUTPUTS</span></span>

### <span data-ttu-id="9bf2b-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="9bf2b-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="9bf2b-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9bf2b-145">NOTES</span></span>

## <span data-ttu-id="9bf2b-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9bf2b-146">RELATED LINKS</span></span>
