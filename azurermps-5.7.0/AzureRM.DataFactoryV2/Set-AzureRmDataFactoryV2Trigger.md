---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 17953aa02bf0242f358fd07b1173977db6318d05
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93758444"
---
# <span data-ttu-id="2fbae-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2fbae-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="2fbae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2fbae-102">SYNOPSIS</span></span>
<span data-ttu-id="2fbae-103">Skapar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="2fbae-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fbae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2fbae-104">SYNTAX</span></span>

### <span data-ttu-id="2fbae-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="2fbae-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fbae-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2fbae-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fbae-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2fbae-107">DESCRIPTION</span></span>
<span data-ttu-id="2fbae-108">Cmdleten **set-AzureRmDataFactoryV2Trigger** skapar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="2fbae-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="2fbae-109">Om du anger ett namn för en trigger som redan finns uppmanas du att bekräfta i cmdleten innan utlösaren byts ut.</span><span class="sxs-lookup"><span data-stu-id="2fbae-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="2fbae-110">Om du anger parametern _Force_ ersätter cmdlet den befintliga utlösaren utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2fbae-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="2fbae-111">Utlösare skapas i tillståndet "stoppad", vilket innebär att de inte omedelbart påbörjar samtals ledningar som de refererar till.</span><span class="sxs-lookup"><span data-stu-id="2fbae-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="2fbae-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2fbae-112">EXAMPLES</span></span>

### <span data-ttu-id="2fbae-113">Exempel 1: skapa en utlösare</span><span class="sxs-lookup"><span data-stu-id="2fbae-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="2fbae-114">Skapa en ny utlösare som heter "ScheduledTrigger" i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="2fbae-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="2fbae-115">Utlösaren skapas i tillståndet "stoppad", vilket innebär att den inte startas omedelbart.</span><span class="sxs-lookup"><span data-stu-id="2fbae-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="2fbae-116">En utlösare kan börja använda `Start-AzureRmDataFactoryV2Trigger` cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2fbae-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="2fbae-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2fbae-117">PARAMETERS</span></span>

### <span data-ttu-id="2fbae-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2fbae-118">-DataFactoryName</span></span>
<span data-ttu-id="2fbae-119">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="2fbae-119">The data factory name.</span></span>

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

### <span data-ttu-id="2fbae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fbae-120">-DefaultProfile</span></span>
<span data-ttu-id="2fbae-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2fbae-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fbae-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="2fbae-122">-DefinitionFile</span></span>
<span data-ttu-id="2fbae-123">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="2fbae-123">The JSON file path.</span></span>

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

### <span data-ttu-id="2fbae-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2fbae-124">-Force</span></span>
<span data-ttu-id="2fbae-125">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2fbae-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2fbae-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="2fbae-126">-Name</span></span>
<span data-ttu-id="2fbae-127">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="2fbae-127">The trigger name.</span></span>

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

### <span data-ttu-id="2fbae-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fbae-128">-ResourceGroupName</span></span>
<span data-ttu-id="2fbae-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2fbae-129">The resource group name.</span></span>

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

### <span data-ttu-id="2fbae-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fbae-130">-ResourceId</span></span>
<span data-ttu-id="2fbae-131">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="2fbae-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2fbae-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2fbae-132">-Confirm</span></span>
<span data-ttu-id="2fbae-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2fbae-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fbae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fbae-134">-WhatIf</span></span>
<span data-ttu-id="2fbae-135">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2fbae-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2fbae-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fbae-136">CommonParameters</span></span>
<span data-ttu-id="2fbae-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fbae-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fbae-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fbae-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fbae-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2fbae-139">INPUTS</span></span>

### <span data-ttu-id="2fbae-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2fbae-140">System.String</span></span>

## <span data-ttu-id="2fbae-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2fbae-141">OUTPUTS</span></span>

### <span data-ttu-id="2fbae-142">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="2fbae-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="2fbae-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2fbae-143">NOTES</span></span>

## <span data-ttu-id="2fbae-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2fbae-144">RELATED LINKS</span></span>

[<span data-ttu-id="2fbae-145">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2fbae-145">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2fbae-146">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2fbae-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2fbae-147">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2fbae-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2fbae-148">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2fbae-148">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
