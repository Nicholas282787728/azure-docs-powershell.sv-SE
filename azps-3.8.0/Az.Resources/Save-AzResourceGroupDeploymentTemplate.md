---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 7d5d5ecc0f8facf03be72f952722ea30b56fa9ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089467"
---
# <span data-ttu-id="4c0fb-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="4c0fb-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="4c0fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c0fb-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0fb-103">Sparar en mall för distribution av resurs grupper i en fil.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="4c0fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c0fb-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c0fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c0fb-105">DESCRIPTION</span></span>
<span data-ttu-id="4c0fb-106">Cmdleten **Save-AzResourceGroupDeploymentTemplate**  sparar en mall för distribution av resurs grupper i en JSON-fil.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="4c0fb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c0fb-107">EXAMPLES</span></span>

### <span data-ttu-id="4c0fb-108">Exempel 1: Spara en distributionsmall</span><span class="sxs-lookup"><span data-stu-id="4c0fb-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="4c0fb-109">Det här kommandot får distributions mal len från TestDeployment och sparar den som en JSON-fil i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="4c0fb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c0fb-110">PARAMETERS</span></span>

### <span data-ttu-id="4c0fb-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4c0fb-111">-ApiVersion</span></span>
<span data-ttu-id="4c0fb-112">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4c0fb-113">Om det inte anges används den senaste API-versionen.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="4c0fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0fb-114">-DefaultProfile</span></span>
<span data-ttu-id="4c0fb-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4c0fb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c0fb-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="4c0fb-116">-DeploymentName</span></span>
<span data-ttu-id="4c0fb-117">Anger namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-117">Specifies the name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0fb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4c0fb-118">-Force</span></span>
<span data-ttu-id="4c0fb-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4c0fb-120">-Path</span><span class="sxs-lookup"><span data-stu-id="4c0fb-120">-Path</span></span>
<span data-ttu-id="4c0fb-121">Anger den utgående sökvägen till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-121">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0fb-122">-För</span><span class="sxs-lookup"><span data-stu-id="4c0fb-122">-Pre</span></span>
<span data-ttu-id="4c0fb-123">Anger att denna cmdlet använder för hands versionen av API-versioner när den automatiskt bestämmer vilken API-version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-123">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="4c0fb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c0fb-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c0fb-125">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-125">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0fb-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4c0fb-126">-Confirm</span></span>
<span data-ttu-id="4c0fb-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0fb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c0fb-128">-WhatIf</span></span>
<span data-ttu-id="4c0fb-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c0fb-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0fb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0fb-131">CommonParameters</span></span>
<span data-ttu-id="4c0fb-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c0fb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0fb-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c0fb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0fb-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c0fb-134">INPUTS</span></span>

### <span data-ttu-id="4c0fb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4c0fb-135">System.String</span></span>

## <span data-ttu-id="4c0fb-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c0fb-136">OUTPUTS</span></span>

### <span data-ttu-id="4c0fb-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4c0fb-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4c0fb-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c0fb-138">NOTES</span></span>

## <span data-ttu-id="4c0fb-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c0fb-139">RELATED LINKS</span></span>
