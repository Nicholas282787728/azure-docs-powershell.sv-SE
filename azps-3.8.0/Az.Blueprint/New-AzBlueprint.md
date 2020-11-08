---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 11a2aeffc1ab3bb170b2e8543d9fd5d0300e3ce5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088897"
---
# <span data-ttu-id="06214-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="06214-101">New-AzBlueprint</span></span>

## <span data-ttu-id="06214-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06214-102">SYNOPSIS</span></span>
<span data-ttu-id="06214-103">Skapa en ny utkasts definition och spara den i det angivna abonnemanget eller den hantera gruppen.</span><span class="sxs-lookup"><span data-stu-id="06214-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="06214-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06214-104">SYNTAX</span></span>

### <span data-ttu-id="06214-105">CreateBlueprintBySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="06214-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06214-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="06214-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06214-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06214-107">DESCRIPTION</span></span>
<span data-ttu-id="06214-108">Skapa en ny utkast definition.</span><span class="sxs-lookup"><span data-stu-id="06214-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="06214-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06214-109">EXAMPLES</span></span>

### <span data-ttu-id="06214-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06214-110">Example 1</span></span>
```powershell
PS C:\> New-AzBlueprint -Name MyNewBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

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

<span data-ttu-id="06214-111">Skapa en ny utkast definition inom det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="06214-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="06214-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06214-112">PARAMETERS</span></span>

### <span data-ttu-id="06214-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="06214-113">-BlueprintFile</span></span>
<span data-ttu-id="06214-114">Sökväg till en skiva med en skiss fil.</span><span class="sxs-lookup"><span data-stu-id="06214-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="06214-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06214-115">-DefaultProfile</span></span>
<span data-ttu-id="06214-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06214-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06214-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="06214-117">-ManagementGroupId</span></span>
<span data-ttu-id="06214-118">Hanterings grupp-ID där ritnings definitionen är eller ska sparas.</span><span class="sxs-lookup"><span data-stu-id="06214-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06214-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="06214-119">-Name</span></span>
<span data-ttu-id="06214-120">Utkastets namn.</span><span class="sxs-lookup"><span data-stu-id="06214-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="06214-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06214-121">-SubscriptionId</span></span>
<span data-ttu-id="06214-122">Abonnemangs-ID där ritnings definitionen är eller ska sparas.</span><span class="sxs-lookup"><span data-stu-id="06214-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06214-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06214-123">-Confirm</span></span>
<span data-ttu-id="06214-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06214-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06214-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06214-125">-WhatIf</span></span>
<span data-ttu-id="06214-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06214-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06214-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06214-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06214-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06214-128">CommonParameters</span></span>
<span data-ttu-id="06214-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06214-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="06214-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06214-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06214-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06214-131">INPUTS</span></span>

### <span data-ttu-id="06214-132">System. String</span><span class="sxs-lookup"><span data-stu-id="06214-132">System.String</span></span>

## <span data-ttu-id="06214-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06214-133">OUTPUTS</span></span>

### <span data-ttu-id="06214-134">Microsoft. Azure. commands. skissa. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="06214-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="06214-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06214-135">NOTES</span></span>

## <span data-ttu-id="06214-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06214-136">RELATED LINKS</span></span>
