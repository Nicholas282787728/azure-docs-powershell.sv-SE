---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
ms.openlocfilehash: 5b7cc3d2ea0273d0ff96dfca39d4dcb3e169c6dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916070"
---
# <span data-ttu-id="303f0-101">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="303f0-101">Get-AzLogicAppTrigger</span></span>

## <span data-ttu-id="303f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="303f0-102">SYNOPSIS</span></span>
<span data-ttu-id="303f0-103">Hämtar utlösare för ett logik program.</span><span class="sxs-lookup"><span data-stu-id="303f0-103">Gets the triggers of a logic app.</span></span>

## <span data-ttu-id="303f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="303f0-104">SYNTAX</span></span>

```
Get-AzLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="303f0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="303f0-105">DESCRIPTION</span></span>
<span data-ttu-id="303f0-106">Cmdleten **Get-AzLogicAppTrigger** får utlösare från ett logik program.</span><span class="sxs-lookup"><span data-stu-id="303f0-106">The **Get-AzLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="303f0-107">Denna cmdlet returnerar ett **WorkflowTrigger** -objekt.</span><span class="sxs-lookup"><span data-stu-id="303f0-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="303f0-108">Ange arbets flödet, resurs gruppen och utlösaren.</span><span class="sxs-lookup"><span data-stu-id="303f0-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="303f0-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="303f0-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="303f0-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="303f0-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="303f0-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="303f0-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="303f0-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="303f0-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="303f0-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="303f0-113">EXAMPLES</span></span>

### <span data-ttu-id="303f0-114">Exempel 1: få en utlösare av ett logik program</span><span class="sxs-lookup"><span data-stu-id="303f0-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger01
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp05
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="303f0-115">Det här kommandot får utlösaren med namnet Trigger01 från programmet Logic som heter LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="303f0-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="303f0-116">Exempel 2: Hämta alla utlösare för ett logik program</span><span class="sxs-lookup"><span data-stu-id="303f0-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger02
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp07
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="303f0-117">Det här kommandot får utlösarna till logik programmet som heter LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="303f0-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="303f0-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="303f0-118">PARAMETERS</span></span>

### <span data-ttu-id="303f0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="303f0-119">-DefaultProfile</span></span>
<span data-ttu-id="303f0-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="303f0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="303f0-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="303f0-121">-Name</span></span>
<span data-ttu-id="303f0-122">Anger namnet på den logik app som den här cmdleten får en utlösare från.</span><span class="sxs-lookup"><span data-stu-id="303f0-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="303f0-123">-ResourceGroupName</span></span>
<span data-ttu-id="303f0-124">Anger namnet på en resurs grupp där denna cmdlet ska ha en utlösare.</span><span class="sxs-lookup"><span data-stu-id="303f0-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303f0-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="303f0-125">-TriggerName</span></span>
<span data-ttu-id="303f0-126">Anger namnet på den utlösare som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="303f0-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="303f0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="303f0-127">CommonParameters</span></span>
<span data-ttu-id="303f0-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="303f0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="303f0-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="303f0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="303f0-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="303f0-130">INPUTS</span></span>

### <span data-ttu-id="303f0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="303f0-131">System.String</span></span>

## <span data-ttu-id="303f0-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="303f0-132">OUTPUTS</span></span>

### <span data-ttu-id="303f0-133">Microsoft. Azure. Management. Logic. Models. WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="303f0-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="303f0-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="303f0-134">NOTES</span></span>

## <span data-ttu-id="303f0-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="303f0-135">RELATED LINKS</span></span>

[<span data-ttu-id="303f0-136">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="303f0-136">Get-AzLogicAppTriggerHistory</span></span>](./Get-AzLogicAppTriggerHistory.md)

[<span data-ttu-id="303f0-137">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="303f0-137">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

