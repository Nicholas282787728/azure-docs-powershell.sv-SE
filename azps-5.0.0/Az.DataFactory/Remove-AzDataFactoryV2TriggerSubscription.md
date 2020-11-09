---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320868"
---
# <span data-ttu-id="3711e-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="3711e-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="3711e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3711e-102">SYNOPSIS</span></span>
<span data-ttu-id="3711e-103">Avabonnera händelse utlösaren för externa tjänst händelser.</span><span class="sxs-lookup"><span data-stu-id="3711e-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="3711e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3711e-104">SYNTAX</span></span>

### <span data-ttu-id="3711e-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="3711e-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3711e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3711e-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3711e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3711e-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3711e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3711e-108">DESCRIPTION</span></span>
<span data-ttu-id="3711e-109">Det här kommandot avabonnerar händelse utlösaren för angivna externa tjänst händelser från trigger defintion.</span><span class="sxs-lookup"><span data-stu-id="3711e-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="3711e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3711e-110">EXAMPLES</span></span>

### <span data-ttu-id="3711e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3711e-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="3711e-112">Det här kommandot avbryter prenumerationen på BlobEnetTrigger1 för angivna händelser från utlösaren defintion.</span><span class="sxs-lookup"><span data-stu-id="3711e-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="3711e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3711e-113">PARAMETERS</span></span>

### <span data-ttu-id="3711e-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3711e-114">-DataFactoryName</span></span>
<span data-ttu-id="3711e-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="3711e-115">The data factory name.</span></span>

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

### <span data-ttu-id="3711e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3711e-116">-DefaultProfile</span></span>
<span data-ttu-id="3711e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3711e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3711e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3711e-118">-Force</span></span>
<span data-ttu-id="3711e-119">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3711e-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3711e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3711e-120">-InputObject</span></span>
<span data-ttu-id="3711e-121">Utlös ande objekt.</span><span class="sxs-lookup"><span data-stu-id="3711e-121">The trigger object.</span></span>

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

### <span data-ttu-id="3711e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="3711e-122">-Name</span></span>
<span data-ttu-id="3711e-123">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="3711e-123">The trigger name.</span></span>

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

### <span data-ttu-id="3711e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3711e-124">-PassThru</span></span>
<span data-ttu-id="3711e-125">Om det här värdet anges returnerar cmdlet return true vid lyckad borttagning.</span><span class="sxs-lookup"><span data-stu-id="3711e-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="3711e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3711e-126">-ResourceGroupName</span></span>
<span data-ttu-id="3711e-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3711e-127">The resource group name.</span></span>

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

### <span data-ttu-id="3711e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3711e-128">-ResourceId</span></span>
<span data-ttu-id="3711e-129">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="3711e-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3711e-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3711e-130">-Confirm</span></span>
<span data-ttu-id="3711e-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3711e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3711e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3711e-132">-WhatIf</span></span>
<span data-ttu-id="3711e-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3711e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3711e-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3711e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3711e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3711e-135">CommonParameters</span></span>
<span data-ttu-id="3711e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3711e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3711e-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3711e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3711e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3711e-138">INPUTS</span></span>

### <span data-ttu-id="3711e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3711e-139">System.String</span></span>
<span data-ttu-id="3711e-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="3711e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="3711e-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3711e-141">OUTPUTS</span></span>

### <span data-ttu-id="3711e-142">Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="3711e-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="3711e-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3711e-143">NOTES</span></span>

## <span data-ttu-id="3711e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3711e-144">RELATED LINKS</span></span>

