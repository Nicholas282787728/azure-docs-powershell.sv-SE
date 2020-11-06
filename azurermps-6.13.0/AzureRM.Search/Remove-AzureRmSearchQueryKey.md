---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchQueryKey.md
ms.openlocfilehash: 1dbdf342335ca204287ccfd2efea737f2eb747fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580704"
---
# <span data-ttu-id="5bf6f-101">Remove-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="5bf6f-101">Remove-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="5bf6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5bf6f-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf6f-103">Ta bort Frågeparametern från Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-103">Remove the query key from the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bf6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5bf6f-104">SYNTAX</span></span>

### <span data-ttu-id="5bf6f-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5bf6f-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bf6f-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bf6f-106">ParentObjectParameterSet</span></span>
```
Remove-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bf6f-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bf6f-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bf6f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5bf6f-108">DESCRIPTION</span></span>
<span data-ttu-id="5bf6f-109">Cmdleten **Remove-AzureRmSearchQueryKey** tar bort Frågeparametern från Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-109">The **Remove-AzureRmSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="5bf6f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5bf6f-110">EXAMPLES</span></span>

### <span data-ttu-id="5bf6f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5bf6f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="5bf6f-112">Exemplet tar bort Frågeparametern från Azure Search-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="5bf6f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5bf6f-113">PARAMETERS</span></span>

### <span data-ttu-id="5bf6f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf6f-114">-DefaultProfile</span></span>
<span data-ttu-id="5bf6f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bf6f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5bf6f-116">-Force</span></span>
<span data-ttu-id="5bf6f-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5bf6f-118">-Nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="5bf6f-118">-KeyValue</span></span>
<span data-ttu-id="5bf6f-119">Sök tjänstens frågeresultat.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="5bf6f-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5bf6f-120">-ParentObject</span></span>
<span data-ttu-id="5bf6f-121">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="5bf6f-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5bf6f-122">-ParentResourceId</span></span>
<span data-ttu-id="5bf6f-123">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="5bf6f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bf6f-124">-PassThru</span></span>
<span data-ttu-id="5bf6f-125">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="5bf6f-126">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5bf6f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bf6f-127">-ResourceGroupName</span></span>
<span data-ttu-id="5bf6f-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-128">Resource Group name.</span></span>

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

### <span data-ttu-id="5bf6f-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5bf6f-129">-ServiceName</span></span>
<span data-ttu-id="5bf6f-130">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-130">Search Service name.</span></span>

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

### <span data-ttu-id="5bf6f-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5bf6f-131">-Confirm</span></span>
<span data-ttu-id="5bf6f-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf6f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf6f-133">-WhatIf</span></span>
<span data-ttu-id="5bf6f-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf6f-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf6f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf6f-136">CommonParameters</span></span>
<span data-ttu-id="5bf6f-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf6f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf6f-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bf6f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf6f-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5bf6f-139">INPUTS</span></span>

### <span data-ttu-id="5bf6f-140">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="5bf6f-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="5bf6f-141">Parametrar: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5bf6f-141">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="5bf6f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5bf6f-142">System.String</span></span>

## <span data-ttu-id="5bf6f-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5bf6f-143">OUTPUTS</span></span>

### <span data-ttu-id="5bf6f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5bf6f-144">System.Boolean</span></span>

## <span data-ttu-id="5bf6f-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5bf6f-145">NOTES</span></span>

## <span data-ttu-id="5bf6f-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5bf6f-146">RELATED LINKS</span></span>

[<span data-ttu-id="5bf6f-147">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="5bf6f-147">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="5bf6f-148">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="5bf6f-148">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)
