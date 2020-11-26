---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6dc016e717e89ad60e066be1c1d86e5871309d9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270462"
---
# <span data-ttu-id="ecd97-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="ecd97-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="ecd97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecd97-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd97-103">Samla in Azure aktivitets logg från angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ecd97-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="ecd97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecd97-104">SYNTAX</span></span>

### <span data-ttu-id="ecd97-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="ecd97-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecd97-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ecd97-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecd97-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecd97-107">DESCRIPTION</span></span>
<span data-ttu-id="ecd97-108">New-AzOperationalInsightsAzureActivityLogDataSource Aktivera logg analys för att samla in Azure aktivitets logg från angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ecd97-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="ecd97-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecd97-109">EXAMPLES</span></span>

### <span data-ttu-id="ecd97-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ecd97-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ecd97-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="ecd97-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="ecd97-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecd97-112">PARAMETERS</span></span>

### <span data-ttu-id="ecd97-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="ecd97-113">-BackfillStartTime</span></span>
<span data-ttu-id="ecd97-114">Du kan välja att använda alla slutfyllnings loggar från en vecka sedan.</span><span class="sxs-lookup"><span data-stu-id="ecd97-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd97-115">-DefaultProfile</span></span>
<span data-ttu-id="ecd97-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ecd97-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecd97-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ecd97-117">-Force</span></span>
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

### <span data-ttu-id="ecd97-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ecd97-118">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd97-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd97-119">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd97-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecd97-120">-SubscriptionId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd97-121">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="ecd97-121">-Workspace</span></span>
```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd97-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ecd97-122">-WorkspaceName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd97-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ecd97-123">-Confirm</span></span>
<span data-ttu-id="ecd97-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ecd97-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecd97-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd97-125">-WhatIf</span></span>
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

### <span data-ttu-id="ecd97-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd97-126">CommonParameters</span></span>
<span data-ttu-id="ecd97-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd97-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd97-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecd97-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd97-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecd97-129">INPUTS</span></span>

### <span data-ttu-id="ecd97-130">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ecd97-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ecd97-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ecd97-131">System.String</span></span>

### <span data-ttu-id="ecd97-132">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ecd97-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="ecd97-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecd97-133">OUTPUTS</span></span>

### <span data-ttu-id="ecd97-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ecd97-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ecd97-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecd97-135">NOTES</span></span>

## <span data-ttu-id="ecd97-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecd97-136">RELATED LINKS</span></span>