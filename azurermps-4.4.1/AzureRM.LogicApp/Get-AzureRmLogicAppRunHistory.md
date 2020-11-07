---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
ms.openlocfilehash: 05ccc9dc237e0058665607488a5083a5295eb2f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757283"
---
# <span data-ttu-id="e7922-101">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="e7922-101">Get-AzureRmLogicAppRunHistory</span></span>

## <span data-ttu-id="e7922-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7922-102">SYNOPSIS</span></span>
<span data-ttu-id="e7922-103">Hämtar programmet kör historik för en logik.</span><span class="sxs-lookup"><span data-stu-id="e7922-103">Gets the run history of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7922-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7922-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7922-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7922-105">DESCRIPTION</span></span>
<span data-ttu-id="e7922-106">Cmdleten **Get-AzureRmLogicAppRunHistory** hämtar en program historik för logik.</span><span class="sxs-lookup"><span data-stu-id="e7922-106">The **Get-AzureRmLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="e7922-107">Denna cmdlet returnerar en mängd med **WorkflowRun** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e7922-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="e7922-108">Ange logik programmet och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e7922-108">Specify the logic app and resource group.</span></span>

<span data-ttu-id="e7922-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="e7922-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e7922-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="e7922-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e7922-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="e7922-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e7922-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="e7922-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e7922-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7922-113">EXAMPLES</span></span>

### <span data-ttu-id="e7922-114">Exempel 1: Hämta programmet kör historik för en logik</span><span class="sxs-lookup"><span data-stu-id="e7922-114">Example 1: Get the run history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="e7922-115">Det här kommandot tar emot kör-historiken för ett logiskt program som heter LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="e7922-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="e7922-116">Exempel 2: få ett logik program att köra</span><span class="sxs-lookup"><span data-stu-id="e7922-116">Example 2: Get a logic app run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="e7922-117">Det här kommandot får ett specifikt logiskt program för logik programmet som heter LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="e7922-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

## <span data-ttu-id="e7922-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7922-118">PARAMETERS</span></span>

### <span data-ttu-id="e7922-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e7922-119">-Name</span></span>
<span data-ttu-id="e7922-120">Anger namnet på den logikfel som denna cmdlet ska köra historik för.</span><span class="sxs-lookup"><span data-stu-id="e7922-120">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7922-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7922-121">-ResourceGroupName</span></span>
<span data-ttu-id="e7922-122">Anger namnet på en resurs grupp som innehåller programmet logik.</span><span class="sxs-lookup"><span data-stu-id="e7922-122">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="e7922-123">-RunName</span><span class="sxs-lookup"><span data-stu-id="e7922-123">-RunName</span></span>
<span data-ttu-id="e7922-124">Anger körnings namnet för en logik-app.</span><span class="sxs-lookup"><span data-stu-id="e7922-124">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="e7922-125">Denna cmdlet hämtar arbets flödes körningen som denna cmdlet anger.</span><span class="sxs-lookup"><span data-stu-id="e7922-125">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="e7922-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7922-126">-DefaultProfile</span></span>
<span data-ttu-id="e7922-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e7922-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7922-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7922-128">CommonParameters</span></span>
<span data-ttu-id="e7922-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7922-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7922-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7922-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7922-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7922-131">INPUTS</span></span>

## <span data-ttu-id="e7922-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7922-132">OUTPUTS</span></span>

### <span data-ttu-id="e7922-133">Microsoft. Azure. Management. Logic. Models. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="e7922-133">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="e7922-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7922-134">NOTES</span></span>

## <span data-ttu-id="e7922-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7922-135">RELATED LINKS</span></span>

[<span data-ttu-id="e7922-136">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="e7922-136">Get-AzureRmLogicAppRunAction</span></span>](./Get-AzureRmLogicAppRunAction.md)

[<span data-ttu-id="e7922-137">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e7922-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

[<span data-ttu-id="e7922-138">Stopp-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="e7922-138">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


