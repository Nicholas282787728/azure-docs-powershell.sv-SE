---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
ms.openlocfilehash: 49968330f56fe0891adb9c5a62a1264700f53224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583275"
---
# <span data-ttu-id="4d1da-101">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="4d1da-101">Get-AzureRmLogicAppRunAction</span></span>

## <span data-ttu-id="4d1da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d1da-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1da-103">Hämtar en åtgärd från ett logik program som körs.</span><span class="sxs-lookup"><span data-stu-id="4d1da-103">Gets an action from a logic app run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d1da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d1da-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String>
 [-ActionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d1da-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d1da-105">DESCRIPTION</span></span>
<span data-ttu-id="4d1da-106">Cmdleten **Get-AzureRmLogicAppRunAction** hämtar en åtgärd från ett logik program.</span><span class="sxs-lookup"><span data-stu-id="4d1da-106">The **Get-AzureRmLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="4d1da-107">Denna cmdlet returnerar ett **WorkflowRunAction** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4d1da-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="4d1da-108">Ange logik program, resurs grupp och kör.</span><span class="sxs-lookup"><span data-stu-id="4d1da-108">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="4d1da-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="4d1da-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4d1da-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="4d1da-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4d1da-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="4d1da-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4d1da-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="4d1da-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4d1da-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d1da-113">EXAMPLES</span></span>

### <span data-ttu-id="4d1da-114">Exempel 1: Hämta en åtgärd från ett logik program</span><span class="sxs-lookup"><span data-stu-id="4d1da-114">Example 1: Get an action from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
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

<span data-ttu-id="4d1da-115">Det här kommandot får en specifik program åtgärd för logik från logik programmet som heter LogicApp05 för kör namnet LogicAppRun56.</span><span class="sxs-lookup"><span data-stu-id="4d1da-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="4d1da-116">Exempel 2: Hämta alla åtgärder från ett logik program</span><span class="sxs-lookup"><span data-stu-id="4d1da-116">Example 2: Get all the actions from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
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

<span data-ttu-id="4d1da-117">Det här kommandot får alla logiska program åtgärder från en kör namngiven LogicAppRun56 av ett logiskt program som heter LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="4d1da-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="4d1da-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d1da-118">PARAMETERS</span></span>

### <span data-ttu-id="4d1da-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="4d1da-119">-ActionName</span></span>
<span data-ttu-id="4d1da-120">Anger namnet på en åtgärd i ett logik program som körs.</span><span class="sxs-lookup"><span data-stu-id="4d1da-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="4d1da-121">Denna cmdlet hämtar den åtgärd som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="4d1da-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="4d1da-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d1da-122">-Name</span></span>
<span data-ttu-id="4d1da-123">Anger namnet på en logik-app för vilken denna cmdlet får en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="4d1da-123">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="4d1da-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d1da-124">-ResourceGroupName</span></span>
<span data-ttu-id="4d1da-125">Anger namnet på en resurs grupp där cmdleten får en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="4d1da-125">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="4d1da-126">-RunName</span><span class="sxs-lookup"><span data-stu-id="4d1da-126">-RunName</span></span>
<span data-ttu-id="4d1da-127">Anger namnet på en körning av en logik-app.</span><span class="sxs-lookup"><span data-stu-id="4d1da-127">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="4d1da-128">Denna cmdlet hämtar en åtgärd för den körning som parametern anger.</span><span class="sxs-lookup"><span data-stu-id="4d1da-128">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="4d1da-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1da-129">-DefaultProfile</span></span>
<span data-ttu-id="4d1da-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d1da-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d1da-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1da-131">CommonParameters</span></span>
<span data-ttu-id="4d1da-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d1da-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1da-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d1da-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1da-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d1da-134">INPUTS</span></span>

## <span data-ttu-id="4d1da-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d1da-135">OUTPUTS</span></span>

### <span data-ttu-id="4d1da-136">Microsoft. Azure. Management. Logic. Models. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="4d1da-136">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="4d1da-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d1da-137">NOTES</span></span>

## <span data-ttu-id="4d1da-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d1da-138">RELATED LINKS</span></span>

[<span data-ttu-id="4d1da-139">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="4d1da-139">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="4d1da-140">Stopp-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="4d1da-140">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


