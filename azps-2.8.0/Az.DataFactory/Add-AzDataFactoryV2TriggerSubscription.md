---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c99626e1323f10e98dcef1efc7ae622aab5f6b5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744818"
---
# <span data-ttu-id="d762a-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="d762a-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="d762a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d762a-102">SYNOPSIS</span></span>
<span data-ttu-id="d762a-103">Abonnera på händelse utlösare för externa tjänst händelser.</span><span class="sxs-lookup"><span data-stu-id="d762a-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="d762a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d762a-104">SYNTAX</span></span>

### <span data-ttu-id="d762a-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="d762a-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d762a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d762a-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d762a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d762a-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d762a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d762a-108">DESCRIPTION</span></span>
<span data-ttu-id="d762a-109">Det här kommandot abonnerar händelse utlösaren på angivna externa tjänst händelser från trigger defintion.</span><span class="sxs-lookup"><span data-stu-id="d762a-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="d762a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d762a-110">EXAMPLES</span></span>

### <span data-ttu-id="d762a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d762a-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="d762a-112">Det här kommandot abonnerar på BlobEnetTrigger1 för angivna händelser från utlösaren defintion.</span><span class="sxs-lookup"><span data-stu-id="d762a-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="d762a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d762a-113">PARAMETERS</span></span>

### <span data-ttu-id="d762a-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d762a-114">-DataFactoryName</span></span>
<span data-ttu-id="d762a-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="d762a-115">The data factory name.</span></span>

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

### <span data-ttu-id="d762a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d762a-116">-DefaultProfile</span></span>
<span data-ttu-id="d762a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d762a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d762a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d762a-118">-InputObject</span></span>
<span data-ttu-id="d762a-119">Utlös ande objekt.</span><span class="sxs-lookup"><span data-stu-id="d762a-119">The trigger object.</span></span>

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

### <span data-ttu-id="d762a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d762a-120">-Name</span></span>
<span data-ttu-id="d762a-121">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="d762a-121">The trigger name.</span></span>

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

### <span data-ttu-id="d762a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d762a-122">-ResourceGroupName</span></span>
<span data-ttu-id="d762a-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d762a-123">The resource group name.</span></span>

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

### <span data-ttu-id="d762a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d762a-124">-ResourceId</span></span>
<span data-ttu-id="d762a-125">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="d762a-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d762a-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d762a-126">-Confirm</span></span>
<span data-ttu-id="d762a-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d762a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d762a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d762a-128">-WhatIf</span></span>
<span data-ttu-id="d762a-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d762a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d762a-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d762a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d762a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d762a-131">CommonParameters</span></span>
<span data-ttu-id="d762a-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d762a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d762a-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d762a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d762a-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d762a-134">INPUTS</span></span>

### <span data-ttu-id="d762a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d762a-135">System.String</span></span>
<span data-ttu-id="d762a-136">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="d762a-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="d762a-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d762a-137">OUTPUTS</span></span>

### <span data-ttu-id="d762a-138">Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="d762a-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="d762a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d762a-139">NOTES</span></span>

## <span data-ttu-id="d762a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d762a-140">RELATED LINKS</span></span>

