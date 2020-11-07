---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 8f146c6516226c800f45489e1f7fa5d37173e151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758010"
---
# <span data-ttu-id="e1d23-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e1d23-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="e1d23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1d23-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d23-103">Sparar en mall för distribution av resurs grupper i en fil.</span><span class="sxs-lookup"><span data-stu-id="e1d23-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1d23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1d23-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1d23-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1d23-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d23-106">Cmdleten **Save-AzureRmResourceGroupDeploymentTemplate**  sparar en mall för distribution av resurs grupper i en JSON-fil.</span><span class="sxs-lookup"><span data-stu-id="e1d23-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="e1d23-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1d23-107">EXAMPLES</span></span>

### <span data-ttu-id="e1d23-108">Exempel 1: Spara en distributionsmall</span><span class="sxs-lookup"><span data-stu-id="e1d23-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="e1d23-109">Det här kommandot får distributions mal len från TestDeployment och sparar den som en JSON-fil i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="e1d23-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="e1d23-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1d23-110">PARAMETERS</span></span>

### <span data-ttu-id="e1d23-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e1d23-111">-ApiVersion</span></span>
<span data-ttu-id="e1d23-112">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e1d23-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e1d23-113">Om det inte anges används den senaste API-versionen.</span><span class="sxs-lookup"><span data-stu-id="e1d23-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="e1d23-114">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="e1d23-114">-DeploymentName</span></span>
<span data-ttu-id="e1d23-115">Anger namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="e1d23-115">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="e1d23-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e1d23-116">-Force</span></span>
<span data-ttu-id="e1d23-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e1d23-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1d23-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e1d23-118">-InformationAction</span></span>
<span data-ttu-id="e1d23-119">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="e1d23-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e1d23-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e1d23-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1d23-121">Vidare</span><span class="sxs-lookup"><span data-stu-id="e1d23-121">Continue</span></span>
- <span data-ttu-id="e1d23-122">Över</span><span class="sxs-lookup"><span data-stu-id="e1d23-122">Ignore</span></span>
- <span data-ttu-id="e1d23-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="e1d23-123">Inquire</span></span>
- <span data-ttu-id="e1d23-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e1d23-124">SilentlyContinue</span></span>
- <span data-ttu-id="e1d23-125">Stanna</span><span class="sxs-lookup"><span data-stu-id="e1d23-125">Stop</span></span>
- <span data-ttu-id="e1d23-126">Avbryt</span><span class="sxs-lookup"><span data-stu-id="e1d23-126">Suspend</span></span>

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

### <span data-ttu-id="e1d23-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e1d23-127">-InformationVariable</span></span>
<span data-ttu-id="e1d23-128">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="e1d23-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e1d23-129">-Path</span><span class="sxs-lookup"><span data-stu-id="e1d23-129">-Path</span></span>
<span data-ttu-id="e1d23-130">Anger den utgående sökvägen till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="e1d23-130">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="e1d23-131">-För</span><span class="sxs-lookup"><span data-stu-id="e1d23-131">-Pre</span></span>
<span data-ttu-id="e1d23-132">Anger att denna cmdlet använder för hands versionen av API-versioner när den automatiskt bestämmer vilken API-version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e1d23-132">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="e1d23-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d23-133">-ResourceGroupName</span></span>
<span data-ttu-id="e1d23-134">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e1d23-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e1d23-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e1d23-135">-Confirm</span></span>
<span data-ttu-id="e1d23-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e1d23-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1d23-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1d23-137">-WhatIf</span></span>
<span data-ttu-id="e1d23-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1d23-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1d23-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e1d23-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1d23-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d23-140">-DefaultProfile</span></span>
<span data-ttu-id="e1d23-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d23-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1d23-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d23-142">CommonParameters</span></span>
<span data-ttu-id="e1d23-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d23-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d23-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d23-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d23-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1d23-145">INPUTS</span></span>

## <span data-ttu-id="e1d23-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1d23-146">OUTPUTS</span></span>

### <span data-ttu-id="e1d23-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e1d23-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e1d23-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1d23-148">NOTES</span></span>

## <span data-ttu-id="e1d23-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1d23-149">RELATED LINKS</span></span>

