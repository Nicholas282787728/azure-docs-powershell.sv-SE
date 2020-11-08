---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: dcee9317e6aad113088dc3498a337e16e61b6320
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273040"
---
# <span data-ttu-id="9bc01-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="9bc01-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="9bc01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9bc01-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc01-103">Sparar en distributionsmall till en fil.</span><span class="sxs-lookup"><span data-stu-id="9bc01-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="9bc01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9bc01-104">SYNTAX</span></span>

### <span data-ttu-id="9bc01-105">SaveByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="9bc01-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bc01-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="9bc01-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bc01-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9bc01-107">DESCRIPTION</span></span>
<span data-ttu-id="9bc01-108">Cmdleten **Save-AzTenantDeploymentTemplate**  sparar en distributionsmall till en JSON-fil för en distribution med klient omfattning.</span><span class="sxs-lookup"><span data-stu-id="9bc01-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="9bc01-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9bc01-109">EXAMPLES</span></span>

### <span data-ttu-id="9bc01-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9bc01-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="9bc01-111">Det här kommandot får distributions mal len från TestDeployment och sparar den som en JSON-fil i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="9bc01-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="9bc01-112">Exempel 2: Hämta en distribution och spara dess mall</span><span class="sxs-lookup"><span data-stu-id="9bc01-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="9bc01-113">Det här kommandot får distributionen "RolesDeployment" vid den aktuella klient organisations omfattningen och sparar mallen.</span><span class="sxs-lookup"><span data-stu-id="9bc01-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="9bc01-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9bc01-114">PARAMETERS</span></span>

### <span data-ttu-id="9bc01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc01-115">-DefaultProfile</span></span>
<span data-ttu-id="9bc01-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9bc01-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bc01-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="9bc01-117">-DeploymentName</span></span>
<span data-ttu-id="9bc01-118">Distributions namn.</span><span class="sxs-lookup"><span data-stu-id="9bc01-118">The deployment name.</span></span>

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

### <span data-ttu-id="9bc01-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="9bc01-119">-DeploymentObject</span></span>
<span data-ttu-id="9bc01-120">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="9bc01-120">The deployment object.</span></span>

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

### <span data-ttu-id="9bc01-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9bc01-121">-Force</span></span>
<span data-ttu-id="9bc01-122">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9bc01-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9bc01-123">-Path</span><span class="sxs-lookup"><span data-stu-id="9bc01-123">-Path</span></span>
<span data-ttu-id="9bc01-124">Utgångs Sök vägen för mallfilen.</span><span class="sxs-lookup"><span data-stu-id="9bc01-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="9bc01-125">-För</span><span class="sxs-lookup"><span data-stu-id="9bc01-125">-Pre</span></span>
<span data-ttu-id="9bc01-126">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="9bc01-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9bc01-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9bc01-127">-Confirm</span></span>
<span data-ttu-id="9bc01-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9bc01-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bc01-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bc01-129">-WhatIf</span></span>
<span data-ttu-id="9bc01-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9bc01-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bc01-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9bc01-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bc01-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc01-132">CommonParameters</span></span>
<span data-ttu-id="9bc01-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bc01-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc01-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bc01-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc01-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9bc01-135">INPUTS</span></span>

### <span data-ttu-id="9bc01-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="9bc01-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="9bc01-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9bc01-137">OUTPUTS</span></span>

### <span data-ttu-id="9bc01-138">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="9bc01-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="9bc01-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9bc01-139">NOTES</span></span>

## <span data-ttu-id="9bc01-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9bc01-140">RELATED LINKS</span></span>
