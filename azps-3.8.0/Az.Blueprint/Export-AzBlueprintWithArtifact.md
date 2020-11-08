---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2136a224a5d187951b77c6f48e0b610b48b021b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090104"
---
# <span data-ttu-id="51c99-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="51c99-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="51c99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51c99-102">SYNOPSIS</span></span>
<span data-ttu-id="51c99-103">Exportera den angivna utkasts definitionen till den angivna platsen som en JSON-fil.</span><span class="sxs-lookup"><span data-stu-id="51c99-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="51c99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51c99-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51c99-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51c99-105">DESCRIPTION</span></span>
<span data-ttu-id="51c99-106">Exportera en skiss definition med dess artefakter och Spara på disk.</span><span class="sxs-lookup"><span data-stu-id="51c99-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="51c99-107">Denna cmdlet exporterar den senaste versionen (utkast eller publicerad) av skissen.</span><span class="sxs-lookup"><span data-stu-id="51c99-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="51c99-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51c99-108">EXAMPLES</span></span>

### <span data-ttu-id="51c99-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51c99-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="51c99-110">Exportera en skiss definition med dess artefakter och Spara på disk.</span><span class="sxs-lookup"><span data-stu-id="51c99-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="51c99-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51c99-111">PARAMETERS</span></span>

### <span data-ttu-id="51c99-112">-Skiss</span><span class="sxs-lookup"><span data-stu-id="51c99-112">-Blueprint</span></span>
<span data-ttu-id="51c99-113">Det definitions objekt som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="51c99-113">The blueprint definition object to export.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51c99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51c99-114">-DefaultProfile</span></span>
<span data-ttu-id="51c99-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51c99-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51c99-116">-Force</span><span class="sxs-lookup"><span data-stu-id="51c99-116">-Force</span></span>
<span data-ttu-id="51c99-117">När det här är inställt på True frågar den inte efter en bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="51c99-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="51c99-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="51c99-118">-OutputPath</span></span>
<span data-ttu-id="51c99-119">Sökväg till en fil på disk dit du vill exportera ritnings definitionen i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="51c99-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c99-120">-Version</span><span class="sxs-lookup"><span data-stu-id="51c99-120">-Version</span></span>
<span data-ttu-id="51c99-121">Publicerad version för ritnings definition.</span><span class="sxs-lookup"><span data-stu-id="51c99-121">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="51c99-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c99-122">CommonParameters</span></span>
<span data-ttu-id="51c99-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51c99-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="51c99-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51c99-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c99-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51c99-125">INPUTS</span></span>

### <span data-ttu-id="51c99-126">Microsoft. Azure. commands. skissa. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="51c99-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="51c99-127">System. String</span><span class="sxs-lookup"><span data-stu-id="51c99-127">System.String</span></span>

## <span data-ttu-id="51c99-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51c99-128">OUTPUTS</span></span>

### <span data-ttu-id="51c99-129">System. String</span><span class="sxs-lookup"><span data-stu-id="51c99-129">System.String</span></span>

## <span data-ttu-id="51c99-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51c99-130">NOTES</span></span>

## <span data-ttu-id="51c99-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51c99-131">RELATED LINKS</span></span>
