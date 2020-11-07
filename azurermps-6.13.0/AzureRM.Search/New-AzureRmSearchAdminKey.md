---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchAdminKey.md
ms.openlocfilehash: fa7ea6f1e53b94a349d51856432f1c01b2e89ba0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756361"
---
# <span data-ttu-id="3d97c-101">New-AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="3d97c-101">New-AzureRmSearchAdminKey</span></span>

## <span data-ttu-id="3d97c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d97c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d97c-103">Återskapar en administratörs nyckeln för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3d97c-103">Regenerates an admin key of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d97c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d97c-104">SYNTAX</span></span>

### <span data-ttu-id="3d97c-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3d97c-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d97c-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d97c-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d97c-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d97c-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d97c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d97c-108">DESCRIPTION</span></span>
<span data-ttu-id="3d97c-109">**New-AzureRmSearchAdminKey** cmdlet återskapar en administratörs nyckeln för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3d97c-109">The **New-AzureRmSearchAdminKey** cmdlet regenerates an admin key of the Azure Search service.</span></span>

## <span data-ttu-id="3d97c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d97c-110">EXAMPLES</span></span>

### <span data-ttu-id="3d97c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3d97c-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="3d97c-112">Exemplet återskapar primär nyckeln för Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3d97c-112">The example regenerates Primary key of the Azure Search Service.</span></span>

## <span data-ttu-id="3d97c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d97c-113">PARAMETERS</span></span>

### <span data-ttu-id="3d97c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d97c-114">-DefaultProfile</span></span>
<span data-ttu-id="3d97c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d97c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d97c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3d97c-116">-Force</span></span>
<span data-ttu-id="3d97c-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3d97c-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3d97c-118">-Sort</span><span class="sxs-lookup"><span data-stu-id="3d97c-118">-KeyKind</span></span>
<span data-ttu-id="3d97c-119">Sök tjänstens administratörs typ (primär/sekundär).</span><span class="sxs-lookup"><span data-stu-id="3d97c-119">Search Service admin key kind (Primary/Secondary).</span></span>

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

### <span data-ttu-id="3d97c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3d97c-120">-ParentObject</span></span>
<span data-ttu-id="3d97c-121">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="3d97c-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="3d97c-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3d97c-122">-ParentResourceId</span></span>
<span data-ttu-id="3d97c-123">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3d97c-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="3d97c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d97c-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d97c-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="3d97c-125">Resource Group name.</span></span>

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

### <span data-ttu-id="3d97c-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3d97c-126">-ServiceName</span></span>
<span data-ttu-id="3d97c-127">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="3d97c-127">Search Service name.</span></span>

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

### <span data-ttu-id="3d97c-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d97c-128">-Confirm</span></span>
<span data-ttu-id="3d97c-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d97c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d97c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d97c-130">-WhatIf</span></span>
<span data-ttu-id="3d97c-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d97c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d97c-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d97c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d97c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d97c-133">CommonParameters</span></span>
<span data-ttu-id="3d97c-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d97c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d97c-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d97c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d97c-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d97c-136">INPUTS</span></span>

### <span data-ttu-id="3d97c-137">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="3d97c-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="3d97c-138">Parametrar: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3d97c-138">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="3d97c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3d97c-139">System.String</span></span>

## <span data-ttu-id="3d97c-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d97c-140">OUTPUTS</span></span>

### <span data-ttu-id="3d97c-141">Microsoft. Azure. commands. Management. search. Models. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="3d97c-141">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="3d97c-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d97c-142">NOTES</span></span>

## <span data-ttu-id="3d97c-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d97c-143">RELATED LINKS</span></span>

[<span data-ttu-id="3d97c-144">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="3d97c-144">Get-AzureRmSearchAdminKeyPair</span></span>](./Get-AzureRmSearchAdminKeyPair.md)
