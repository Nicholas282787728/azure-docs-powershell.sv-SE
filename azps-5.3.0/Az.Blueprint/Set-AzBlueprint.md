---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: cbfd316b459c9cd2e1fc60e4416e50c426a3dc19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527188"
---
# <span data-ttu-id="ea8f3-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="ea8f3-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="ea8f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8f3-103">Uppdatera en skiss definition.</span><span class="sxs-lookup"><span data-stu-id="ea8f3-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="ea8f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea8f3-104">SYNTAX</span></span>

### <span data-ttu-id="ea8f3-105">UpdateBlueprintBySubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="ea8f3-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea8f3-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ea8f3-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea8f3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea8f3-107">DESCRIPTION</span></span>
<span data-ttu-id="ea8f3-108">Uppdatera en skiss definition och spara den i det angivna abonnemanget eller den hantera gruppen.</span><span class="sxs-lookup"><span data-stu-id="ea8f3-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="ea8f3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea8f3-109">EXAMPLES</span></span>

### <span data-ttu-id="ea8f3-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ea8f3-110">Example 1</span></span>
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

<span data-ttu-id="ea8f3-111">Uppdatera en skiss definition med nya parametrar.</span><span class="sxs-lookup"><span data-stu-id="ea8f3-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="ea8f3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea8f3-112">PARAMETERS</span></span>

### <span data-ttu-id="ea8f3-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="ea8f3-113">-BlueprintFile</span></span>
<span data-ttu-id="ea8f3-114">Sökväg till en skiva med en skiss fil.</span><span class="sxs-lookup"><span data-stu-id="ea8f3-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="ea8f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8f3-115">-DefaultProfile</span></span>
<span data-ttu-id="ea8f3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea8f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea8f3-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ea8f3-117">-ManagementGroupId</span></span>
<span data-ttu-id="ea8f3-118">Hanterings grupp-ID där ritnings definitionen är eller ska sparas.</span><span class="sxs-lookup"><span data-stu-id="ea8f3-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8f3-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea8f3-119">-Name</span></span>
<span data-ttu-id="ea8f3-120">Utkastets namn.</span><span class="sxs-lookup"><span data-stu-id="ea8f3-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="ea8f3-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea8f3-121">-SubscriptionId</span></span>
<span data-ttu-id="ea8f3-122">Abonnemangs-ID där ritnings definitionen är eller ska sparas.</span><span class="sxs-lookup"><span data-stu-id="ea8f3-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8f3-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea8f3-123">-Confirm</span></span>
<span data-ttu-id="ea8f3-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea8f3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea8f3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea8f3-125">-WhatIf</span></span>
<span data-ttu-id="ea8f3-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea8f3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea8f3-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea8f3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea8f3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8f3-128">CommonParameters</span></span>
<span data-ttu-id="ea8f3-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea8f3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8f3-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea8f3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8f3-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea8f3-131">INPUTS</span></span>

### <span data-ttu-id="ea8f3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ea8f3-132">System.String</span></span>

## <span data-ttu-id="ea8f3-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea8f3-133">OUTPUTS</span></span>

### <span data-ttu-id="ea8f3-134">Microsoft. Azure. commands. skissa. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="ea8f3-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="ea8f3-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea8f3-135">NOTES</span></span>

## <span data-ttu-id="ea8f3-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea8f3-136">RELATED LINKS</span></span>
