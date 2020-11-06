---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 7c14b5c53cdffa51671a64ad40fe18a400ae6803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582736"
---
# <span data-ttu-id="94d8d-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="94d8d-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="94d8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="94d8d-103">Hämtar information om utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="94d8d-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94d8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94d8d-104">SYNTAX</span></span>

### <span data-ttu-id="94d8d-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="94d8d-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94d8d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="94d8d-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94d8d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="94d8d-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94d8d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94d8d-108">DESCRIPTION</span></span>
<span data-ttu-id="94d8d-109">Cmdleten **Get-AzureRmDataFactoryV2Trigger** hämtar information om utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="94d8d-109">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="94d8d-110">Om du anger namnet på en utlösare får cmdleten information om den utlösaren.</span><span class="sxs-lookup"><span data-stu-id="94d8d-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="94d8d-111">Om du inte anger ett namn får cmdleten information om alla utlösare i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="94d8d-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="94d8d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94d8d-112">EXAMPLES</span></span>

### <span data-ttu-id="94d8d-113">Exempel 1: få information om en viss utlösare</span><span class="sxs-lookup"><span data-stu-id="94d8d-113">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="94d8d-114">Hämtar en lista över alla utlösare som har skapats i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="94d8d-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="94d8d-115">Exempel 2: få information om alla utlösare</span><span class="sxs-lookup"><span data-stu-id="94d8d-115">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="94d8d-116">Hämtar en enkel utlösare som heter "ScheduledTrigger" i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="94d8d-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="94d8d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94d8d-117">PARAMETERS</span></span>

### <span data-ttu-id="94d8d-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="94d8d-118">-DataFactory</span></span>
<span data-ttu-id="94d8d-119">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="94d8d-119">The data factory object.</span></span>

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

### <span data-ttu-id="94d8d-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="94d8d-120">-DataFactoryName</span></span>
<span data-ttu-id="94d8d-121">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="94d8d-121">The data factory name.</span></span>

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

### <span data-ttu-id="94d8d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d8d-122">-DefaultProfile</span></span>
<span data-ttu-id="94d8d-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94d8d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94d8d-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="94d8d-124">-Name</span></span>
<span data-ttu-id="94d8d-125">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="94d8d-125">The trigger name.</span></span>

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

### <span data-ttu-id="94d8d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94d8d-126">-ResourceGroupName</span></span>
<span data-ttu-id="94d8d-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="94d8d-127">The resource group name.</span></span>

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

### <span data-ttu-id="94d8d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94d8d-128">-ResourceId</span></span>
<span data-ttu-id="94d8d-129">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="94d8d-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="94d8d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d8d-130">CommonParameters</span></span>
<span data-ttu-id="94d8d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94d8d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d8d-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d8d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d8d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94d8d-133">INPUTS</span></span>

### <span data-ttu-id="94d8d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="94d8d-134">System.String</span></span>

### <span data-ttu-id="94d8d-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="94d8d-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="94d8d-136">Parametrar: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="94d8d-136">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="94d8d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94d8d-137">OUTPUTS</span></span>

### <span data-ttu-id="94d8d-138">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="94d8d-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="94d8d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94d8d-139">NOTES</span></span>

## <span data-ttu-id="94d8d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94d8d-140">RELATED LINKS</span></span>

[<span data-ttu-id="94d8d-141">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="94d8d-141">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="94d8d-142">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="94d8d-142">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="94d8d-143">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="94d8d-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="94d8d-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="94d8d-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
