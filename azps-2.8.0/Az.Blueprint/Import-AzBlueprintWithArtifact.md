---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 3853cc1785ca0e9f087b1e30870d17d304666df4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745366"
---
# <span data-ttu-id="7b0b1-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="7b0b1-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="7b0b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b0b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7b0b1-103">Importera en skiss fil i JSON-format till ett skiss-objekt och spara det i det angivna abonnemanget eller hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="7b0b1-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="7b0b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b0b1-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b0b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b0b1-105">DESCRIPTION</span></span>
<span data-ttu-id="7b0b1-106">Importera en skiss definition med dess artefakter.</span><span class="sxs-lookup"><span data-stu-id="7b0b1-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="7b0b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b0b1-107">EXAMPLES</span></span>

### <span data-ttu-id="7b0b1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7b0b1-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="7b0b1-109">Importera en skiss definition med dess artefakter och spara i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="7b0b1-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="7b0b1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b0b1-110">PARAMETERS</span></span>

### <span data-ttu-id="7b0b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b0b1-111">-DefaultProfile</span></span>
<span data-ttu-id="7b0b1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b0b1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b0b1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7b0b1-113">-Force</span></span>
<span data-ttu-id="7b0b1-114">När det här är inställt på True frågar den inte efter en bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7b0b1-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="7b0b1-115">-InputPath</span><span class="sxs-lookup"><span data-stu-id="7b0b1-115">-InputPath</span></span>
<span data-ttu-id="7b0b1-116">Sökväg till en skiva med en skiss fil.</span><span class="sxs-lookup"><span data-stu-id="7b0b1-116">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="7b0b1-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="7b0b1-117">-ManagementGroupId</span></span>
<span data-ttu-id="7b0b1-118">Hanterings grupp-ID där ritnings definitionen är eller ska sparas.</span><span class="sxs-lookup"><span data-stu-id="7b0b1-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="7b0b1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="7b0b1-119">-Name</span></span>
<span data-ttu-id="7b0b1-120">Utkastets namn.</span><span class="sxs-lookup"><span data-stu-id="7b0b1-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="7b0b1-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b0b1-121">-SubscriptionId</span></span>
<span data-ttu-id="7b0b1-122">Abonnemangs-ID där ritnings definitionen är eller ska sparas.</span><span class="sxs-lookup"><span data-stu-id="7b0b1-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="7b0b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b0b1-123">CommonParameters</span></span>
<span data-ttu-id="7b0b1-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b0b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7b0b1-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b0b1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b0b1-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b0b1-126">INPUTS</span></span>

### <span data-ttu-id="7b0b1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7b0b1-127">System.String</span></span>

## <span data-ttu-id="7b0b1-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b0b1-128">OUTPUTS</span></span>

### <span data-ttu-id="7b0b1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7b0b1-129">System.String</span></span>

## <span data-ttu-id="7b0b1-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b0b1-130">NOTES</span></span>

## <span data-ttu-id="7b0b1-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b0b1-131">RELATED LINKS</span></span>
