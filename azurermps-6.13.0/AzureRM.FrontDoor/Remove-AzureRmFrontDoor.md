---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
ms.openlocfilehash: 8eae5034080bd1035cfe7e8331ca015820688e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755199"
---
# <span data-ttu-id="72d14-101">Remove-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="72d14-101">Remove-AzureRmFrontDoor</span></span>

## <span data-ttu-id="72d14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72d14-102">SYNOPSIS</span></span>
<span data-ttu-id="72d14-103">Ta bort belastningsutjämnaren för främre dörrar</span><span class="sxs-lookup"><span data-stu-id="72d14-103">Remove Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72d14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72d14-104">SYNTAX</span></span>

### <span data-ttu-id="72d14-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="72d14-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72d14-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72d14-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72d14-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72d14-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72d14-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72d14-108">DESCRIPTION</span></span>
<span data-ttu-id="72d14-109">Cmdleten **Remove-AzureRmFrontDoor** tar bort en belastningsutjämnare för front dörr under den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="72d14-109">The **Remove-AzureRmFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="72d14-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72d14-110">EXAMPLES</span></span>

### <span data-ttu-id="72d14-111">Exempel 1: ta bort "frontdoor1" i resurs gruppen "RG1" under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="72d14-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="72d14-112">Ta bort "frontdoor1" i resurs gruppen "RG1" under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="72d14-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="72d14-113">Exempel 2: ta bort alla FrontDoors i resurs gruppen "RG1" under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="72d14-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="72d14-114">Ta bort alla FrontDoors i resurs gruppen "RG1" under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="72d14-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="72d14-115">Exempel 3: ta bort alla FrontDoors under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="72d14-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor | Remove-AzureRmFrontDoor
```

<span data-ttu-id="72d14-116">Ta bort alla FrontDoors under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="72d14-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="72d14-117">Exempel 4: ta bort alla FrontDoors med namnet "frontdoor1" under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="72d14-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="72d14-118">Ta bort alla FrontDoors med namnet "frontdoor1" under det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="72d14-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="72d14-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72d14-119">PARAMETERS</span></span>

### <span data-ttu-id="72d14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d14-120">-DefaultProfile</span></span>
<span data-ttu-id="72d14-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72d14-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72d14-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72d14-122">-InputObject</span></span>
<span data-ttu-id="72d14-123">Den främre dörr objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="72d14-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="72d14-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="72d14-124">-Name</span></span>
<span data-ttu-id="72d14-125">Namnet på den som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="72d14-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="72d14-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72d14-126">-PassThru</span></span>
<span data-ttu-id="72d14-127">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="72d14-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="72d14-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72d14-128">-ResourceGroupName</span></span>
<span data-ttu-id="72d14-129">Den resurs grupp som front dörren tillhör.</span><span class="sxs-lookup"><span data-stu-id="72d14-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="72d14-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72d14-130">-ResourceId</span></span>
<span data-ttu-id="72d14-131">Resurs-ID för den främre dörren som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="72d14-131">Resource Id of the Front Door to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72d14-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="72d14-132">-Confirm</span></span>
<span data-ttu-id="72d14-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="72d14-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72d14-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72d14-134">-WhatIf</span></span>
<span data-ttu-id="72d14-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="72d14-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72d14-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="72d14-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72d14-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d14-137">CommonParameters</span></span>
<span data-ttu-id="72d14-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72d14-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d14-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72d14-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d14-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72d14-140">INPUTS</span></span>

### <span data-ttu-id="72d14-141">Microsoft. Azure. commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="72d14-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="72d14-142">System. String</span><span class="sxs-lookup"><span data-stu-id="72d14-142">System.String</span></span>

### <span data-ttu-id="72d14-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="72d14-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="72d14-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72d14-144">OUTPUTS</span></span>

### <span data-ttu-id="72d14-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72d14-145">System.Boolean</span></span>

## <span data-ttu-id="72d14-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72d14-146">NOTES</span></span>

## <span data-ttu-id="72d14-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72d14-147">RELATED LINKS</span></span>

<span data-ttu-id="72d14-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="72d14-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span></span>
