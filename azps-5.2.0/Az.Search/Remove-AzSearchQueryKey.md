---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: e7a74fcc6d5e1a80282cfb365070df1b339aea45
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406912"
---
# <span data-ttu-id="c230e-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="c230e-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="c230e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c230e-102">SYNOPSIS</span></span>
<span data-ttu-id="c230e-103">Ta bort Frågeparametern från Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c230e-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="c230e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c230e-104">SYNTAX</span></span>

### <span data-ttu-id="c230e-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c230e-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c230e-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c230e-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c230e-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c230e-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c230e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c230e-108">DESCRIPTION</span></span>
<span data-ttu-id="c230e-109">Cmdleten **Remove-AzSearchQueryKey** tar bort Frågeparametern från Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c230e-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="c230e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c230e-110">EXAMPLES</span></span>

### <span data-ttu-id="c230e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c230e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="c230e-112">Exemplet tar bort Frågeparametern från Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c230e-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="c230e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c230e-113">PARAMETERS</span></span>

### <span data-ttu-id="c230e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c230e-114">-DefaultProfile</span></span>
<span data-ttu-id="c230e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c230e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c230e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c230e-116">-Force</span></span>
<span data-ttu-id="c230e-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c230e-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c230e-118">-Nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="c230e-118">-KeyValue</span></span>
<span data-ttu-id="c230e-119">Sök tjänstens frågeresultat.</span><span class="sxs-lookup"><span data-stu-id="c230e-119">Search Service query key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c230e-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c230e-120">-ParentObject</span></span>
<span data-ttu-id="c230e-121">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="c230e-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="c230e-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c230e-122">-ParentResourceId</span></span>
<span data-ttu-id="c230e-123">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c230e-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="c230e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c230e-124">-PassThru</span></span>
<span data-ttu-id="c230e-125">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="c230e-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="c230e-126">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="c230e-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c230e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c230e-127">-ResourceGroupName</span></span>
<span data-ttu-id="c230e-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c230e-128">Resource Group name.</span></span>

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

### <span data-ttu-id="c230e-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c230e-129">-ServiceName</span></span>
<span data-ttu-id="c230e-130">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="c230e-130">Search Service name.</span></span>

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

### <span data-ttu-id="c230e-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c230e-131">-Confirm</span></span>
<span data-ttu-id="c230e-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c230e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c230e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c230e-133">-WhatIf</span></span>
<span data-ttu-id="c230e-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c230e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c230e-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c230e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c230e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c230e-136">CommonParameters</span></span>
<span data-ttu-id="c230e-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c230e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c230e-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c230e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c230e-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c230e-139">INPUTS</span></span>

### <span data-ttu-id="c230e-140">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="c230e-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="c230e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c230e-141">System.String</span></span>

## <span data-ttu-id="c230e-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c230e-142">OUTPUTS</span></span>

### <span data-ttu-id="c230e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c230e-143">System.Boolean</span></span>

## <span data-ttu-id="c230e-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c230e-144">NOTES</span></span>

## <span data-ttu-id="c230e-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c230e-145">RELATED LINKS</span></span>

[<span data-ttu-id="c230e-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="c230e-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="c230e-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="c230e-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
