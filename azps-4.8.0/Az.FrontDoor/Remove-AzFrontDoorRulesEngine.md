---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100980"
---
# <span data-ttu-id="8b9c5-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="8b9c5-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="8b9c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b9c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8b9c5-103">Ta bort regel motorn från Front dörren</span><span class="sxs-lookup"><span data-stu-id="8b9c5-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="8b9c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b9c5-104">SYNTAX</span></span>

### <span data-ttu-id="8b9c5-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8b9c5-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b9c5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b9c5-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b9c5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b9c5-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b9c5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b9c5-108">DESCRIPTION</span></span>
<span data-ttu-id="8b9c5-109">Ta bort regel motorn från Front dörren</span><span class="sxs-lookup"><span data-stu-id="8b9c5-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="8b9c5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b9c5-110">EXAMPLES</span></span>

### <span data-ttu-id="8b9c5-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8b9c5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="8b9c5-112">Ta bort regel motor konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8b9c5-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="8b9c5-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8b9c5-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="8b9c5-114">Förväntat resultat när du tar bort en regel motor konfiguration som inte finns.</span><span class="sxs-lookup"><span data-stu-id="8b9c5-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="8b9c5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b9c5-115">PARAMETERS</span></span>

### <span data-ttu-id="8b9c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b9c5-116">-DefaultProfile</span></span>
<span data-ttu-id="8b9c5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b9c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b9c5-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8b9c5-118">-FrontDoorName</span></span>
<span data-ttu-id="8b9c5-119">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="8b9c5-119">Front Door name.</span></span>

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

### <span data-ttu-id="8b9c5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b9c5-120">-InputObject</span></span>
<span data-ttu-id="8b9c5-121">Prestandaobjektet att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="8b9c5-121">The Rules Engine object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b9c5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b9c5-122">-Name</span></span>
<span data-ttu-id="8b9c5-123">Namn på regel motor.</span><span class="sxs-lookup"><span data-stu-id="8b9c5-123">Rules engine name.</span></span>

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

### <span data-ttu-id="8b9c5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b9c5-124">-PassThru</span></span>
<span data-ttu-id="8b9c5-125">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="8b9c5-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="8b9c5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b9c5-126">-ResourceGroupName</span></span>
<span data-ttu-id="8b9c5-127">Namnet på den resurs grupp som ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="8b9c5-127">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="8b9c5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b9c5-128">-ResourceId</span></span>
<span data-ttu-id="8b9c5-129">Resurs-ID för RulesEngine som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="8b9c5-129">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="8b9c5-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b9c5-130">-Confirm</span></span>
<span data-ttu-id="8b9c5-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b9c5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b9c5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b9c5-132">-WhatIf</span></span>
<span data-ttu-id="8b9c5-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b9c5-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b9c5-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b9c5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b9c5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b9c5-135">CommonParameters</span></span>
<span data-ttu-id="8b9c5-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b9c5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b9c5-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b9c5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b9c5-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b9c5-138">INPUTS</span></span>

### <span data-ttu-id="8b9c5-139">Microsoft. Azure. commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="8b9c5-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="8b9c5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8b9c5-140">System.String</span></span>

## <span data-ttu-id="8b9c5-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b9c5-141">OUTPUTS</span></span>

### <span data-ttu-id="8b9c5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b9c5-142">System.Boolean</span></span>

## <span data-ttu-id="8b9c5-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b9c5-143">NOTES</span></span>

## <span data-ttu-id="8b9c5-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b9c5-144">RELATED LINKS</span></span>
