---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527207"
---
# <span data-ttu-id="a1833-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="a1833-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="a1833-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1833-102">SYNOPSIS</span></span>
<span data-ttu-id="a1833-103">Exportera den angivna utkasts definitionen till den angivna platsen som en JSON-fil.</span><span class="sxs-lookup"><span data-stu-id="a1833-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="a1833-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1833-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1833-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1833-105">DESCRIPTION</span></span>
<span data-ttu-id="a1833-106">Exportera en skiss definition med dess artefakter och Spara på disk.</span><span class="sxs-lookup"><span data-stu-id="a1833-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="a1833-107">Denna cmdlet exporterar den senaste versionen (utkast eller publicerad) av skissen.</span><span class="sxs-lookup"><span data-stu-id="a1833-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="a1833-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1833-108">EXAMPLES</span></span>

### <span data-ttu-id="a1833-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a1833-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="a1833-110">Exportera en skiss definition med dess artefakter och Spara på disk.</span><span class="sxs-lookup"><span data-stu-id="a1833-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="a1833-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1833-111">PARAMETERS</span></span>

### <span data-ttu-id="a1833-112">-Skiss</span><span class="sxs-lookup"><span data-stu-id="a1833-112">-Blueprint</span></span>
<span data-ttu-id="a1833-113">Det definitions objekt som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="a1833-113">The blueprint definition object to export.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1833-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1833-114">-DefaultProfile</span></span>
<span data-ttu-id="a1833-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1833-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1833-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a1833-116">-Force</span></span>
<span data-ttu-id="a1833-117">När det här är inställt på True frågar den inte efter en bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a1833-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="a1833-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="a1833-118">-OutputPath</span></span>
<span data-ttu-id="a1833-119">Sökväg till en fil på disk dit du vill exportera ritnings definitionen i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="a1833-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="a1833-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1833-120">-PassThru</span></span>
<span data-ttu-id="a1833-121">När den är aktive rad returnerar cmdleten ett objekt som representerar den exporterade utkasts definitionen.</span><span class="sxs-lookup"><span data-stu-id="a1833-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="a1833-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a1833-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a1833-123">-Version</span><span class="sxs-lookup"><span data-stu-id="a1833-123">-Version</span></span>
<span data-ttu-id="a1833-124">Publicerad version för ritnings definition.</span><span class="sxs-lookup"><span data-stu-id="a1833-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="a1833-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a1833-125">-Confirm</span></span>
<span data-ttu-id="a1833-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a1833-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1833-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1833-127">-WhatIf</span></span>
<span data-ttu-id="a1833-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a1833-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1833-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a1833-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1833-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1833-130">CommonParameters</span></span>
<span data-ttu-id="a1833-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1833-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1833-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1833-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1833-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1833-133">INPUTS</span></span>

### <span data-ttu-id="a1833-134">Microsoft. Azure. commands. skissa. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="a1833-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="a1833-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a1833-135">System.String</span></span>

## <span data-ttu-id="a1833-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1833-136">OUTPUTS</span></span>

### <span data-ttu-id="a1833-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a1833-137">System.String</span></span>

## <span data-ttu-id="a1833-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1833-138">NOTES</span></span>

## <span data-ttu-id="a1833-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1833-139">RELATED LINKS</span></span>
