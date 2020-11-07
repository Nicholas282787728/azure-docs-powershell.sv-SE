---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 490965bf1edf39942272b9ef6caeb598b4e2d296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758103"
---
# <span data-ttu-id="be68d-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="be68d-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="be68d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="be68d-102">SYNOPSIS</span></span>
<span data-ttu-id="be68d-103">Skapar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="be68d-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be68d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="be68d-104">SYNTAX</span></span>

### <span data-ttu-id="be68d-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="be68d-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be68d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="be68d-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be68d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="be68d-107">DESCRIPTION</span></span>
<span data-ttu-id="be68d-108">Cmdleten **set-AzureRmDataFactoryV2Trigger** skapar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="be68d-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="be68d-109">Om du anger ett namn för en trigger som redan finns uppmanas du att bekräfta i cmdleten innan utlösaren byts ut.</span><span class="sxs-lookup"><span data-stu-id="be68d-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="be68d-110">Om du anger parametern _Force_ ersätter cmdlet den befintliga utlösaren utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="be68d-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="be68d-111">Utlösare skapas i tillståndet "stoppad", vilket innebär att de inte omedelbart påbörjar samtals ledningar som de refererar till.</span><span class="sxs-lookup"><span data-stu-id="be68d-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="be68d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="be68d-112">EXAMPLES</span></span>

### <span data-ttu-id="be68d-113">Exempel 1: skapa en utlösare</span><span class="sxs-lookup"><span data-stu-id="be68d-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="be68d-114">Skapa en ny utlösare som heter "ScheduledTrigger" i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="be68d-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="be68d-115">Utlösaren skapas i tillståndet "stoppad", vilket innebär att den inte startas omedelbart.</span><span class="sxs-lookup"><span data-stu-id="be68d-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="be68d-116">En utlösare kan börja använda `Start-AzureRmDataFactoryV2Trigger` cmdleten.</span><span class="sxs-lookup"><span data-stu-id="be68d-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="be68d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="be68d-117">PARAMETERS</span></span>

### <span data-ttu-id="be68d-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="be68d-118">-Confirm</span></span>
<span data-ttu-id="be68d-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="be68d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be68d-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="be68d-120">-DataFactoryName</span></span>
<span data-ttu-id="be68d-121">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="be68d-121">The data factory name.</span></span>

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

### <span data-ttu-id="be68d-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="be68d-122">-DefinitionFile</span></span>
<span data-ttu-id="be68d-123">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="be68d-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be68d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="be68d-124">-Force</span></span>
<span data-ttu-id="be68d-125">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="be68d-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="be68d-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="be68d-126">-Name</span></span>
<span data-ttu-id="be68d-127">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="be68d-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be68d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be68d-128">-ResourceGroupName</span></span>
<span data-ttu-id="be68d-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="be68d-129">The resource group name.</span></span>

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

### <span data-ttu-id="be68d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be68d-130">-ResourceId</span></span>
<span data-ttu-id="be68d-131">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="be68d-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="be68d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be68d-132">-WhatIf</span></span>
<span data-ttu-id="be68d-133">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="be68d-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="be68d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be68d-134">-DefaultProfile</span></span>
<span data-ttu-id="be68d-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="be68d-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be68d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be68d-136">CommonParameters</span></span>
<span data-ttu-id="be68d-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be68d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be68d-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be68d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be68d-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="be68d-139">INPUTS</span></span>

### <span data-ttu-id="be68d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="be68d-140">System.String</span></span>

## <span data-ttu-id="be68d-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="be68d-141">OUTPUTS</span></span>

### <span data-ttu-id="be68d-142">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="be68d-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="be68d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="be68d-143">NOTES</span></span>

## <span data-ttu-id="be68d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="be68d-144">RELATED LINKS</span></span>

[<span data-ttu-id="be68d-145">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="be68d-145">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="be68d-146">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="be68d-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="be68d-147">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="be68d-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="be68d-148">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="be68d-148">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
