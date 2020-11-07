---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 96bcf29f2f2f3125f74657cc64cbcf66370760dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744689"
---
# <span data-ttu-id="3d044-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3d044-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="3d044-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d044-102">SYNOPSIS</span></span>
<span data-ttu-id="3d044-103">Skapar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="3d044-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="3d044-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d044-104">SYNTAX</span></span>

### <span data-ttu-id="3d044-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="3d044-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d044-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3d044-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d044-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d044-107">DESCRIPTION</span></span>
<span data-ttu-id="3d044-108">Cmdleten **set-AzDataFactoryV2Trigger** skapar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="3d044-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="3d044-109">Om du anger ett namn för en trigger som redan finns uppmanas du att bekräfta i cmdleten innan utlösaren byts ut.</span><span class="sxs-lookup"><span data-stu-id="3d044-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="3d044-110">Om du anger parametern _Force_ ersätter cmdlet den befintliga utlösaren utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="3d044-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="3d044-111">Utlösare skapas i tillståndet "stoppad", vilket innebär att de inte omedelbart påbörjar samtals ledningar som de refererar till.</span><span class="sxs-lookup"><span data-stu-id="3d044-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="3d044-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d044-112">EXAMPLES</span></span>

### <span data-ttu-id="3d044-113">Exempel 1: skapa en utlösare</span><span class="sxs-lookup"><span data-stu-id="3d044-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="3d044-114">Skapa en ny utlösare som heter "ScheduledTrigger" i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="3d044-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="3d044-115">Utlösaren skapas i tillståndet "stoppad", vilket innebär att den inte startas omedelbart.</span><span class="sxs-lookup"><span data-stu-id="3d044-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="3d044-116">En utlösare kan börja använda `Start-AzDataFactoryV2Trigger` cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d044-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="3d044-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d044-117">PARAMETERS</span></span>

### <span data-ttu-id="3d044-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3d044-118">-DataFactoryName</span></span>
<span data-ttu-id="3d044-119">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="3d044-119">The data factory name.</span></span>

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

### <span data-ttu-id="3d044-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d044-120">-DefaultProfile</span></span>
<span data-ttu-id="3d044-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d044-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d044-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="3d044-122">-DefinitionFile</span></span>
<span data-ttu-id="3d044-123">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="3d044-123">The JSON file path.</span></span>

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

### <span data-ttu-id="3d044-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3d044-124">-Force</span></span>
<span data-ttu-id="3d044-125">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="3d044-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3d044-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d044-126">-Name</span></span>
<span data-ttu-id="3d044-127">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="3d044-127">The trigger name.</span></span>

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

### <span data-ttu-id="3d044-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d044-128">-ResourceGroupName</span></span>
<span data-ttu-id="3d044-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3d044-129">The resource group name.</span></span>

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

### <span data-ttu-id="3d044-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d044-130">-ResourceId</span></span>
<span data-ttu-id="3d044-131">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="3d044-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3d044-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d044-132">-Confirm</span></span>
<span data-ttu-id="3d044-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d044-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d044-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d044-134">-WhatIf</span></span>
<span data-ttu-id="3d044-135">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d044-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3d044-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d044-136">CommonParameters</span></span>
<span data-ttu-id="3d044-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d044-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d044-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d044-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d044-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d044-139">INPUTS</span></span>

### <span data-ttu-id="3d044-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3d044-140">System.String</span></span>

## <span data-ttu-id="3d044-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d044-141">OUTPUTS</span></span>

### <span data-ttu-id="3d044-142">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="3d044-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="3d044-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d044-143">NOTES</span></span>

## <span data-ttu-id="3d044-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d044-144">RELATED LINKS</span></span>

[<span data-ttu-id="3d044-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3d044-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3d044-146">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3d044-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3d044-147">Stopp-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3d044-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3d044-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3d044-148">Remove-AzDataFactoryV2Trigger</span></span>]()