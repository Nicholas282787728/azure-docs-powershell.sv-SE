---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: ae925d39dab3b56e70cb7c42b320e57eb7f7811a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258027"
---
# <span data-ttu-id="393a7-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="393a7-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="393a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="393a7-102">SYNOPSIS</span></span>
<span data-ttu-id="393a7-103">Återskapar en administratörs nyckeln för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="393a7-103">Regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="393a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="393a7-104">SYNTAX</span></span>

### <span data-ttu-id="393a7-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="393a7-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="393a7-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="393a7-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="393a7-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="393a7-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="393a7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="393a7-108">DESCRIPTION</span></span>
<span data-ttu-id="393a7-109">**New-AzSearchAdminKey** cmdlet återskapar en administratörs nyckeln för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="393a7-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="393a7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="393a7-110">EXAMPLES</span></span>

### <span data-ttu-id="393a7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="393a7-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="393a7-112">Exemplet återskapar primär nyckeln för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="393a7-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="393a7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="393a7-113">PARAMETERS</span></span>

### <span data-ttu-id="393a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393a7-114">-DefaultProfile</span></span>
<span data-ttu-id="393a7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="393a7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="393a7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="393a7-116">-Force</span></span>
<span data-ttu-id="393a7-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="393a7-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="393a7-118">-Sort</span><span class="sxs-lookup"><span data-stu-id="393a7-118">-KeyKind</span></span>
<span data-ttu-id="393a7-119">Sök tjänstens administratörs typ (primär/sekundär).</span><span class="sxs-lookup"><span data-stu-id="393a7-119">Search Service admin key kind (Primary/Secondary).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKeyKind
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393a7-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="393a7-120">-ParentObject</span></span>
<span data-ttu-id="393a7-121">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="393a7-121">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="393a7-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="393a7-122">-ParentResourceId</span></span>
<span data-ttu-id="393a7-123">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="393a7-123">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="393a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="393a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="393a7-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="393a7-125">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393a7-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="393a7-126">-ServiceName</span></span>
<span data-ttu-id="393a7-127">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="393a7-127">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393a7-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="393a7-128">-Confirm</span></span>
<span data-ttu-id="393a7-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="393a7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="393a7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="393a7-130">-WhatIf</span></span>
<span data-ttu-id="393a7-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="393a7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="393a7-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="393a7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="393a7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393a7-133">CommonParameters</span></span>
<span data-ttu-id="393a7-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="393a7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393a7-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="393a7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393a7-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="393a7-136">INPUTS</span></span>

### <span data-ttu-id="393a7-137">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="393a7-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="393a7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="393a7-138">System.String</span></span>

## <span data-ttu-id="393a7-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="393a7-139">OUTPUTS</span></span>

### <span data-ttu-id="393a7-140">Microsoft. Azure. commands. Management. search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="393a7-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="393a7-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="393a7-141">NOTES</span></span>

## <span data-ttu-id="393a7-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="393a7-142">RELATED LINKS</span></span>

[<span data-ttu-id="393a7-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="393a7-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)