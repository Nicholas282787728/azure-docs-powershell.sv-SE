---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526314"
---
# <span data-ttu-id="9a9f2-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="9a9f2-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="9a9f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9a9f2-103">Abonnera på händelse utlösare för externa tjänst händelser.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="9a9f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a9f2-104">SYNTAX</span></span>

### <span data-ttu-id="9a9f2-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="9a9f2-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a9f2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9a9f2-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a9f2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a9f2-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a9f2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a9f2-108">DESCRIPTION</span></span>
<span data-ttu-id="9a9f2-109">Det här kommandot abonnerar händelse utlösaren på angivna externa tjänst händelser från trigger defintion.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="9a9f2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a9f2-110">EXAMPLES</span></span>

### <span data-ttu-id="9a9f2-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9a9f2-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="9a9f2-112">Det här kommandot abonnerar på BlobEnetTrigger1 för angivna händelser från utlösaren defintion.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="9a9f2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a9f2-113">PARAMETERS</span></span>

### <span data-ttu-id="9a9f2-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9a9f2-114">-DataFactoryName</span></span>
<span data-ttu-id="9a9f2-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-115">The data factory name.</span></span>

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

### <span data-ttu-id="9a9f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a9f2-116">-DefaultProfile</span></span>
<span data-ttu-id="9a9f2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9f2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a9f2-118">-InputObject</span></span>
<span data-ttu-id="9a9f2-119">Utlös ande objekt.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-119">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a9f2-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9a9f2-120">-Name</span></span>
<span data-ttu-id="9a9f2-121">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-121">The trigger name.</span></span>

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

### <span data-ttu-id="9a9f2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a9f2-122">-ResourceGroupName</span></span>
<span data-ttu-id="9a9f2-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-123">The resource group name.</span></span>

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

### <span data-ttu-id="9a9f2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a9f2-124">-ResourceId</span></span>
<span data-ttu-id="9a9f2-125">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9a9f2-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9a9f2-126">-Confirm</span></span>
<span data-ttu-id="9a9f2-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a9f2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a9f2-128">-WhatIf</span></span>
<span data-ttu-id="9a9f2-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a9f2-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a9f2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a9f2-131">CommonParameters</span></span>
<span data-ttu-id="9a9f2-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a9f2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a9f2-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a9f2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a9f2-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a9f2-134">INPUTS</span></span>

### <span data-ttu-id="9a9f2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9a9f2-135">System.String</span></span>
<span data-ttu-id="9a9f2-136">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="9a9f2-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="9a9f2-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a9f2-137">OUTPUTS</span></span>

### <span data-ttu-id="9a9f2-138">Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="9a9f2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="9a9f2-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a9f2-139">NOTES</span></span>

## <span data-ttu-id="9a9f2-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a9f2-140">RELATED LINKS</span></span>

