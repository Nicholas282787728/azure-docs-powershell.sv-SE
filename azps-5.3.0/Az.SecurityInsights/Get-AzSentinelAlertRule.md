---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 02dc3b58d9cd4b4be58b83f36cc6e42e11008812
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525602"
---
# <span data-ttu-id="fa29d-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="fa29d-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="fa29d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa29d-102">SYNOPSIS</span></span>
<span data-ttu-id="fa29d-103">Hämtar en analys (varnings regel).</span><span class="sxs-lookup"><span data-stu-id="fa29d-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="fa29d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa29d-104">SYNTAX</span></span>

### <span data-ttu-id="fa29d-105">WorkspaceScope (standard)</span><span class="sxs-lookup"><span data-stu-id="fa29d-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa29d-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="fa29d-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa29d-107">ID</span><span class="sxs-lookup"><span data-stu-id="fa29d-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa29d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa29d-108">DESCRIPTION</span></span>
<span data-ttu-id="fa29d-109">Cmdleten **Get-AzSentinelAlertRule** får en analys (notifieringsregel) från den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="fa29d-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="fa29d-110">Om du anger parametern *AlertRuleId* returneras ett enskilt **AlertRule** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fa29d-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="fa29d-111">Om du inte anger parametern *AlertRuleId* returneras en matris med alla varnings regler på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="fa29d-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="fa29d-112">Du kan använda **AlertRule** -objektet för att uppdatera AlertRule, till exempel om du vill inaktivera **AlertRule**.</span><span class="sxs-lookup"><span data-stu-id="fa29d-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="fa29d-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa29d-113">EXAMPLES</span></span>

### <span data-ttu-id="fa29d-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fa29d-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="fa29d-115">Det här exemplet får alla **AlertRules** på den angivna arbets ytan och lagrar dem sedan i $AlertRules variabel.</span><span class="sxs-lookup"><span data-stu-id="fa29d-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="fa29d-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fa29d-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="fa29d-117">Det här exemplet får en **AlertRule** på den angivna arbets ytan och lagrar den sedan i $AlertRule variabel.</span><span class="sxs-lookup"><span data-stu-id="fa29d-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="fa29d-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa29d-118">PARAMETERS</span></span>

### <span data-ttu-id="fa29d-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="fa29d-119">-AlertRuleId</span></span>
<span data-ttu-id="fa29d-120">ID för notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="fa29d-120">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa29d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa29d-121">-DefaultProfile</span></span>
<span data-ttu-id="fa29d-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa29d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa29d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa29d-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa29d-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fa29d-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa29d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa29d-125">-ResourceId</span></span>
<span data-ttu-id="fa29d-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="fa29d-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa29d-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fa29d-127">-WorkspaceName</span></span>
<span data-ttu-id="fa29d-128">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="fa29d-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa29d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa29d-129">CommonParameters</span></span>
<span data-ttu-id="fa29d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa29d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa29d-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa29d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa29d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa29d-132">INPUTS</span></span>

### <span data-ttu-id="fa29d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fa29d-133">System.String</span></span>
## <span data-ttu-id="fa29d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa29d-134">OUTPUTS</span></span>

### <span data-ttu-id="fa29d-135">Microsoft. Azure. commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="fa29d-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="fa29d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa29d-136">NOTES</span></span>

## <span data-ttu-id="fa29d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa29d-137">RELATED LINKS</span></span>
