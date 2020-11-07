---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 654663e9fdc44270266aa2872b7deb939be93e83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576143"
---
# <span data-ttu-id="ee41f-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="ee41f-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="ee41f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee41f-102">SYNOPSIS</span></span>
<span data-ttu-id="ee41f-103">Samla in Azure aktivitets logg från angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ee41f-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee41f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee41f-104">SYNTAX</span></span>

### <span data-ttu-id="ee41f-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="ee41f-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee41f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ee41f-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee41f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee41f-107">DESCRIPTION</span></span>
<span data-ttu-id="ee41f-108">New-AzureRmOperationalInsightsAzureActivityLogDataSource Aktivera logg analys för att samla in Azure aktivitets logg från angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ee41f-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="ee41f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee41f-109">EXAMPLES</span></span>

### <span data-ttu-id="ee41f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ee41f-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ee41f-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="ee41f-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="ee41f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee41f-112">PARAMETERS</span></span>

### <span data-ttu-id="ee41f-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="ee41f-113">-BackfillStartTime</span></span>
<span data-ttu-id="ee41f-114">Du kan välja att använda alla slutfyllnings loggar från en vecka sedan.</span><span class="sxs-lookup"><span data-stu-id="ee41f-114">You can choose to backfill logs from a week ago.</span></span>

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

### <span data-ttu-id="ee41f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee41f-115">-DefaultProfile</span></span>
<span data-ttu-id="ee41f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ee41f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee41f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ee41f-117">-Force</span></span>
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

### <span data-ttu-id="ee41f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee41f-118">-Name</span></span>
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

### <span data-ttu-id="ee41f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee41f-119">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ee41f-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee41f-120">-SubscriptionId</span></span>
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

### <span data-ttu-id="ee41f-121">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="ee41f-121">-Workspace</span></span>
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

### <span data-ttu-id="ee41f-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ee41f-122">-WorkspaceName</span></span>
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

### <span data-ttu-id="ee41f-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee41f-123">-Confirm</span></span>
<span data-ttu-id="ee41f-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee41f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee41f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee41f-125">-WhatIf</span></span>
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

### <span data-ttu-id="ee41f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee41f-126">CommonParameters</span></span>
<span data-ttu-id="ee41f-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee41f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee41f-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee41f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee41f-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee41f-129">INPUTS</span></span>

### <span data-ttu-id="ee41f-130">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ee41f-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="ee41f-131">Parametrar: arbets yta (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ee41f-131">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="ee41f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ee41f-132">System.String</span></span>

### <span data-ttu-id="ee41f-133">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ee41f-133">System.DateTimeOffset</span></span>

## <span data-ttu-id="ee41f-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee41f-134">OUTPUTS</span></span>

### <span data-ttu-id="ee41f-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ee41f-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ee41f-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee41f-136">NOTES</span></span>

## <span data-ttu-id="ee41f-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee41f-137">RELATED LINKS</span></span>