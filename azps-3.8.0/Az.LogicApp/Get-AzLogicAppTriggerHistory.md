---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: d20d6ba980b424109e33fd4380eec9be4f7728ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092068"
---
# <span data-ttu-id="1fa2d-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="1fa2d-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="1fa2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1fa2d-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa2d-103">Hämtar historiken för utlösare i en logik app.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="1fa2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1fa2d-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fa2d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1fa2d-105">DESCRIPTION</span></span>
<span data-ttu-id="1fa2d-106">Cmdleten **Get-AzLogicAppTriggerHistory** hämtar historiken för utlösare i en logik app i funktionen logiska appar.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="1fa2d-107">Denna cmdlet returnerar ett **WorkflowTriggerHistory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="1fa2d-108">Ange logik program, resurs grupp och utlösare.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="1fa2d-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1fa2d-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1fa2d-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1fa2d-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1fa2d-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1fa2d-113">EXAMPLES</span></span>

### <span data-ttu-id="1fa2d-114">Exempel 1: få en avtryckare-historik för ett logiskt program</span><span class="sxs-lookup"><span data-stu-id="1fa2d-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A15%3A16Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="1fa2d-115">Det här kommandot får en specifik logik program utlösare för en utlösare i logik programmet som heter LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="1fa2d-116">Exempel 2: få Utlös ande historik för ett logiskt program</span><span class="sxs-lookup"><span data-stu-id="1fa2d-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
Code        : BadRequest
EndTime     : 1/13/2016 2:43:33 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/CAB46_60e2ad0f0e1947e8b5798716914c5d
              b6_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489106716457817
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:43:33 PM
Status      : Failed
TrackingId  : c91a63f1-48b4-4eae-91eb-8f6dbfa9fe06
Type        : Microsoft.Logic/workflows/triggers/histories

Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="1fa2d-117">Det här kommandot får arbets flödets utlösare historik för en utlösare i logik programmet som heter LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="1fa2d-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1fa2d-118">PARAMETERS</span></span>

### <span data-ttu-id="1fa2d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fa2d-119">-DefaultProfile</span></span>
<span data-ttu-id="1fa2d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1fa2d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fa2d-121">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="1fa2d-121">-HistoryName</span></span>
<span data-ttu-id="1fa2d-122">Anger namnet på den historik som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-122">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1fa2d-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="1fa2d-123">-Name</span></span>
<span data-ttu-id="1fa2d-124">Anger namnet på den logikfel som denna cmdlet ska utlösa historik för.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="1fa2d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fa2d-125">-ResourceGroupName</span></span>
<span data-ttu-id="1fa2d-126">Anger namnet på den resurs grupp där denna cmdlet ska historik.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="1fa2d-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="1fa2d-127">-TriggerName</span></span>
<span data-ttu-id="1fa2d-128">Anger namnet på den trigger som denna cmdlet ska ha historik för.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="1fa2d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa2d-129">CommonParameters</span></span>
<span data-ttu-id="1fa2d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fa2d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa2d-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fa2d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa2d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1fa2d-132">INPUTS</span></span>

### <span data-ttu-id="1fa2d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1fa2d-133">System.String</span></span>

## <span data-ttu-id="1fa2d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1fa2d-134">OUTPUTS</span></span>

### <span data-ttu-id="1fa2d-135">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="1fa2d-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="1fa2d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1fa2d-136">NOTES</span></span>

## <span data-ttu-id="1fa2d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1fa2d-137">RELATED LINKS</span></span>

[<span data-ttu-id="1fa2d-138">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="1fa2d-138">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="1fa2d-139">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="1fa2d-139">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="1fa2d-140">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1fa2d-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


