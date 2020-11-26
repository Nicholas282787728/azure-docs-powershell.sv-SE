---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269340"
---
# <span data-ttu-id="2221b-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="2221b-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="2221b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2221b-102">SYNOPSIS</span></span>
<span data-ttu-id="2221b-103">Importera en skiss fil i JSON-format till ett skiss-objekt och spara det i det angivna abonnemanget eller hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="2221b-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="2221b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2221b-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2221b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2221b-105">DESCRIPTION</span></span>
<span data-ttu-id="2221b-106">Importera en skiss definition med dess artefakter.</span><span class="sxs-lookup"><span data-stu-id="2221b-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="2221b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2221b-107">EXAMPLES</span></span>

### <span data-ttu-id="2221b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2221b-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="2221b-109">Importera en skiss definition med dess artefakter och spara i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="2221b-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="2221b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2221b-110">PARAMETERS</span></span>

### <span data-ttu-id="2221b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2221b-111">-DefaultProfile</span></span>
<span data-ttu-id="2221b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2221b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2221b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2221b-113">-Force</span></span>
<span data-ttu-id="2221b-114">När det här är inställt på True frågar den inte efter en bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2221b-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="2221b-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="2221b-115">-IncludeSubFolders</span></span>
<span data-ttu-id="2221b-116">När du har angett värdet sant inkluderas artefakt i undermappar.</span><span class="sxs-lookup"><span data-stu-id="2221b-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="2221b-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="2221b-117">-InputPath</span></span>
<span data-ttu-id="2221b-118">Sökväg till en skiva med en skiss fil.</span><span class="sxs-lookup"><span data-stu-id="2221b-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="2221b-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="2221b-119">-ManagementGroupId</span></span>
<span data-ttu-id="2221b-120">Hanterings grupp-ID där ritnings definitionen är eller ska sparas.</span><span class="sxs-lookup"><span data-stu-id="2221b-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="2221b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="2221b-121">-Name</span></span>
<span data-ttu-id="2221b-122">Utkastets namn.</span><span class="sxs-lookup"><span data-stu-id="2221b-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="2221b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2221b-123">-PassThru</span></span>
<span data-ttu-id="2221b-124">När den är aktive rad returnerar cmdleten ett objekt som representerar den importerade utkasts definitionen.</span><span class="sxs-lookup"><span data-stu-id="2221b-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="2221b-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2221b-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2221b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2221b-126">-SubscriptionId</span></span>
<span data-ttu-id="2221b-127">Abonnemangs-ID där ritnings definitionen är eller ska sparas.</span><span class="sxs-lookup"><span data-stu-id="2221b-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="2221b-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2221b-128">-Confirm</span></span>
<span data-ttu-id="2221b-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2221b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2221b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2221b-130">-WhatIf</span></span>
<span data-ttu-id="2221b-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2221b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2221b-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2221b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2221b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2221b-133">CommonParameters</span></span>
<span data-ttu-id="2221b-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2221b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2221b-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2221b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2221b-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2221b-136">INPUTS</span></span>

### <span data-ttu-id="2221b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2221b-137">System.String</span></span>

## <span data-ttu-id="2221b-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2221b-138">OUTPUTS</span></span>

### <span data-ttu-id="2221b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2221b-139">System.String</span></span>

## <span data-ttu-id="2221b-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2221b-140">NOTES</span></span>

## <span data-ttu-id="2221b-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2221b-141">RELATED LINKS</span></span>