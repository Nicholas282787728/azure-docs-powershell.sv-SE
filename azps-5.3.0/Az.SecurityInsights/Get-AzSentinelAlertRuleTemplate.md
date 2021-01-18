---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: aa5dabced1439d8a754e220d56f7309c7b2df3e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525592"
---
# <span data-ttu-id="781a1-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="781a1-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="781a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="781a1-102">SYNOPSIS</span></span>
<span data-ttu-id="781a1-103">Mall för analys regel.</span><span class="sxs-lookup"><span data-stu-id="781a1-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="781a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="781a1-104">SYNTAX</span></span>

### <span data-ttu-id="781a1-105">WorkspaceScope (standard)</span><span class="sxs-lookup"><span data-stu-id="781a1-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="781a1-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="781a1-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="781a1-107">ID</span><span class="sxs-lookup"><span data-stu-id="781a1-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="781a1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="781a1-108">DESCRIPTION</span></span>
<span data-ttu-id="781a1-109">Cmdleten **Get-AzSentinelAlertRuleTemplate** hämtar en mall för notifieringsregler från den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="781a1-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="781a1-110">Om du anger parametern *AlertRuleTemplateId* returneras ett enskilt **AlertRuleTemplate** -objekt.</span><span class="sxs-lookup"><span data-stu-id="781a1-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="781a1-111">Om du inte anger parametern *AlertRuleTemplateId* returneras en matris med alla mallar för notifieringsregler på den angivna arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="781a1-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="781a1-112">Du kan använda **AlertRuleTemplate** -objektet för att skapa en ny notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="781a1-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="781a1-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="781a1-113">EXAMPLES</span></span>

### <span data-ttu-id="781a1-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="781a1-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="781a1-115">Det här exemplet får alla **AlertRuleTemplates** på den angivna arbets ytan och lagrar dem sedan i $AlertRuleTemplates variabel.</span><span class="sxs-lookup"><span data-stu-id="781a1-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="781a1-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="781a1-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="781a1-117">Det här exemplet får en **AlertRuleTemplate** på den angivna arbets ytan och lagrar den sedan i $AlertRuleTemplate variabel.</span><span class="sxs-lookup"><span data-stu-id="781a1-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="781a1-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="781a1-118">PARAMETERS</span></span>

### <span data-ttu-id="781a1-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="781a1-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="781a1-120">ID för regel för notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="781a1-120">Template Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="781a1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="781a1-121">-DefaultProfile</span></span>
<span data-ttu-id="781a1-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="781a1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="781a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="781a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="781a1-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="781a1-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="781a1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="781a1-125">-ResourceId</span></span>
<span data-ttu-id="781a1-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="781a1-126">Resource Id.</span></span>

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

### <span data-ttu-id="781a1-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="781a1-127">-WorkspaceName</span></span>
<span data-ttu-id="781a1-128">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="781a1-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="781a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="781a1-129">CommonParameters</span></span>
<span data-ttu-id="781a1-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="781a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="781a1-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="781a1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="781a1-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="781a1-132">INPUTS</span></span>

### <span data-ttu-id="781a1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="781a1-133">System.String</span></span>
## <span data-ttu-id="781a1-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="781a1-134">OUTPUTS</span></span>

### <span data-ttu-id="781a1-135">Microsoft. Azure. commands. SecurityInsights. Models. AlertRuleTemplates. PSSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="781a1-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="781a1-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="781a1-136">NOTES</span></span>

## <span data-ttu-id="781a1-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="781a1-137">RELATED LINKS</span></span>
