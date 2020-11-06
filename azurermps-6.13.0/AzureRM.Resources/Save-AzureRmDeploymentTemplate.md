---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmDeploymentTemplate.md
ms.openlocfilehash: ed9309599b83079858d02fddeffe7dad4b3bb2dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583987"
---
# <span data-ttu-id="ea0e8-101">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="ea0e8-101">Save-AzureRmDeploymentTemplate</span></span>

## <span data-ttu-id="ea0e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea0e8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0e8-103">Sparar en distributionsmall till en fil.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-103">Saves a deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea0e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea0e8-104">SYNTAX</span></span>

### <span data-ttu-id="ea0e8-105">SaveByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="ea0e8-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzureRmDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea0e8-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="ea0e8-106">SaveByDeploymentObject</span></span>
```
Save-AzureRmDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea0e8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea0e8-107">DESCRIPTION</span></span>
<span data-ttu-id="ea0e8-108">Cmdleten **Save-AzureRmDeploymentTemplate**  sparar en distributionsmall till en JSON-fil.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-108">The **Save-AzureRmDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="ea0e8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea0e8-109">EXAMPLES</span></span>

### <span data-ttu-id="ea0e8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ea0e8-110">Example 1</span></span>
```powershell
PS C:\> Save-AzureRmDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="ea0e8-111">Det här kommandot får distributions mal len från TestDeployment och sparar den som en JSON-fil i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="ea0e8-112">Exempel 2: Hämta en distribution och spara dess mall</span><span class="sxs-lookup"><span data-stu-id="ea0e8-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "RolesDeployment" | Save-AzureRmDeploymentTemplate
```

<span data-ttu-id="ea0e8-113">Det här kommandot får distributionen "RolesDeployment" vid den aktuella prenumerations omfattningen och sparar mallen.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="ea0e8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea0e8-114">PARAMETERS</span></span>

### <span data-ttu-id="ea0e8-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ea0e8-115">-ApiVersion</span></span>
<span data-ttu-id="ea0e8-116">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ea0e8-117">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0e8-118">-DefaultProfile</span></span>
<span data-ttu-id="ea0e8-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0e8-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="ea0e8-120">-DeploymentName</span></span>
<span data-ttu-id="ea0e8-121">Distributions namn.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0e8-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="ea0e8-122">-DeploymentObject</span></span>
<span data-ttu-id="ea0e8-123">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0e8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ea0e8-124">-Force</span></span>
<span data-ttu-id="ea0e8-125">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ea0e8-126">-Path</span><span class="sxs-lookup"><span data-stu-id="ea0e8-126">-Path</span></span>
<span data-ttu-id="ea0e8-127">Utgångs Sök vägen för mallfilen.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-127">The output path of the template file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0e8-128">-För</span><span class="sxs-lookup"><span data-stu-id="ea0e8-128">-Pre</span></span>
<span data-ttu-id="ea0e8-129">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ea0e8-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea0e8-130">-Confirm</span></span>
<span data-ttu-id="ea0e8-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea0e8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea0e8-132">-WhatIf</span></span>
<span data-ttu-id="ea0e8-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea0e8-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea0e8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0e8-135">CommonParameters</span></span>
<span data-ttu-id="ea0e8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea0e8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0e8-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea0e8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0e8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea0e8-138">INPUTS</span></span>

### <span data-ttu-id="ea0e8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ea0e8-139">System.String</span></span>

## <span data-ttu-id="ea0e8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea0e8-140">OUTPUTS</span></span>

### <span data-ttu-id="ea0e8-141">Microsoft. Azure. commands. ResourceManager. cmdlets. SdkModels</span><span class="sxs-lookup"><span data-stu-id="ea0e8-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels</span></span>

## <span data-ttu-id="ea0e8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea0e8-142">NOTES</span></span>

## <span data-ttu-id="ea0e8-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea0e8-143">RELATED LINKS</span></span>
