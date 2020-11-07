---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: f1801aab91887b3dd0d6a9842c7d4a6de1988a88
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "93758456"
---
# <span data-ttu-id="00460-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="00460-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="00460-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00460-102">SYNOPSIS</span></span>
<span data-ttu-id="00460-103">Skapar en resurs grupp som en mall och sparar den i en fil.</span><span class="sxs-lookup"><span data-stu-id="00460-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="00460-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00460-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00460-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00460-105">DESCRIPTION</span></span>
<span data-ttu-id="00460-106">Cmdleten **export-AzResourceGroup** fångar den angivna resurs gruppen som en mall och sparar den i en JSON-fil. Det här kan vara användbart i de fall då du redan har skapat resurser i resurs gruppen och sedan vill använda en mall för distribution av mallar.</span><span class="sxs-lookup"><span data-stu-id="00460-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="00460-107">Denna cmdlet är ett enkelt sätt att börja skapa en mall för de befintliga resurserna i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="00460-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="00460-108">Det kan finnas vissa fall där denna cmdlet inte kan generera vissa delar av mallen.</span><span class="sxs-lookup"><span data-stu-id="00460-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="00460-109">Varnings meddelanden meddelar dig om de resurser som misslyckats.</span><span class="sxs-lookup"><span data-stu-id="00460-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="00460-110">Mallen skapas fortfarande för de delar som lyckades.</span><span class="sxs-lookup"><span data-stu-id="00460-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="00460-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00460-111">EXAMPLES</span></span>

### <span data-ttu-id="00460-112">Exempel 1: exportera en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="00460-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="00460-113">Det här kommandot fångar resurs gruppen som heter TestGroup som en mall och sparar den i en JSON-fil i den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="00460-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="00460-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00460-114">PARAMETERS</span></span>

### <span data-ttu-id="00460-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="00460-115">-ApiVersion</span></span>
<span data-ttu-id="00460-116">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="00460-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="00460-117">Om det inte anges används den senaste API-versionen.</span><span class="sxs-lookup"><span data-stu-id="00460-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="00460-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00460-118">-DefaultProfile</span></span>
<span data-ttu-id="00460-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="00460-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00460-120">-Force</span><span class="sxs-lookup"><span data-stu-id="00460-120">-Force</span></span>
<span data-ttu-id="00460-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="00460-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00460-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="00460-122">-IncludeComments</span></span>
<span data-ttu-id="00460-123">Anger att den här åtgärden exporterar mallen med kommentarer.</span><span class="sxs-lookup"><span data-stu-id="00460-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="00460-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="00460-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="00460-125">Anger att den här åtgärden exporterar mallparameter med standardvärdet.</span><span class="sxs-lookup"><span data-stu-id="00460-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="00460-126">-Path</span><span class="sxs-lookup"><span data-stu-id="00460-126">-Path</span></span>
<span data-ttu-id="00460-127">Anger den utgående sökvägen till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="00460-127">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="00460-128">-För</span><span class="sxs-lookup"><span data-stu-id="00460-128">-Pre</span></span>
<span data-ttu-id="00460-129">Anger att denna cmdlet använder för hands versionen av API-versioner när den automatiskt bestämmer vilken API-version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="00460-129">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="00460-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00460-130">-ResourceGroupName</span></span>
<span data-ttu-id="00460-131">Anger namnet på den resurs grupp som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="00460-131">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="00460-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="00460-132">-Confirm</span></span>
<span data-ttu-id="00460-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="00460-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00460-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00460-134">-WhatIf</span></span>
<span data-ttu-id="00460-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="00460-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00460-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="00460-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00460-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00460-137">CommonParameters</span></span>
<span data-ttu-id="00460-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00460-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00460-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00460-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00460-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00460-140">INPUTS</span></span>

### <span data-ttu-id="00460-141">System. String</span><span class="sxs-lookup"><span data-stu-id="00460-141">System.String</span></span>

## <span data-ttu-id="00460-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00460-142">OUTPUTS</span></span>

### <span data-ttu-id="00460-143">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="00460-143">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="00460-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00460-144">NOTES</span></span>

## <span data-ttu-id="00460-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00460-145">RELATED LINKS</span></span>

[<span data-ttu-id="00460-146">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="00460-146">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


