---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 771097c11aceabb9bd2011c6024e469a37a39f4e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573643"
---
# <span data-ttu-id="1db3b-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1db3b-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="1db3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1db3b-102">SYNOPSIS</span></span>
<span data-ttu-id="1db3b-103">Tar bort en utlösare från en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="1db3b-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1db3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1db3b-104">SYNTAX</span></span>

### <span data-ttu-id="1db3b-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="1db3b-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1db3b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1db3b-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1db3b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1db3b-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1db3b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1db3b-108">DESCRIPTION</span></span>
<span data-ttu-id="1db3b-109">Cmdleten **Remove-AzureRmDataFactoryV2Trigger** tar bort en utlösare från en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="1db3b-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="1db3b-110">Om parametern _Force_ anges frågar inte cmdleten innan utlösaren tas bort.</span><span class="sxs-lookup"><span data-stu-id="1db3b-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="1db3b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1db3b-111">EXAMPLES</span></span>

### <span data-ttu-id="1db3b-112">Exempel 1: ta bort en utlösare</span><span class="sxs-lookup"><span data-stu-id="1db3b-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="1db3b-113">Ta bort en utlösare som heter "ScheduledTrigger" från data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="1db3b-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="1db3b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1db3b-114">PARAMETERS</span></span>

### <span data-ttu-id="1db3b-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1db3b-115">-Confirm</span></span>
<span data-ttu-id="1db3b-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1db3b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1db3b-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1db3b-117">-DataFactoryName</span></span>
<span data-ttu-id="1db3b-118">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="1db3b-118">The data factory name.</span></span>

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

### <span data-ttu-id="1db3b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1db3b-119">-Force</span></span>
<span data-ttu-id="1db3b-120">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1db3b-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1db3b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="1db3b-121">-Name</span></span>
<span data-ttu-id="1db3b-122">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="1db3b-122">The trigger name.</span></span>

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

### <span data-ttu-id="1db3b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1db3b-123">-ResourceGroupName</span></span>
<span data-ttu-id="1db3b-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1db3b-124">The resource group name.</span></span>

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

### <span data-ttu-id="1db3b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1db3b-125">-ResourceId</span></span>
<span data-ttu-id="1db3b-126">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="1db3b-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1db3b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1db3b-127">-InputObject</span></span>
<span data-ttu-id="1db3b-128">Det Utlös ande objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1db3b-128">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="1db3b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1db3b-129">-WhatIf</span></span>
<span data-ttu-id="1db3b-130">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1db3b-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1db3b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db3b-131">-DefaultProfile</span></span>
<span data-ttu-id="1db3b-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1db3b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1db3b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db3b-133">CommonParameters</span></span>
<span data-ttu-id="1db3b-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1db3b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db3b-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1db3b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db3b-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1db3b-136">INPUTS</span></span>

### <span data-ttu-id="1db3b-137">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="1db3b-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="1db3b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1db3b-138">System.String</span></span>

## <span data-ttu-id="1db3b-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1db3b-139">OUTPUTS</span></span>

### <span data-ttu-id="1db3b-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="1db3b-140">System.Object</span></span>

## <span data-ttu-id="1db3b-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1db3b-141">NOTES</span></span>

## <span data-ttu-id="1db3b-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1db3b-142">RELATED LINKS</span></span>

[<span data-ttu-id="1db3b-143">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1db3b-143">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1db3b-144">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1db3b-144">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1db3b-145">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1db3b-145">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1db3b-146">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1db3b-146">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

