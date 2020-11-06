---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8bf4a713784b367363e4f1f9167cfb144d06c0d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586551"
---
# <span data-ttu-id="e8e95-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e8e95-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="e8e95-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8e95-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e95-103">Skapar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="e8e95-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8e95-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8e95-104">SYNTAX</span></span>

### <span data-ttu-id="e8e95-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="e8e95-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e8e95-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e95-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e8e95-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8e95-107">DESCRIPTION</span></span>

<span data-ttu-id="e8e95-108">Cmdleten **set-AzureRmDataFactoryV2Trigger** skapar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="e8e95-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="e8e95-109">Om du anger ett namn för en trigger som redan finns uppmanas du att bekräfta i cmdleten innan utlösaren byts ut.</span><span class="sxs-lookup"><span data-stu-id="e8e95-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="e8e95-110">Om du anger parametern _Force_ ersätter cmdlet den befintliga utlösaren utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e8e95-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="e8e95-111">Utlösare skapas i tillståndet "stoppad", vilket innebär att de inte omedelbart påbörjar samtals ledningar som de refererar till.</span><span class="sxs-lookup"><span data-stu-id="e8e95-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="e8e95-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8e95-112">EXAMPLES</span></span>

### <span data-ttu-id="e8e95-113">Exempel 1: skapa en utlösare</span><span class="sxs-lookup"><span data-stu-id="e8e95-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

```

<span data-ttu-id="e8e95-114">Skapa en ny utlösare som heter "ScheduledTrigger" i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="e8e95-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="e8e95-115">Utlösaren skapas i tillståndet "stoppad", vilket innebär att den inte startas omedelbart.</span><span class="sxs-lookup"><span data-stu-id="e8e95-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="e8e95-116">En utlösare kan börja använda `Start-AzureRmDataFactoryV2Trigger` cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e8e95-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="e8e95-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8e95-117">PARAMETERS</span></span>

### <span data-ttu-id="e8e95-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e8e95-118">-Confirm</span></span>
<span data-ttu-id="e8e95-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e8e95-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e95-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e8e95-120">-DataFactoryName</span></span>
<span data-ttu-id="e8e95-121">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="e8e95-121">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e95-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e8e95-122">-DefinitionFile</span></span>
<span data-ttu-id="e8e95-123">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="e8e95-123">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e95-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e8e95-124">-Force</span></span>
<span data-ttu-id="e8e95-125">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e8e95-125">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8e95-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="e8e95-126">-Name</span></span>
<span data-ttu-id="e8e95-127">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="e8e95-127">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e95-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8e95-128">-ResourceGroupName</span></span>
<span data-ttu-id="e8e95-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e8e95-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e95-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e95-130">-ResourceId</span></span>
<span data-ttu-id="e8e95-131">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="e8e95-131">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e95-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8e95-132">-WhatIf</span></span>
<span data-ttu-id="e8e95-133">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e8e95-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="e8e95-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8e95-134">INPUTS</span></span>

### <span data-ttu-id="e8e95-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e8e95-135">System.String</span></span>


## <span data-ttu-id="e8e95-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8e95-136">OUTPUTS</span></span>

### <span data-ttu-id="e8e95-137">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="e8e95-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="e8e95-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8e95-138">NOTES</span></span>

## <span data-ttu-id="e8e95-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8e95-139">RELATED LINKS</span></span>
[<span data-ttu-id="e8e95-140">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e8e95-140">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e8e95-141">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e8e95-141">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e8e95-142">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e8e95-142">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="e8e95-143">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="e8e95-143">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
