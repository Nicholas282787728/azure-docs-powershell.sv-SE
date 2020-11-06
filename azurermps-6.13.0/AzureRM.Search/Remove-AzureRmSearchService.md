---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
ms.openlocfilehash: c558a5d7228253e0a76b0d47fb21f581b4e06f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580699"
---
# <span data-ttu-id="6d055-101">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="6d055-101">Remove-AzureRmSearchService</span></span>

## <span data-ttu-id="6d055-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d055-102">SYNOPSIS</span></span>
<span data-ttu-id="6d055-103">Ta bort en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="6d055-103">Remove an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d055-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d055-104">SYNTAX</span></span>

### <span data-ttu-id="6d055-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6d055-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d055-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d055-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d055-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d055-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d055-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d055-108">DESCRIPTION</span></span>
<span data-ttu-id="6d055-109">Cmdleten **Remove-AzureRmSearchService** tar bort en Azure Search-tjänst med angiven paramters.</span><span class="sxs-lookup"><span data-stu-id="6d055-109">The **Remove-AzureRmSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="6d055-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d055-110">EXAMPLES</span></span>

### <span data-ttu-id="6d055-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6d055-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="6d055-112">Exemplet tar bort en Azure Search-tjänst.</span><span class="sxs-lookup"><span data-stu-id="6d055-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="6d055-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d055-113">PARAMETERS</span></span>

### <span data-ttu-id="6d055-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d055-114">-DefaultProfile</span></span>
<span data-ttu-id="6d055-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d055-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d055-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6d055-116">-Force</span></span>
<span data-ttu-id="6d055-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6d055-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6d055-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d055-118">-InputObject</span></span>
<span data-ttu-id="6d055-119">Objekt för Sök tjänst.</span><span class="sxs-lookup"><span data-stu-id="6d055-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="6d055-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d055-120">-Name</span></span>
<span data-ttu-id="6d055-121">Sök tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="6d055-121">Search Service name.</span></span>

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

### <span data-ttu-id="6d055-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d055-122">-PassThru</span></span>
<span data-ttu-id="6d055-123">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="6d055-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="6d055-124">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="6d055-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6d055-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d055-125">-ResourceGroupName</span></span>
<span data-ttu-id="6d055-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6d055-126">Resource Group name.</span></span>

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

### <span data-ttu-id="6d055-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d055-127">-ResourceId</span></span>
<span data-ttu-id="6d055-128">Sök tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6d055-128">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="6d055-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6d055-129">-Confirm</span></span>
<span data-ttu-id="6d055-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6d055-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d055-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d055-131">-WhatIf</span></span>
<span data-ttu-id="6d055-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d055-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d055-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6d055-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d055-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d055-134">CommonParameters</span></span>
<span data-ttu-id="6d055-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d055-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d055-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d055-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d055-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d055-137">INPUTS</span></span>

### <span data-ttu-id="6d055-138">Microsoft. Azure. commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="6d055-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="6d055-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6d055-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="6d055-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6d055-140">System.String</span></span>

## <span data-ttu-id="6d055-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d055-141">OUTPUTS</span></span>

### <span data-ttu-id="6d055-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d055-142">System.Boolean</span></span>

## <span data-ttu-id="6d055-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d055-143">NOTES</span></span>

## <span data-ttu-id="6d055-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d055-144">RELATED LINKS</span></span>

[<span data-ttu-id="6d055-145">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="6d055-145">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="6d055-146">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="6d055-146">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="6d055-147">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="6d055-147">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

