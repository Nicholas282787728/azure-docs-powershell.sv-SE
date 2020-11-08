---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 7a1778ce107e9753f78876aff3a2dfba19e138e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091412"
---
# <span data-ttu-id="4c22e-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="4c22e-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="4c22e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c22e-102">SYNOPSIS</span></span>
<span data-ttu-id="4c22e-103">Importera en skiss fil i JSON-format till ett skiss-objekt och spara det i det angivna abonnemanget eller hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="4c22e-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="4c22e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c22e-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c22e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c22e-105">DESCRIPTION</span></span>
<span data-ttu-id="4c22e-106">Importera en skiss definition med dess artefakter.</span><span class="sxs-lookup"><span data-stu-id="4c22e-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="4c22e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c22e-107">EXAMPLES</span></span>

### <span data-ttu-id="4c22e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4c22e-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="4c22e-109">Importera en skiss definition med dess artefakter och spara i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="4c22e-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="4c22e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c22e-110">PARAMETERS</span></span>

### <span data-ttu-id="4c22e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c22e-111">-DefaultProfile</span></span>
<span data-ttu-id="4c22e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c22e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c22e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4c22e-113">-Force</span></span>
<span data-ttu-id="4c22e-114">När det här är inställt på True frågar den inte efter en bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4c22e-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="4c22e-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="4c22e-115">-IncludeSubFolders</span></span>
<span data-ttu-id="4c22e-116">När du har angett värdet sant inkluderas artefakt i undermappar.</span><span class="sxs-lookup"><span data-stu-id="4c22e-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="4c22e-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="4c22e-117">-InputPath</span></span>
<span data-ttu-id="4c22e-118">Sökväg till en skiva med en skiss fil.</span><span class="sxs-lookup"><span data-stu-id="4c22e-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="4c22e-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="4c22e-119">-ManagementGroupId</span></span>
<span data-ttu-id="4c22e-120">Hanterings grupp-ID där ritnings definitionen är eller ska sparas.</span><span class="sxs-lookup"><span data-stu-id="4c22e-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="4c22e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="4c22e-121">-Name</span></span>
<span data-ttu-id="4c22e-122">Utkastets namn.</span><span class="sxs-lookup"><span data-stu-id="4c22e-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="4c22e-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c22e-123">-SubscriptionId</span></span>
<span data-ttu-id="4c22e-124">Abonnemangs-ID där ritnings definitionen är eller ska sparas.</span><span class="sxs-lookup"><span data-stu-id="4c22e-124">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="4c22e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c22e-125">CommonParameters</span></span>
<span data-ttu-id="4c22e-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c22e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4c22e-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c22e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c22e-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c22e-128">INPUTS</span></span>

### <span data-ttu-id="4c22e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4c22e-129">System.String</span></span>

## <span data-ttu-id="4c22e-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c22e-130">OUTPUTS</span></span>

### <span data-ttu-id="4c22e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4c22e-131">System.String</span></span>

## <span data-ttu-id="4c22e-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c22e-132">NOTES</span></span>

## <span data-ttu-id="4c22e-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c22e-133">RELATED LINKS</span></span>
