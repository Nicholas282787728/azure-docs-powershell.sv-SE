---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523647"
---
# <span data-ttu-id="4341c-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="4341c-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="4341c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4341c-102">SYNOPSIS</span></span>
<span data-ttu-id="4341c-103">Skapa en ny regel motor konfiguration för en viss front dörr.</span><span class="sxs-lookup"><span data-stu-id="4341c-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="4341c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4341c-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4341c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4341c-105">DESCRIPTION</span></span>
<span data-ttu-id="4341c-106">Skapa en ny regel motor konfiguration för en viss front dörr.</span><span class="sxs-lookup"><span data-stu-id="4341c-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="4341c-107">Använd cmdlet "New-AzFrontDoorRulesEngineRule" för att skapa regler för regel motor för att passera till parametern "-Rules" för denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4341c-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="4341c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4341c-108">EXAMPLES</span></span>

### <span data-ttu-id="4341c-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4341c-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="4341c-110">Skapa en ny regel motor konfiguration för angiven främre dörr.</span><span class="sxs-lookup"><span data-stu-id="4341c-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="4341c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4341c-111">PARAMETERS</span></span>

### <span data-ttu-id="4341c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4341c-112">-DefaultProfile</span></span>
<span data-ttu-id="4341c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4341c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4341c-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="4341c-114">-FrontDoorName</span></span>
<span data-ttu-id="4341c-115">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="4341c-115">Front Door name.</span></span>

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

### <span data-ttu-id="4341c-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="4341c-116">-Name</span></span>
<span data-ttu-id="4341c-117">Namn på regel motor.</span><span class="sxs-lookup"><span data-stu-id="4341c-117">Rules engine name.</span></span>

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

### <span data-ttu-id="4341c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4341c-118">-ResourceGroupName</span></span>
<span data-ttu-id="4341c-119">Namnet på den resurs grupp som ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="4341c-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="4341c-120">-Regel</span><span class="sxs-lookup"><span data-stu-id="4341c-120">-Rule</span></span>
<span data-ttu-id="4341c-121">En lista med regler som definierar en viss regel motor konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4341c-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="4341c-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4341c-122">-Confirm</span></span>
<span data-ttu-id="4341c-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4341c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4341c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4341c-124">-WhatIf</span></span>
<span data-ttu-id="4341c-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4341c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4341c-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4341c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4341c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4341c-127">CommonParameters</span></span>
<span data-ttu-id="4341c-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4341c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4341c-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4341c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4341c-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4341c-130">INPUTS</span></span>

### <span data-ttu-id="4341c-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="4341c-131">None</span></span>

## <span data-ttu-id="4341c-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4341c-132">OUTPUTS</span></span>

### <span data-ttu-id="4341c-133">Microsoft. Azure. commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="4341c-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="4341c-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4341c-134">NOTES</span></span>

## <span data-ttu-id="4341c-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4341c-135">RELATED LINKS</span></span>
