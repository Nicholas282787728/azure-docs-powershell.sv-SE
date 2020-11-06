---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 3d5db6b7aa1b7c2ffdd63292696230e2d12bd4c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574987"
---
# <span data-ttu-id="57875-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57875-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="57875-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57875-102">SYNOPSIS</span></span>
<span data-ttu-id="57875-103">Hämtar information om utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="57875-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57875-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57875-104">SYNTAX</span></span>

### <span data-ttu-id="57875-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="57875-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57875-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="57875-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57875-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57875-107">DESCRIPTION</span></span>
<span data-ttu-id="57875-108">Cmdleten **Get-AzureRmDataFactoryV2Trigger** hämtar information om utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="57875-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="57875-109">Om du anger namnet på en utlösare får cmdleten information om den utlösaren.</span><span class="sxs-lookup"><span data-stu-id="57875-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="57875-110">Om du inte anger ett namn får cmdleten information om alla utlösare i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="57875-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="57875-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57875-111">EXAMPLES</span></span>

### <span data-ttu-id="57875-112">Exempel 1: få information om en viss utlösare</span><span class="sxs-lookup"><span data-stu-id="57875-112">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="57875-113">Hämtar en lista över alla utlösare som har skapats i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="57875-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="57875-114">Exempel 2: få information om alla utlösare</span><span class="sxs-lookup"><span data-stu-id="57875-114">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="57875-115">Hämtar en enkel utlösare som heter "ScheduledTrigger" i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="57875-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="57875-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57875-116">PARAMETERS</span></span>

### <span data-ttu-id="57875-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="57875-117">-DataFactory</span></span>
<span data-ttu-id="57875-118">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="57875-118">The data factory object.</span></span>

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

### <span data-ttu-id="57875-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="57875-119">-DataFactoryName</span></span>
<span data-ttu-id="57875-120">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="57875-120">The data factory name.</span></span>

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

### <span data-ttu-id="57875-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="57875-121">-Name</span></span>
<span data-ttu-id="57875-122">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="57875-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57875-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57875-123">-ResourceGroupName</span></span>
<span data-ttu-id="57875-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="57875-124">The resource group name.</span></span>

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

### <span data-ttu-id="57875-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57875-125">-DefaultProfile</span></span>
<span data-ttu-id="57875-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="57875-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57875-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57875-127">CommonParameters</span></span>
<span data-ttu-id="57875-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57875-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57875-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57875-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57875-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57875-130">INPUTS</span></span>

### <span data-ttu-id="57875-131">System. String</span><span class="sxs-lookup"><span data-stu-id="57875-131">System.String</span></span>
<span data-ttu-id="57875-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="57875-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="57875-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57875-133">OUTPUTS</span></span>

### <span data-ttu-id="57875-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="57875-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="57875-135">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="57875-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="57875-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57875-136">NOTES</span></span>

## <span data-ttu-id="57875-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57875-137">RELATED LINKS</span></span>

[<span data-ttu-id="57875-138">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57875-138">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="57875-139">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57875-139">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="57875-140">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57875-140">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="57875-141">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57875-141">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
