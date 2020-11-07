---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 6f6653c9ba7f69c6bf2cc91d2517edb06fae7523
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920009"
---
# <span data-ttu-id="b22a3-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b22a3-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="b22a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b22a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b22a3-103">Ta bort en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="b22a3-103">Remove an Azure Search service.</span></span>

## <span data-ttu-id="b22a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b22a3-104">SYNTAX</span></span>

### <span data-ttu-id="b22a3-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b22a3-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b22a3-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b22a3-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b22a3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b22a3-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b22a3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b22a3-108">DESCRIPTION</span></span>
<span data-ttu-id="b22a3-109">Cmdleten **Remove-AzSearchService** tar bort en Azure Search-tjänst med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="b22a3-109">The **Remove-AzSearchService** cmdlet removes an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="b22a3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b22a3-110">EXAMPLES</span></span>

### <span data-ttu-id="b22a3-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b22a3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="b22a3-112">Exemplet tar bort en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="b22a3-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="b22a3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b22a3-113">PARAMETERS</span></span>

### <span data-ttu-id="b22a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22a3-114">-DefaultProfile</span></span>
<span data-ttu-id="b22a3-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b22a3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b22a3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b22a3-116">-Force</span></span>
<span data-ttu-id="b22a3-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b22a3-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b22a3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b22a3-118">-InputObject</span></span>
<span data-ttu-id="b22a3-119">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="b22a3-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b22a3-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b22a3-120">-Name</span></span>
<span data-ttu-id="b22a3-121">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="b22a3-121">Search Service name.</span></span>

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

### <span data-ttu-id="b22a3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b22a3-122">-PassThru</span></span>
<span data-ttu-id="b22a3-123">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="b22a3-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="b22a3-124">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="b22a3-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b22a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b22a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="b22a3-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b22a3-126">Resource Group name.</span></span>

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

### <span data-ttu-id="b22a3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b22a3-127">-ResourceId</span></span>
<span data-ttu-id="b22a3-128">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b22a3-128">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22a3-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b22a3-129">-Confirm</span></span>
<span data-ttu-id="b22a3-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b22a3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b22a3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b22a3-131">-WhatIf</span></span>
<span data-ttu-id="b22a3-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b22a3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b22a3-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b22a3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b22a3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22a3-134">CommonParameters</span></span>
<span data-ttu-id="b22a3-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b22a3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22a3-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b22a3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22a3-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b22a3-137">INPUTS</span></span>

### <span data-ttu-id="b22a3-138">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b22a3-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="b22a3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b22a3-139">System.String</span></span>

## <span data-ttu-id="b22a3-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b22a3-140">OUTPUTS</span></span>

### <span data-ttu-id="b22a3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b22a3-141">System.Boolean</span></span>

## <span data-ttu-id="b22a3-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b22a3-142">NOTES</span></span>

## <span data-ttu-id="b22a3-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b22a3-143">RELATED LINKS</span></span>

[<span data-ttu-id="b22a3-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b22a3-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="b22a3-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b22a3-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="b22a3-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b22a3-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

