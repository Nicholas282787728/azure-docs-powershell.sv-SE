---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: 155bf1a7851f6cc8e3283c66297df811738edd2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088714"
---
# <span data-ttu-id="a3f5a-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a3f5a-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="a3f5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f5a-103">Uppdatera en skiss definition.</span><span class="sxs-lookup"><span data-stu-id="a3f5a-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="a3f5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3f5a-104">SYNTAX</span></span>

### <span data-ttu-id="a3f5a-105">UpdateBlueprintBySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="a3f5a-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3f5a-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a3f5a-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3f5a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3f5a-107">DESCRIPTION</span></span>
<span data-ttu-id="a3f5a-108">Uppdatera en skiss definition och spara den i det angivna abonnemanget eller den hantera gruppen.</span><span class="sxs-lookup"><span data-stu-id="a3f5a-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="a3f5a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3f5a-109">EXAMPLES</span></span>

### <span data-ttu-id="a3f5a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a3f5a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzBlueprint -Name MyBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

<span data-ttu-id="a3f5a-111">Uppdatera en skiss definition med nya parametrar.</span><span class="sxs-lookup"><span data-stu-id="a3f5a-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="a3f5a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3f5a-112">PARAMETERS</span></span>

### <span data-ttu-id="a3f5a-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="a3f5a-113">-BlueprintFile</span></span>
<span data-ttu-id="a3f5a-114">Sökväg till en skiva med en skiss fil.</span><span class="sxs-lookup"><span data-stu-id="a3f5a-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f5a-115">-DefaultProfile</span></span>
<span data-ttu-id="a3f5a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a3f5a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3f5a-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a3f5a-117">-ManagementGroupId</span></span>
<span data-ttu-id="a3f5a-118">Hanterings grupp-ID där ritnings definitionen är eller ska sparas.</span><span class="sxs-lookup"><span data-stu-id="a3f5a-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup, ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a3f5a-119">-Name</span></span>
<span data-ttu-id="a3f5a-120">Utkastets namn.</span><span class="sxs-lookup"><span data-stu-id="a3f5a-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup, ImportBlueprint
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5a-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3f5a-121">-SubscriptionId</span></span>
<span data-ttu-id="a3f5a-122">Abonnemangs-ID där ritnings definitionen är eller ska sparas.</span><span class="sxs-lookup"><span data-stu-id="a3f5a-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, ImportBlueprint, SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5a-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3f5a-123">-Confirm</span></span>
<span data-ttu-id="a3f5a-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3f5a-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3f5a-125">-WhatIf</span></span>
<span data-ttu-id="a3f5a-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3f5a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3f5a-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3f5a-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f5a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f5a-128">CommonParameters</span></span>
<span data-ttu-id="a3f5a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3f5a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a3f5a-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3f5a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f5a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3f5a-131">INPUTS</span></span>

### <span data-ttu-id="a3f5a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a3f5a-132">System.String</span></span>

## <span data-ttu-id="a3f5a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3f5a-133">OUTPUTS</span></span>

### <span data-ttu-id="a3f5a-134">Microsoft. Azure. commands. skissa. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="a3f5a-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="a3f5a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3f5a-135">NOTES</span></span>

## <span data-ttu-id="a3f5a-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3f5a-136">RELATED LINKS</span></span>
