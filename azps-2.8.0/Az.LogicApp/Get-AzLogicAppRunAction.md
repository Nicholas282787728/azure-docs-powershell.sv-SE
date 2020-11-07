---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 46f0afa20fbc8e7d8ac659f4fcb13a10591aa79f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743796"
---
# <span data-ttu-id="a40dc-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="a40dc-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="a40dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a40dc-102">SYNOPSIS</span></span>
<span data-ttu-id="a40dc-103">Hämtar en åtgärd från ett logik program som körs.</span><span class="sxs-lookup"><span data-stu-id="a40dc-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="a40dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a40dc-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a40dc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a40dc-105">DESCRIPTION</span></span>
<span data-ttu-id="a40dc-106">Cmdleten **Get-AzLogicAppRunAction** hämtar en åtgärd från ett logik program.</span><span class="sxs-lookup"><span data-stu-id="a40dc-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="a40dc-107">Denna cmdlet returnerar ett **WorkflowRunAction** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a40dc-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="a40dc-108">Ange logik program, resurs grupp och kör.</span><span class="sxs-lookup"><span data-stu-id="a40dc-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="a40dc-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="a40dc-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a40dc-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="a40dc-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a40dc-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="a40dc-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a40dc-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="a40dc-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a40dc-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a40dc-113">EXAMPLES</span></span>

### <span data-ttu-id="a40dc-114">Exempel 1: Hämta en åtgärd från ett logik program</span><span class="sxs-lookup"><span data-stu-id="a40dc-114">Example 1: Get an action from a Logic App run</span></span>
```
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction01
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="a40dc-115">Det här kommandot får en specifik program åtgärd för logik från logik programmet som heter LogicApp05 för kör namnet LogicAppRun56.</span><span class="sxs-lookup"><span data-stu-id="a40dc-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="a40dc-116">Exempel 2: Hämta alla åtgärder från ett logik program</span><span class="sxs-lookup"><span data-stu-id="a40dc-116">Example 2: Get all the actions from a Logic App run</span></span>
```
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction1
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="a40dc-117">Det här kommandot får alla logiska program åtgärder från en kör namngiven LogicAppRun56 av ett logiskt program som heter LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="a40dc-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="a40dc-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a40dc-118">PARAMETERS</span></span>

### <span data-ttu-id="a40dc-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="a40dc-119">-ActionName</span></span>
<span data-ttu-id="a40dc-120">Anger namnet på en åtgärd i ett logik program som körs.</span><span class="sxs-lookup"><span data-stu-id="a40dc-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="a40dc-121">Denna cmdlet hämtar den åtgärd som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a40dc-121">This cmdlet gets the action that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40dc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40dc-122">-DefaultProfile</span></span>
<span data-ttu-id="a40dc-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a40dc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a40dc-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a40dc-124">-Name</span></span>
<span data-ttu-id="a40dc-125">Anger namnet på en logik-app för vilken denna cmdlet får en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="a40dc-125">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="a40dc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a40dc-126">-ResourceGroupName</span></span>
<span data-ttu-id="a40dc-127">Anger namnet på en resurs grupp där cmdleten får en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="a40dc-127">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="a40dc-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="a40dc-128">-RunName</span></span>
<span data-ttu-id="a40dc-129">Anger namnet på en körning av en logik-app.</span><span class="sxs-lookup"><span data-stu-id="a40dc-129">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="a40dc-130">Denna cmdlet hämtar en åtgärd för den körning som parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a40dc-130">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="a40dc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40dc-131">CommonParameters</span></span>
<span data-ttu-id="a40dc-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a40dc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40dc-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40dc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40dc-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a40dc-134">INPUTS</span></span>

### <span data-ttu-id="a40dc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a40dc-135">System.String</span></span>

## <span data-ttu-id="a40dc-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a40dc-136">OUTPUTS</span></span>

### <span data-ttu-id="a40dc-137">Microsoft. Azure. Management. Logic. Models. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="a40dc-137">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="a40dc-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a40dc-138">NOTES</span></span>

## <span data-ttu-id="a40dc-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a40dc-139">RELATED LINKS</span></span>

[<span data-ttu-id="a40dc-140">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="a40dc-140">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="a40dc-141">Stopp-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="a40dc-141">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


