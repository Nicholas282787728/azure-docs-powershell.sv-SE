---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: e5afbdd389d1ee9e1b74895743ed47ceed0b4ae9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744772"
---
# <span data-ttu-id="fb747-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fb747-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="fb747-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb747-102">SYNOPSIS</span></span>
<span data-ttu-id="fb747-103">Hämtar information om utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="fb747-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="fb747-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb747-104">SYNTAX</span></span>

### <span data-ttu-id="fb747-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="fb747-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb747-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fb747-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb747-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb747-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb747-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb747-108">DESCRIPTION</span></span>
<span data-ttu-id="fb747-109">Cmdleten **Get-AzDataFactoryV2Trigger** hämtar information om utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="fb747-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="fb747-110">Om du anger namnet på en utlösare får cmdleten information om den utlösaren.</span><span class="sxs-lookup"><span data-stu-id="fb747-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="fb747-111">Om du inte anger ett namn får cmdleten information om alla utlösare i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="fb747-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="fb747-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb747-112">EXAMPLES</span></span>

### <span data-ttu-id="fb747-113">Exempel 1: få information om en viss utlösare</span><span class="sxs-lookup"><span data-stu-id="fb747-113">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="fb747-114">Hämtar en lista över alla utlösare som har skapats i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="fb747-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="fb747-115">Exempel 2: få information om alla utlösare</span><span class="sxs-lookup"><span data-stu-id="fb747-115">Example 2: Get information about all triggers</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="fb747-116">Hämtar en enkel utlösare som heter "ScheduledTrigger" i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="fb747-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="fb747-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb747-117">PARAMETERS</span></span>

### <span data-ttu-id="fb747-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fb747-118">-DataFactory</span></span>
<span data-ttu-id="fb747-119">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="fb747-119">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb747-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fb747-120">-DataFactoryName</span></span>
<span data-ttu-id="fb747-121">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="fb747-121">The data factory name.</span></span>

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

### <span data-ttu-id="fb747-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb747-122">-DefaultProfile</span></span>
<span data-ttu-id="fb747-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb747-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb747-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb747-124">-Name</span></span>
<span data-ttu-id="fb747-125">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="fb747-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb747-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb747-126">-ResourceGroupName</span></span>
<span data-ttu-id="fb747-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fb747-127">The resource group name.</span></span>

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

### <span data-ttu-id="fb747-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb747-128">-ResourceId</span></span>
<span data-ttu-id="fb747-129">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="fb747-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fb747-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb747-130">CommonParameters</span></span>
<span data-ttu-id="fb747-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb747-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb747-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb747-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb747-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb747-133">INPUTS</span></span>

### <span data-ttu-id="fb747-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fb747-134">System.String</span></span>

### <span data-ttu-id="fb747-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fb747-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="fb747-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb747-136">OUTPUTS</span></span>

### <span data-ttu-id="fb747-137">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="fb747-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="fb747-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb747-138">NOTES</span></span>

## <span data-ttu-id="fb747-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb747-139">RELATED LINKS</span></span>

[<span data-ttu-id="fb747-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fb747-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fb747-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fb747-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fb747-142">Stopp-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fb747-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fb747-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fb747-143">Remove-AzDataFactoryV2Trigger</span></span>]()