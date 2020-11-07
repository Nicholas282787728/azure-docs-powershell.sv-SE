---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c1e7fab8eb4e8afe22bdebc5930c8599c2dadceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744711"
---
# <span data-ttu-id="b7c94-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="b7c94-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="b7c94-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7c94-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c94-103">Avabonnera händelse utlösaren för externa tjänst händelser.</span><span class="sxs-lookup"><span data-stu-id="b7c94-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="b7c94-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7c94-104">SYNTAX</span></span>

### <span data-ttu-id="b7c94-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="b7c94-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7c94-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b7c94-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7c94-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7c94-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7c94-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7c94-108">DESCRIPTION</span></span>
<span data-ttu-id="b7c94-109">Det här kommandot avabonnerar händelse utlösaren för angivna externa tjänst händelser från trigger defintion.</span><span class="sxs-lookup"><span data-stu-id="b7c94-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="b7c94-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7c94-110">EXAMPLES</span></span>

### <span data-ttu-id="b7c94-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b7c94-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="b7c94-112">Det här kommandot avbryter prenumerationen på BlobEnetTrigger1 för angivna händelser från utlösaren defintion.</span><span class="sxs-lookup"><span data-stu-id="b7c94-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="b7c94-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7c94-113">PARAMETERS</span></span>

### <span data-ttu-id="b7c94-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b7c94-114">-DataFactoryName</span></span>
<span data-ttu-id="b7c94-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="b7c94-115">The data factory name.</span></span>

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

### <span data-ttu-id="b7c94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c94-116">-DefaultProfile</span></span>
<span data-ttu-id="b7c94-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c94-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7c94-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b7c94-118">-Force</span></span>
<span data-ttu-id="b7c94-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b7c94-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b7c94-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7c94-120">-InputObject</span></span>
<span data-ttu-id="b7c94-121">Utlös ande objekt.</span><span class="sxs-lookup"><span data-stu-id="b7c94-121">The trigger object.</span></span>

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

### <span data-ttu-id="b7c94-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7c94-122">-Name</span></span>
<span data-ttu-id="b7c94-123">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="b7c94-123">The trigger name.</span></span>

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

### <span data-ttu-id="b7c94-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7c94-124">-PassThru</span></span>
<span data-ttu-id="b7c94-125">Om det här värdet anges returnerar cmdlet return true vid lyckad borttagning.</span><span class="sxs-lookup"><span data-stu-id="b7c94-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="b7c94-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c94-126">-ResourceGroupName</span></span>
<span data-ttu-id="b7c94-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b7c94-127">The resource group name.</span></span>

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

### <span data-ttu-id="b7c94-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7c94-128">-ResourceId</span></span>
<span data-ttu-id="b7c94-129">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="b7c94-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b7c94-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7c94-130">-Confirm</span></span>
<span data-ttu-id="b7c94-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7c94-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7c94-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7c94-132">-WhatIf</span></span>
<span data-ttu-id="b7c94-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7c94-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7c94-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7c94-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7c94-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c94-135">CommonParameters</span></span>
<span data-ttu-id="b7c94-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c94-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c94-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c94-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c94-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7c94-138">INPUTS</span></span>

### <span data-ttu-id="b7c94-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c94-139">System.String</span></span>
<span data-ttu-id="b7c94-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="b7c94-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="b7c94-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7c94-141">OUTPUTS</span></span>

### <span data-ttu-id="b7c94-142">Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b7c94-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="b7c94-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7c94-143">NOTES</span></span>

## <span data-ttu-id="b7c94-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7c94-144">RELATED LINKS</span></span>
