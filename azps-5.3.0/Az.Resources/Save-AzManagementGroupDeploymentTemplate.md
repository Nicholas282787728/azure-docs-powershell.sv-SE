---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: f45602ad2515a90e39e45edb80ca1cb0bf051f00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423664"
---
# <span data-ttu-id="19897-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="19897-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="19897-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19897-102">SYNOPSIS</span></span>
<span data-ttu-id="19897-103">Sparar en distributionsmall till en fil.</span><span class="sxs-lookup"><span data-stu-id="19897-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="19897-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19897-104">SYNTAX</span></span>

### <span data-ttu-id="19897-105">SaveByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="19897-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19897-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="19897-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19897-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19897-107">DESCRIPTION</span></span>
<span data-ttu-id="19897-108">Cmdleten **Save-AzManagementGroupDeploymentTemplate**  sparar en distributionsmall till en JSON-fil för en distribution i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="19897-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="19897-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19897-109">EXAMPLES</span></span>

### <span data-ttu-id="19897-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="19897-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="19897-111">Det här kommandot får distributions mal len från TestDeployment och sparar den som en JSON-fil i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="19897-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="19897-112">Exempel 2: Hämta en distribution och spara dess mall</span><span class="sxs-lookup"><span data-stu-id="19897-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="19897-113">Det här kommandot får distributionen "RolesDeployment" i hanterings gruppen "myMG" och sparar dess mall.</span><span class="sxs-lookup"><span data-stu-id="19897-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="19897-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19897-114">PARAMETERS</span></span>

### <span data-ttu-id="19897-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19897-115">-DefaultProfile</span></span>
<span data-ttu-id="19897-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="19897-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19897-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="19897-117">-DeploymentName</span></span>
<span data-ttu-id="19897-118">Distributions namn.</span><span class="sxs-lookup"><span data-stu-id="19897-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19897-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="19897-119">-DeploymentObject</span></span>
<span data-ttu-id="19897-120">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="19897-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19897-121">-Force</span><span class="sxs-lookup"><span data-stu-id="19897-121">-Force</span></span>
<span data-ttu-id="19897-122">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="19897-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="19897-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="19897-123">-ManagementGroupId</span></span>
<span data-ttu-id="19897-124">Hanterings gruppens ID.</span><span class="sxs-lookup"><span data-stu-id="19897-124">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19897-125">-Path</span><span class="sxs-lookup"><span data-stu-id="19897-125">-Path</span></span>
<span data-ttu-id="19897-126">Utgångs Sök vägen för mallfilen.</span><span class="sxs-lookup"><span data-stu-id="19897-126">The output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19897-127">-För</span><span class="sxs-lookup"><span data-stu-id="19897-127">-Pre</span></span>
<span data-ttu-id="19897-128">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="19897-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="19897-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="19897-129">-Confirm</span></span>
<span data-ttu-id="19897-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="19897-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19897-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19897-131">-WhatIf</span></span>
<span data-ttu-id="19897-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="19897-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19897-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="19897-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19897-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19897-134">CommonParameters</span></span>
<span data-ttu-id="19897-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19897-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19897-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19897-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19897-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19897-137">INPUTS</span></span>

### <span data-ttu-id="19897-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="19897-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="19897-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19897-139">OUTPUTS</span></span>

### <span data-ttu-id="19897-140">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="19897-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="19897-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19897-141">NOTES</span></span>

## <span data-ttu-id="19897-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19897-142">RELATED LINKS</span></span>
