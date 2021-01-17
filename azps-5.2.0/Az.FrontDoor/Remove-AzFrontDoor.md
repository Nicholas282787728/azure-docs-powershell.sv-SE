---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392603"
---
# <span data-ttu-id="b3298-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="b3298-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="b3298-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3298-102">SYNOPSIS</span></span>
<span data-ttu-id="b3298-103">Ta bort belastningsutjämnaren för främre dörrar</span><span class="sxs-lookup"><span data-stu-id="b3298-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="b3298-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3298-104">SYNTAX</span></span>

### <span data-ttu-id="b3298-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b3298-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3298-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3298-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3298-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3298-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3298-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3298-108">DESCRIPTION</span></span>
<span data-ttu-id="b3298-109">Cmdleten **Remove-AzFrontDoor** tar bort en belastningsutjämnare för front dörr under den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="b3298-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="b3298-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3298-110">EXAMPLES</span></span>

### <span data-ttu-id="b3298-111">Exempel 1: ta bort "frontdoor1" i resurs gruppen "RG1" under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b3298-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="b3298-112">Ta bort "frontdoor1" i resurs gruppen "RG1" under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b3298-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="b3298-113">Exempel 2: ta bort alla FrontDoors i resurs gruppen "RG1" under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b3298-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="b3298-114">Ta bort alla FrontDoors i resurs gruppen "RG1" under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b3298-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="b3298-115">Exempel 3: ta bort alla FrontDoors under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b3298-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="b3298-116">Ta bort alla FrontDoors under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b3298-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="b3298-117">Exempel 4: ta bort alla FrontDoors med namnet "frontdoor1" under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b3298-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="b3298-118">Ta bort alla FrontDoors med namnet "frontdoor1" under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="b3298-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="b3298-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3298-119">PARAMETERS</span></span>

### <span data-ttu-id="b3298-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3298-120">-DefaultProfile</span></span>
<span data-ttu-id="b3298-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3298-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3298-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3298-122">-InputObject</span></span>
<span data-ttu-id="b3298-123">Den främre dörr objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b3298-123">The Front Door object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3298-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="b3298-124">-Name</span></span>
<span data-ttu-id="b3298-125">Namnet på den som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b3298-125">The name of the Front Door to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3298-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3298-126">-PassThru</span></span>
<span data-ttu-id="b3298-127">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="b3298-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="b3298-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3298-128">-ResourceGroupName</span></span>
<span data-ttu-id="b3298-129">Den resurs grupp som front dörren tillhör.</span><span class="sxs-lookup"><span data-stu-id="b3298-129">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3298-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3298-130">-ResourceId</span></span>
<span data-ttu-id="b3298-131">Resurs-ID för den främre dörren som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="b3298-131">Resource Id of the Front Door to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3298-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b3298-132">-Confirm</span></span>
<span data-ttu-id="b3298-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b3298-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3298-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3298-134">-WhatIf</span></span>
<span data-ttu-id="b3298-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b3298-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3298-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b3298-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3298-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3298-137">CommonParameters</span></span>
<span data-ttu-id="b3298-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3298-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3298-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3298-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3298-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3298-140">INPUTS</span></span>

### <span data-ttu-id="b3298-141">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="b3298-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="b3298-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b3298-142">System.String</span></span>

## <span data-ttu-id="b3298-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3298-143">OUTPUTS</span></span>

### <span data-ttu-id="b3298-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3298-144">System.Boolean</span></span>

## <span data-ttu-id="b3298-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3298-145">NOTES</span></span>

## <span data-ttu-id="b3298-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3298-146">RELATED LINKS</span></span>

<span data-ttu-id="b3298-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="b3298-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>