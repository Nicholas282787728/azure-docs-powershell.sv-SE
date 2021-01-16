---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: cf98121f535f60c7d1ddc3b29e33f10fd8f29842
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523631"
---
# <span data-ttu-id="ada2a-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="ada2a-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="ada2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ada2a-102">SYNOPSIS</span></span>
<span data-ttu-id="ada2a-103">Uppdatera en regel motor.</span><span class="sxs-lookup"><span data-stu-id="ada2a-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="ada2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ada2a-104">SYNTAX</span></span>

### <span data-ttu-id="ada2a-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ada2a-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ada2a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ada2a-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ada2a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ada2a-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ada2a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ada2a-108">DESCRIPTION</span></span>
<span data-ttu-id="ada2a-109">Uppdatera en regel motor.</span><span class="sxs-lookup"><span data-stu-id="ada2a-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="ada2a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ada2a-110">EXAMPLES</span></span>

### <span data-ttu-id="ada2a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ada2a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}

PS C:\> $rulesEngineRule2 = New-AzFrontDoorRulesEngineRuleObject -Name rules2 -Priority 3 -Action $rulesEngineAction
PS C:\AFD\azure-powershell\artifacts\Debug\Az.FrontDoor> Set-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1, $rulesEngineRule2

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1, rules2}
```

<span data-ttu-id="ada2a-112">Skaffa en befintlig regel motor konfiguration och Lägg till en annan regel motor regler i den.</span><span class="sxs-lookup"><span data-stu-id="ada2a-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="ada2a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ada2a-113">PARAMETERS</span></span>

### <span data-ttu-id="ada2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada2a-114">-DefaultProfile</span></span>
<span data-ttu-id="ada2a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ada2a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ada2a-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="ada2a-116">-FrontDoorName</span></span>
<span data-ttu-id="ada2a-117">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="ada2a-117">Front Door name.</span></span>

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

### <span data-ttu-id="ada2a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ada2a-118">-InputObject</span></span>
<span data-ttu-id="ada2a-119">Prestandaobjektet att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="ada2a-119">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="ada2a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ada2a-120">-Name</span></span>
<span data-ttu-id="ada2a-121">Namn på regel motor.</span><span class="sxs-lookup"><span data-stu-id="ada2a-121">Rules engine name.</span></span>

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

### <span data-ttu-id="ada2a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada2a-122">-ResourceGroupName</span></span>
<span data-ttu-id="ada2a-123">Namnet på den resurs grupp som ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="ada2a-123">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="ada2a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ada2a-124">-ResourceId</span></span>
<span data-ttu-id="ada2a-125">Resurs-ID för RulesEngine som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="ada2a-125">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="ada2a-126">-Regel</span><span class="sxs-lookup"><span data-stu-id="ada2a-126">-Rule</span></span>
<span data-ttu-id="ada2a-127">En lista med regler som definierar en viss regel motor konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ada2a-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada2a-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ada2a-128">-Confirm</span></span>
<span data-ttu-id="ada2a-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ada2a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ada2a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ada2a-130">-WhatIf</span></span>
<span data-ttu-id="ada2a-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ada2a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ada2a-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ada2a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ada2a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada2a-133">CommonParameters</span></span>
<span data-ttu-id="ada2a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada2a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada2a-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ada2a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada2a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ada2a-136">INPUTS</span></span>

### <span data-ttu-id="ada2a-137">Microsoft. Azure. commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="ada2a-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="ada2a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ada2a-138">System.String</span></span>

## <span data-ttu-id="ada2a-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ada2a-139">OUTPUTS</span></span>

### <span data-ttu-id="ada2a-140">Microsoft. Azure. commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="ada2a-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="ada2a-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ada2a-141">NOTES</span></span>

## <span data-ttu-id="ada2a-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ada2a-142">RELATED LINKS</span></span>
