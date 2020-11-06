---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: bc60bbb5b48c4022e7db6a95e26a1f43ef891ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585667"
---
# <span data-ttu-id="9ef10-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9ef10-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="9ef10-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ef10-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef10-103">Hämtar information om utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="9ef10-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ef10-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ef10-104">SYNTAX</span></span>

### <span data-ttu-id="9ef10-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="9ef10-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="9ef10-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9ef10-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="9ef10-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ef10-107">DESCRIPTION</span></span>
<span data-ttu-id="9ef10-108">Cmdleten **Get-AzureRmDataFactoryV2Trigger** hämtar information om utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="9ef10-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="9ef10-109">Om du anger namnet på en utlösare får cmdleten information om den utlösaren.</span><span class="sxs-lookup"><span data-stu-id="9ef10-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="9ef10-110">Om du inte anger ett namn får cmdleten information om alla utlösare i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="9ef10-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>


## <span data-ttu-id="9ef10-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ef10-111">EXAMPLES</span></span>

### <span data-ttu-id="9ef10-112">Exempel 1: få information om en viss utlösare</span><span class="sxs-lookup"><span data-stu-id="9ef10-112">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="9ef10-113">Hämtar en lista över alla utlösare som har skapats i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="9ef10-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="9ef10-114">Exempel 2: få information om alla utlösare</span><span class="sxs-lookup"><span data-stu-id="9ef10-114">Example 2: Get information about all triggers</span></span>

```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="9ef10-115">Hämtar en enkel utlösare som heter "ScheduledTrigger" i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="9ef10-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="9ef10-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ef10-116">PARAMETERS</span></span>

### <span data-ttu-id="9ef10-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9ef10-117">-DataFactory</span></span>
<span data-ttu-id="9ef10-118">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="9ef10-118">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ef10-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9ef10-119">-DataFactoryName</span></span>
<span data-ttu-id="9ef10-120">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="9ef10-120">The data factory name.</span></span>

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

### <span data-ttu-id="9ef10-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9ef10-121">-Name</span></span>
<span data-ttu-id="9ef10-122">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="9ef10-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ef10-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef10-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ef10-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9ef10-124">The resource group name.</span></span>

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

## <span data-ttu-id="9ef10-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ef10-125">INPUTS</span></span>

### <span data-ttu-id="9ef10-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9ef10-126">System.String</span></span>
<span data-ttu-id="9ef10-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9ef10-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="9ef10-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ef10-128">OUTPUTS</span></span>

### <span data-ttu-id="9ef10-129">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9ef10-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="9ef10-130">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="9ef10-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="9ef10-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ef10-131">NOTES</span></span>

## <span data-ttu-id="9ef10-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ef10-132">RELATED LINKS</span></span>
[<span data-ttu-id="9ef10-133">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9ef10-133">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9ef10-134">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9ef10-134">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9ef10-135">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9ef10-135">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9ef10-136">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9ef10-136">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
