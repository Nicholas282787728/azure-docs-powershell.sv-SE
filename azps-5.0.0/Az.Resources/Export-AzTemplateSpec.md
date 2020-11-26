---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322410"
---
# <span data-ttu-id="0b3e5-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="0b3e5-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="0b3e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3e5-103">Exporterar en mall till det lokala fil systemet</span><span class="sxs-lookup"><span data-stu-id="0b3e5-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="0b3e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b3e5-104">SYNTAX</span></span>

### <span data-ttu-id="0b3e5-105">ExportByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0b3e5-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b3e5-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b3e5-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b3e5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b3e5-107">DESCRIPTION</span></span>
<span data-ttu-id="0b3e5-108">Exporterar en specifik mall-version till det lokala fil systemet.</span><span class="sxs-lookup"><span data-stu-id="0b3e5-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="0b3e5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b3e5-109">EXAMPLES</span></span>

### <span data-ttu-id="0b3e5-110">Exempel 1: exportera med namn</span><span class="sxs-lookup"><span data-stu-id="0b3e5-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="0b3e5-111">Exporterar version ' v 1.0 ' för mallnamnet med namnet "MyTemplateSpec" i resurs gruppen "myRG" till den lokala utdatafilen "v1".</span><span class="sxs-lookup"><span data-stu-id="0b3e5-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="0b3e5-112">Exempel 2: exportera per resurs-ID</span><span class="sxs-lookup"><span data-stu-id="0b3e5-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="0b3e5-113">Exporterar version ' v 1.0 ' för mallnamnet med namnet "MyTemplateSpec" i resurs gruppen "myRG" i prenumerationen \{ subId \} till den lokala utdatafilen "v1".</span><span class="sxs-lookup"><span data-stu-id="0b3e5-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="0b3e5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b3e5-114">PARAMETERS</span></span>

### <span data-ttu-id="0b3e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b3e5-115">-DefaultProfile</span></span>
<span data-ttu-id="0b3e5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b3e5-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="0b3e5-117">-Name</span></span>
<span data-ttu-id="0b3e5-118">Namnet på mallens spec.</span><span class="sxs-lookup"><span data-stu-id="0b3e5-118">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3e5-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="0b3e5-119">-OutputFolder</span></span>
<span data-ttu-id="0b3e5-120">Sökvägen till mappen där versions information för mallen ska sparas.</span><span class="sxs-lookup"><span data-stu-id="0b3e5-120">The path to the folder where the template spec version will be output to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b3e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="0b3e5-122">Namnet på resurs gruppen för den här mallen.</span><span class="sxs-lookup"><span data-stu-id="0b3e5-122">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3e5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b3e5-123">-ResourceId</span></span>
<span data-ttu-id="0b3e5-124">Fullständigt resurs-ID för mallens spec. exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="0b3e5-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3e5-125">-Version</span><span class="sxs-lookup"><span data-stu-id="0b3e5-125">-Version</span></span>
<span data-ttu-id="0b3e5-126">Den version av mallen som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="0b3e5-126">The version of the template spec to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b3e5-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0b3e5-127">-Confirm</span></span>
<span data-ttu-id="0b3e5-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0b3e5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b3e5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b3e5-129">-WhatIf</span></span>
<span data-ttu-id="0b3e5-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0b3e5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b3e5-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0b3e5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b3e5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3e5-132">CommonParameters</span></span>
<span data-ttu-id="0b3e5-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b3e5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3e5-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b3e5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3e5-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b3e5-135">INPUTS</span></span>

### <span data-ttu-id="0b3e5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0b3e5-136">System.String</span></span>

## <span data-ttu-id="0b3e5-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b3e5-137">OUTPUTS</span></span>

### <span data-ttu-id="0b3e5-138">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0b3e5-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0b3e5-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b3e5-139">NOTES</span></span>

## <span data-ttu-id="0b3e5-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b3e5-140">RELATED LINKS</span></span>