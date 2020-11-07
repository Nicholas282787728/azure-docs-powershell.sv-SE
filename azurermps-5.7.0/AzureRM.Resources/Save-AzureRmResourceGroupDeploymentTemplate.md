---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 2be6deeca64a8d167231cf7afe3b84b60f6e6c68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757234"
---
# <span data-ttu-id="34558-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="34558-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="34558-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34558-102">SYNOPSIS</span></span>
<span data-ttu-id="34558-103">Sparar en mall för distribution av resurs grupper i en fil.</span><span class="sxs-lookup"><span data-stu-id="34558-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34558-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34558-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34558-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34558-105">DESCRIPTION</span></span>
<span data-ttu-id="34558-106">Cmdleten **Save-AzureRmResourceGroupDeploymentTemplate**  sparar en mall för distribution av resurs grupper i en JSON-fil.</span><span class="sxs-lookup"><span data-stu-id="34558-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="34558-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34558-107">EXAMPLES</span></span>

### <span data-ttu-id="34558-108">Exempel 1: Spara en distributionsmall</span><span class="sxs-lookup"><span data-stu-id="34558-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="34558-109">Det här kommandot får distributions mal len från TestDeployment och sparar den som en JSON-fil i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="34558-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="34558-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34558-110">PARAMETERS</span></span>

### <span data-ttu-id="34558-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="34558-111">-ApiVersion</span></span>
<span data-ttu-id="34558-112">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="34558-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="34558-113">Om det inte anges används den senaste API-versionen.</span><span class="sxs-lookup"><span data-stu-id="34558-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="34558-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34558-114">-DefaultProfile</span></span>
<span data-ttu-id="34558-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="34558-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34558-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="34558-116">-DeploymentName</span></span>
<span data-ttu-id="34558-117">Anger namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="34558-117">Specifies the name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34558-118">-Force</span><span class="sxs-lookup"><span data-stu-id="34558-118">-Force</span></span>
<span data-ttu-id="34558-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="34558-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34558-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="34558-120">-InformationAction</span></span>
<span data-ttu-id="34558-121">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="34558-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="34558-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="34558-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="34558-123">Vidare</span><span class="sxs-lookup"><span data-stu-id="34558-123">Continue</span></span>
- <span data-ttu-id="34558-124">Över</span><span class="sxs-lookup"><span data-stu-id="34558-124">Ignore</span></span>
- <span data-ttu-id="34558-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="34558-125">Inquire</span></span>
- <span data-ttu-id="34558-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="34558-126">SilentlyContinue</span></span>
- <span data-ttu-id="34558-127">Stanna</span><span class="sxs-lookup"><span data-stu-id="34558-127">Stop</span></span>
- <span data-ttu-id="34558-128">Avbryt</span><span class="sxs-lookup"><span data-stu-id="34558-128">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34558-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="34558-129">-InformationVariable</span></span>
<span data-ttu-id="34558-130">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="34558-130">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34558-131">-Path</span><span class="sxs-lookup"><span data-stu-id="34558-131">-Path</span></span>
<span data-ttu-id="34558-132">Anger den utgående sökvägen till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="34558-132">Specifies the output path of the template file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34558-133">-För</span><span class="sxs-lookup"><span data-stu-id="34558-133">-Pre</span></span>
<span data-ttu-id="34558-134">Anger att denna cmdlet använder för hands versionen av API-versioner när den automatiskt bestämmer vilken API-version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="34558-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="34558-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34558-135">-ResourceGroupName</span></span>
<span data-ttu-id="34558-136">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="34558-136">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34558-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="34558-137">-Confirm</span></span>
<span data-ttu-id="34558-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="34558-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34558-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34558-139">-WhatIf</span></span>
<span data-ttu-id="34558-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="34558-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34558-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="34558-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34558-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34558-142">CommonParameters</span></span>
<span data-ttu-id="34558-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34558-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34558-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34558-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34558-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34558-145">INPUTS</span></span>

### <span data-ttu-id="34558-146">Ingen</span><span class="sxs-lookup"><span data-stu-id="34558-146">None</span></span>
<span data-ttu-id="34558-147">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="34558-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34558-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34558-148">OUTPUTS</span></span>

### <span data-ttu-id="34558-149">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="34558-149">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="34558-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34558-150">NOTES</span></span>

## <span data-ttu-id="34558-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34558-151">RELATED LINKS</span></span>
