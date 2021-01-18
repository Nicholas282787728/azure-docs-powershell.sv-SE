---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 6e60f4ed93dd3963fa748db250cacfcf0aeecce3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525599"
---
# <span data-ttu-id="67d34-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="67d34-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="67d34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67d34-102">SYNOPSIS</span></span>
<span data-ttu-id="67d34-103">Få ett automatiskt svar (varnings regel åtgärd).</span><span class="sxs-lookup"><span data-stu-id="67d34-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="67d34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67d34-104">SYNTAX</span></span>

### <span data-ttu-id="67d34-105">AlertRuleId (standard)</span><span class="sxs-lookup"><span data-stu-id="67d34-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67d34-106">ActionId</span><span class="sxs-lookup"><span data-stu-id="67d34-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67d34-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67d34-107">DESCRIPTION</span></span>
<span data-ttu-id="67d34-108">Cmdleten **Get-AzSentinelAlertRuleAction** får ett automatiskt svar (varnings regel åtgärd) från den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="67d34-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="67d34-109">Om du anger parametrarna *ActionId* och *AlertRuleId* returneras ett enskilt **AlertRuleAction** -objekt.</span><span class="sxs-lookup"><span data-stu-id="67d34-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="67d34-110">Om du inte anger parametern *ActionId* returneras en matris som innehåller alla åtgärder för den specifika varnings regeln på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="67d34-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="67d34-111">Du kan **använda händelseobjektet för att uppdatera åtgärden,** till exempel om du vill ändra **åtgärden** för en notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="67d34-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="67d34-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67d34-112">EXAMPLES</span></span>

### <span data-ttu-id="67d34-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="67d34-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="67d34-114">Det här exemplet får alla **åtgärder** för den angivna notifieringsregeln på den angivna arbets ytan och lagrar den sedan i $AlertRuleActions variabel.</span><span class="sxs-lookup"><span data-stu-id="67d34-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="67d34-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="67d34-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="67d34-116">Det här exemplet får en **AlertRuleAction** för den angivna notifieringsregeln på den angivna arbets ytan och lagrar den sedan i $AlertRuleAction variabel.</span><span class="sxs-lookup"><span data-stu-id="67d34-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="67d34-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67d34-117">PARAMETERS</span></span>

### <span data-ttu-id="67d34-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="67d34-118">-ActionId</span></span>
<span data-ttu-id="67d34-119">Åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="67d34-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d34-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="67d34-120">-AlertRuleId</span></span>
<span data-ttu-id="67d34-121">ID för notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="67d34-121">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d34-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d34-122">-DefaultProfile</span></span>
<span data-ttu-id="67d34-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67d34-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67d34-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d34-124">-ResourceGroupName</span></span>
<span data-ttu-id="67d34-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="67d34-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d34-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="67d34-126">-WorkspaceName</span></span>
<span data-ttu-id="67d34-127">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="67d34-127">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d34-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d34-128">CommonParameters</span></span>
<span data-ttu-id="67d34-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d34-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d34-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67d34-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d34-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67d34-131">INPUTS</span></span>

### <span data-ttu-id="67d34-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="67d34-132">None</span></span>
## <span data-ttu-id="67d34-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67d34-133">OUTPUTS</span></span>

### <span data-ttu-id="67d34-134">Microsoft. Azure. commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="67d34-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="67d34-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67d34-135">NOTES</span></span>

## <span data-ttu-id="67d34-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67d34-136">RELATED LINKS</span></span>
