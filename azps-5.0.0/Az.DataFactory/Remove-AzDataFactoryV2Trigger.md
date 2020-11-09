---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320871"
---
# <span data-ttu-id="89428-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="89428-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="89428-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89428-102">SYNOPSIS</span></span>
<span data-ttu-id="89428-103">Tar bort en utlösare från en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="89428-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="89428-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89428-104">SYNTAX</span></span>

### <span data-ttu-id="89428-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="89428-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89428-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="89428-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89428-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="89428-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89428-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89428-108">DESCRIPTION</span></span>
<span data-ttu-id="89428-109">Cmdleten **Remove-AzDataFactoryV2Trigger** tar bort en utlösare från en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="89428-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="89428-110">Om parametern _Force_ anges frågar inte cmdleten innan utlösaren tas bort.</span><span class="sxs-lookup"><span data-stu-id="89428-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="89428-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89428-111">EXAMPLES</span></span>

### <span data-ttu-id="89428-112">Exempel 1: ta bort en utlösare</span><span class="sxs-lookup"><span data-stu-id="89428-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="89428-113">Ta bort en utlösare som heter "ScheduledTrigger" från data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="89428-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="89428-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89428-114">PARAMETERS</span></span>

### <span data-ttu-id="89428-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="89428-115">-DataFactoryName</span></span>
<span data-ttu-id="89428-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="89428-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89428-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89428-117">-DefaultProfile</span></span>
<span data-ttu-id="89428-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89428-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89428-119">-Force</span><span class="sxs-lookup"><span data-stu-id="89428-119">-Force</span></span>
<span data-ttu-id="89428-120">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="89428-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="89428-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89428-121">-InputObject</span></span>
<span data-ttu-id="89428-122">Det Utlös ande objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="89428-122">The Trigger object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89428-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="89428-123">-Name</span></span>
<span data-ttu-id="89428-124">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="89428-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89428-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89428-125">-ResourceGroupName</span></span>
<span data-ttu-id="89428-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="89428-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89428-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89428-127">-ResourceId</span></span>
<span data-ttu-id="89428-128">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="89428-128">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89428-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="89428-129">-Confirm</span></span>
<span data-ttu-id="89428-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89428-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89428-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89428-131">-WhatIf</span></span>
<span data-ttu-id="89428-132">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89428-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="89428-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89428-133">CommonParameters</span></span>
<span data-ttu-id="89428-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89428-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89428-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89428-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89428-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89428-136">INPUTS</span></span>

### <span data-ttu-id="89428-137">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="89428-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="89428-138">System. String</span><span class="sxs-lookup"><span data-stu-id="89428-138">System.String</span></span>

## <span data-ttu-id="89428-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89428-139">OUTPUTS</span></span>

### <span data-ttu-id="89428-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89428-140">System.Boolean</span></span>

## <span data-ttu-id="89428-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89428-141">NOTES</span></span>

## <span data-ttu-id="89428-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89428-142">RELATED LINKS</span></span>

[<span data-ttu-id="89428-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="89428-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="89428-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="89428-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="89428-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="89428-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="89428-146">Stopp-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="89428-146">Stop-AzDataFactoryV2Trigger</span></span>]()

