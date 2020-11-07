---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-Azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 1ffdcef1bb27ec06873c12f64a135adc0e433929
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923790"
---
# <span data-ttu-id="b47d4-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="b47d4-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="b47d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b47d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b47d4-103">Sparar en mall för distribution av resurs grupper i en fil.</span><span class="sxs-lookup"><span data-stu-id="b47d4-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="b47d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b47d4-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b47d4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b47d4-105">DESCRIPTION</span></span>
<span data-ttu-id="b47d4-106">Cmdleten **Save-AzResourceGroupDeploymentTemplate**  sparar en mall för distribution av resurs grupper i en JSON-fil.</span><span class="sxs-lookup"><span data-stu-id="b47d4-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="b47d4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b47d4-107">EXAMPLES</span></span>

### <span data-ttu-id="b47d4-108">Exempel 1: Spara en distributionsmall</span><span class="sxs-lookup"><span data-stu-id="b47d4-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="b47d4-109">Det här kommandot får distributions mal len från TestDeployment och sparar den som en JSON-fil i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="b47d4-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="b47d4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b47d4-110">PARAMETERS</span></span>

### <span data-ttu-id="b47d4-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b47d4-111">-ApiVersion</span></span>
<span data-ttu-id="b47d4-112">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="b47d4-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b47d4-113">Om det inte anges används den senaste API-versionen.</span><span class="sxs-lookup"><span data-stu-id="b47d4-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="b47d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b47d4-114">-DefaultProfile</span></span>
<span data-ttu-id="b47d4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b47d4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b47d4-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="b47d4-116">-DeploymentName</span></span>
<span data-ttu-id="b47d4-117">Anger namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="b47d4-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="b47d4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b47d4-118">-Force</span></span>
<span data-ttu-id="b47d4-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b47d4-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b47d4-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b47d4-120">-InformationAction</span></span>
<span data-ttu-id="b47d4-121">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="b47d4-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="b47d4-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b47d4-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b47d4-123">Vidare</span><span class="sxs-lookup"><span data-stu-id="b47d4-123">Continue</span></span>
- <span data-ttu-id="b47d4-124">Över</span><span class="sxs-lookup"><span data-stu-id="b47d4-124">Ignore</span></span>
- <span data-ttu-id="b47d4-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="b47d4-125">Inquire</span></span>
- <span data-ttu-id="b47d4-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b47d4-126">SilentlyContinue</span></span>
- <span data-ttu-id="b47d4-127">Stanna</span><span class="sxs-lookup"><span data-stu-id="b47d4-127">Stop</span></span>
- <span data-ttu-id="b47d4-128">Avbryt</span><span class="sxs-lookup"><span data-stu-id="b47d4-128">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b47d4-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b47d4-129">-InformationVariable</span></span>
<span data-ttu-id="b47d4-130">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="b47d4-130">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b47d4-131">-Path</span><span class="sxs-lookup"><span data-stu-id="b47d4-131">-Path</span></span>
<span data-ttu-id="b47d4-132">Anger den utgående sökvägen till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="b47d4-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="b47d4-133">-För</span><span class="sxs-lookup"><span data-stu-id="b47d4-133">-Pre</span></span>
<span data-ttu-id="b47d4-134">Anger att denna cmdlet använder för hands versionen av API-versioner när den automatiskt bestämmer vilken API-version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="b47d4-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="b47d4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b47d4-135">-ResourceGroupName</span></span>
<span data-ttu-id="b47d4-136">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b47d4-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b47d4-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b47d4-137">-Confirm</span></span>
<span data-ttu-id="b47d4-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b47d4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b47d4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b47d4-139">-WhatIf</span></span>
<span data-ttu-id="b47d4-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b47d4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b47d4-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b47d4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b47d4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b47d4-142">CommonParameters</span></span>
<span data-ttu-id="b47d4-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b47d4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b47d4-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b47d4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b47d4-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b47d4-145">INPUTS</span></span>

## <span data-ttu-id="b47d4-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b47d4-146">OUTPUTS</span></span>

## <span data-ttu-id="b47d4-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b47d4-147">NOTES</span></span>

## <span data-ttu-id="b47d4-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b47d4-148">RELATED LINKS</span></span>
