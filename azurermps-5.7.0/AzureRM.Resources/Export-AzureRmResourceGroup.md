---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/export-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
ms.openlocfilehash: 489e1fed20231dbd4fbb20d52365e7e46b1d4230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576427"
---
# <span data-ttu-id="7e003-101">Export-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7e003-101">Export-AzureRmResourceGroup</span></span>

## <span data-ttu-id="7e003-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e003-102">SYNOPSIS</span></span>
<span data-ttu-id="7e003-103">Skapar en resurs grupp som en mall och sparar den i en fil.</span><span class="sxs-lookup"><span data-stu-id="7e003-103">Captures a resource group as a template and saves it to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e003-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e003-104">SYNTAX</span></span>

```
Export-AzureRmResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e003-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e003-105">DESCRIPTION</span></span>
<span data-ttu-id="7e003-106">Cmdleten **export-AzureRmResourceGroup** fångar den angivna resurs gruppen som en mall och sparar den i en JSON-fil. Det här kan vara användbart i de fall då du redan har skapat resurser i resurs gruppen och sedan vill använda en mall för distribution av mallar.</span><span class="sxs-lookup"><span data-stu-id="7e003-106">The **Export-AzureRmResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="7e003-107">Denna cmdlet är ett enkelt sätt att börja skapa en mall för de befintliga resurserna i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7e003-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>

<span data-ttu-id="7e003-108">Det kan finnas vissa fall där denna cmdlet inte kan generera vissa delar av mallen.</span><span class="sxs-lookup"><span data-stu-id="7e003-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="7e003-109">Varnings meddelanden meddelar dig om de resurser som misslyckats.</span><span class="sxs-lookup"><span data-stu-id="7e003-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="7e003-110">Mallen skapas fortfarande för de delar som lyckades.</span><span class="sxs-lookup"><span data-stu-id="7e003-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="7e003-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e003-111">EXAMPLES</span></span>

### <span data-ttu-id="7e003-112">Exempel 1: exportera en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="7e003-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzureRmResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="7e003-113">Det här kommandot fångar resurs gruppen som heter TestGroup som en mall och sparar den i en JSON-fil i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="7e003-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="7e003-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e003-114">PARAMETERS</span></span>

### <span data-ttu-id="7e003-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7e003-115">-ApiVersion</span></span>
<span data-ttu-id="7e003-116">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="7e003-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7e003-117">Om det inte anges används den senaste API-versionen.</span><span class="sxs-lookup"><span data-stu-id="7e003-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="7e003-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e003-118">-DefaultProfile</span></span>
<span data-ttu-id="7e003-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7e003-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e003-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7e003-120">-Force</span></span>
<span data-ttu-id="7e003-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7e003-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7e003-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="7e003-122">-IncludeComments</span></span>
<span data-ttu-id="7e003-123">Anger att den här åtgärden exporterar mallen med kommentarer.</span><span class="sxs-lookup"><span data-stu-id="7e003-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="7e003-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="7e003-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="7e003-125">Anger att den här åtgärden exporterar mallparameter med standardvärdet.</span><span class="sxs-lookup"><span data-stu-id="7e003-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="7e003-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7e003-126">-InformationAction</span></span>
<span data-ttu-id="7e003-127">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="7e003-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7e003-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7e003-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e003-129">Vidare</span><span class="sxs-lookup"><span data-stu-id="7e003-129">Continue</span></span>
- <span data-ttu-id="7e003-130">Över</span><span class="sxs-lookup"><span data-stu-id="7e003-130">Ignore</span></span>
- <span data-ttu-id="7e003-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="7e003-131">Inquire</span></span>
- <span data-ttu-id="7e003-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7e003-132">SilentlyContinue</span></span>
- <span data-ttu-id="7e003-133">Stanna</span><span class="sxs-lookup"><span data-stu-id="7e003-133">Stop</span></span>
- <span data-ttu-id="7e003-134">Avbryt</span><span class="sxs-lookup"><span data-stu-id="7e003-134">Suspend</span></span>

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

### <span data-ttu-id="7e003-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7e003-135">-InformationVariable</span></span>
<span data-ttu-id="7e003-136">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="7e003-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7e003-137">-Path</span><span class="sxs-lookup"><span data-stu-id="7e003-137">-Path</span></span>
<span data-ttu-id="7e003-138">Anger den utgående sökvägen till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="7e003-138">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="7e003-139">-För</span><span class="sxs-lookup"><span data-stu-id="7e003-139">-Pre</span></span>
<span data-ttu-id="7e003-140">Anger att denna cmdlet använder för hands versionen av API-versioner när den automatiskt bestämmer vilken API-version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="7e003-140">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="7e003-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e003-141">-ResourceGroupName</span></span>
<span data-ttu-id="7e003-142">Anger namnet på den resurs grupp som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="7e003-142">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="7e003-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7e003-143">-Confirm</span></span>
<span data-ttu-id="7e003-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7e003-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e003-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e003-145">-WhatIf</span></span>
<span data-ttu-id="7e003-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7e003-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e003-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7e003-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e003-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e003-148">CommonParameters</span></span>
<span data-ttu-id="7e003-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e003-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e003-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e003-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e003-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e003-151">INPUTS</span></span>

### <span data-ttu-id="7e003-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="7e003-152">None</span></span>
<span data-ttu-id="7e003-153">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7e003-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e003-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e003-154">OUTPUTS</span></span>

### <span data-ttu-id="7e003-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7e003-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7e003-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e003-156">NOTES</span></span>

## <span data-ttu-id="7e003-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e003-157">RELATED LINKS</span></span>

[<span data-ttu-id="7e003-158">Sök-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7e003-158">Find-AzureRmResourceGroup</span></span>](./Find-AzureRmResourceGroup.md)

