---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
ms.openlocfilehash: 9c27fd1e46d17722f843a09babab31338e88e2ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757600"
---
# <span data-ttu-id="a7e30-101">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="a7e30-101">Get-AzureRmLogicAppTriggerHistory</span></span>

## <span data-ttu-id="a7e30-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7e30-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e30-103">Hämtar historiken för utlösare i en logik app.</span><span class="sxs-lookup"><span data-stu-id="a7e30-103">Gets the history of triggers in a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7e30-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7e30-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7e30-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7e30-105">DESCRIPTION</span></span>
<span data-ttu-id="a7e30-106">Cmdleten **Get-AzureRmLogicAppTriggerHistory** hämtar historiken för utlösare i en logik app i funktionen logiska appar.</span><span class="sxs-lookup"><span data-stu-id="a7e30-106">The **Get-AzureRmLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="a7e30-107">Denna cmdlet returnerar ett **WorkflowTriggerHistory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a7e30-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="a7e30-108">Ange logik program, resurs grupp och utlösare.</span><span class="sxs-lookup"><span data-stu-id="a7e30-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="a7e30-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="a7e30-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a7e30-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="a7e30-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a7e30-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="a7e30-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a7e30-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="a7e30-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a7e30-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7e30-113">EXAMPLES</span></span>

### <span data-ttu-id="a7e30-114">Exempel 1: få en avtryckare-historik för ett logiskt program</span><span class="sxs-lookup"><span data-stu-id="a7e30-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
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

<span data-ttu-id="a7e30-115">Det här kommandot får en specifik logik program utlösare för en utlösare i logik programmet som heter LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="a7e30-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="a7e30-116">Exempel 2: få Utlös ande historik för ett logiskt program</span><span class="sxs-lookup"><span data-stu-id="a7e30-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
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

<span data-ttu-id="a7e30-117">Det här kommandot får arbets flödets utlösare historik för en utlösare i logik programmet som heter LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="a7e30-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="a7e30-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7e30-118">PARAMETERS</span></span>

### <span data-ttu-id="a7e30-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e30-119">-DefaultProfile</span></span>
<span data-ttu-id="a7e30-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a7e30-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7e30-121">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="a7e30-121">-HistoryName</span></span>
<span data-ttu-id="a7e30-122">Anger namnet på den historik som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="a7e30-122">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a7e30-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="a7e30-123">-Name</span></span>
<span data-ttu-id="a7e30-124">Anger namnet på den logikfel som denna cmdlet ska utlösa historik för.</span><span class="sxs-lookup"><span data-stu-id="a7e30-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="a7e30-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7e30-125">-ResourceGroupName</span></span>
<span data-ttu-id="a7e30-126">Anger namnet på den resurs grupp där denna cmdlet ska historik.</span><span class="sxs-lookup"><span data-stu-id="a7e30-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="a7e30-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="a7e30-127">-TriggerName</span></span>
<span data-ttu-id="a7e30-128">Anger namnet på den trigger som denna cmdlet ska ha historik för.</span><span class="sxs-lookup"><span data-stu-id="a7e30-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="a7e30-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e30-129">CommonParameters</span></span>
<span data-ttu-id="a7e30-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7e30-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e30-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7e30-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e30-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7e30-132">INPUTS</span></span>

### <span data-ttu-id="a7e30-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a7e30-133">System.String</span></span>

## <span data-ttu-id="a7e30-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7e30-134">OUTPUTS</span></span>

### <span data-ttu-id="a7e30-135">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="a7e30-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="a7e30-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7e30-136">NOTES</span></span>

## <span data-ttu-id="a7e30-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7e30-137">RELATED LINKS</span></span>

[<span data-ttu-id="a7e30-138">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="a7e30-138">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="a7e30-139">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="a7e30-139">Get-AzureRmLogicAppTrigger</span></span>](./Get-AzureRmLogicAppTrigger.md)

[<span data-ttu-id="a7e30-140">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a7e30-140">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


