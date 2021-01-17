---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: dc6f7c5b66d72ae5c01ecbb8ec93fa737199d06e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423688"
---
# <span data-ttu-id="d37b9-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d37b9-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="d37b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d37b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d37b9-103">Sparar en distributionsmall till en fil.</span><span class="sxs-lookup"><span data-stu-id="d37b9-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="d37b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d37b9-104">SYNTAX</span></span>

### <span data-ttu-id="d37b9-105">SaveByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="d37b9-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d37b9-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d37b9-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d37b9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d37b9-107">DESCRIPTION</span></span>
<span data-ttu-id="d37b9-108">Cmdleten **Save-AzDeploymentTemplate**  sparar en distributionsmall till en JSON-fil.</span><span class="sxs-lookup"><span data-stu-id="d37b9-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="d37b9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d37b9-109">EXAMPLES</span></span>

### <span data-ttu-id="d37b9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d37b9-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="d37b9-111">Det här kommandot får distributions mal len från TestDeployment och sparar den som en JSON-fil i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="d37b9-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="d37b9-112">Exempel 2: Hämta en distribution och spara dess mall</span><span class="sxs-lookup"><span data-stu-id="d37b9-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="d37b9-113">Det här kommandot får distributionen "RolesDeployment" vid den aktuella prenumerations omfattningen och sparar mallen.</span><span class="sxs-lookup"><span data-stu-id="d37b9-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="d37b9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d37b9-114">PARAMETERS</span></span>

### <span data-ttu-id="d37b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37b9-115">-DefaultProfile</span></span>
<span data-ttu-id="d37b9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d37b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d37b9-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d37b9-117">-DeploymentName</span></span>
<span data-ttu-id="d37b9-118">Distributions namn.</span><span class="sxs-lookup"><span data-stu-id="d37b9-118">The deployment name.</span></span>

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

### <span data-ttu-id="d37b9-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d37b9-119">-DeploymentObject</span></span>
<span data-ttu-id="d37b9-120">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="d37b9-120">The deployment object.</span></span>

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

### <span data-ttu-id="d37b9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d37b9-121">-Force</span></span>
<span data-ttu-id="d37b9-122">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d37b9-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d37b9-123">-Path</span><span class="sxs-lookup"><span data-stu-id="d37b9-123">-Path</span></span>
<span data-ttu-id="d37b9-124">Utgångs Sök vägen för mallfilen.</span><span class="sxs-lookup"><span data-stu-id="d37b9-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="d37b9-125">-För</span><span class="sxs-lookup"><span data-stu-id="d37b9-125">-Pre</span></span>
<span data-ttu-id="d37b9-126">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d37b9-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d37b9-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d37b9-127">-Confirm</span></span>
<span data-ttu-id="d37b9-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d37b9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d37b9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37b9-129">-WhatIf</span></span>
<span data-ttu-id="d37b9-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d37b9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d37b9-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d37b9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d37b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37b9-132">CommonParameters</span></span>
<span data-ttu-id="d37b9-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37b9-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d37b9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37b9-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d37b9-135">INPUTS</span></span>

### <span data-ttu-id="d37b9-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d37b9-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d37b9-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d37b9-137">OUTPUTS</span></span>

### <span data-ttu-id="d37b9-138">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="d37b9-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="d37b9-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d37b9-139">NOTES</span></span>

## <span data-ttu-id="d37b9-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d37b9-140">RELATED LINKS</span></span>
