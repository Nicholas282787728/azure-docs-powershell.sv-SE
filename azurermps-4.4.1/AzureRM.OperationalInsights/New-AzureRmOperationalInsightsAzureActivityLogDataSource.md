---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 15138ee817cddb992f5b6bbe0beccee10620ffdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577580"
---
# <span data-ttu-id="d2e92-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="d2e92-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="d2e92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2e92-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e92-103">Samla in Azure aktivitets logg från angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="d2e92-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2e92-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2e92-104">SYNTAX</span></span>

### <span data-ttu-id="d2e92-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="d2e92-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2e92-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d2e92-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2e92-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2e92-107">DESCRIPTION</span></span>
<span data-ttu-id="d2e92-108">New-AzureRmOperationalInsightsAzureActivityLogDataSource Aktivera logg analys för att samla in Azure aktivitets logg från angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="d2e92-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="d2e92-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2e92-109">EXAMPLES</span></span>

### <span data-ttu-id="d2e92-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d2e92-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d2e92-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="d2e92-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="d2e92-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2e92-112">PARAMETERS</span></span>

### <span data-ttu-id="d2e92-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="d2e92-113">-BackfillStartTime</span></span>
<span data-ttu-id="d2e92-114">Du kan välja att använda alla slutfyllnings loggar från en vecka sedan.</span><span class="sxs-lookup"><span data-stu-id="d2e92-114">You can choose to backfill logs from a week ago.</span></span>

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

### <span data-ttu-id="d2e92-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d2e92-115">-Force</span></span>
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

### <span data-ttu-id="d2e92-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="d2e92-116">-Name</span></span>
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

### <span data-ttu-id="d2e92-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e92-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d2e92-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2e92-118">-SubscriptionId</span></span>
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

### <span data-ttu-id="d2e92-119">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="d2e92-119">-Workspace</span></span>
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

### <span data-ttu-id="d2e92-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d2e92-120">-WorkspaceName</span></span>
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

### <span data-ttu-id="d2e92-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d2e92-121">-Confirm</span></span>
<span data-ttu-id="d2e92-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d2e92-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2e92-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2e92-123">-WhatIf</span></span>
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

### <span data-ttu-id="d2e92-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e92-124">-DefaultProfile</span></span>
<span data-ttu-id="d2e92-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e92-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2e92-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e92-126">CommonParameters</span></span>
<span data-ttu-id="d2e92-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2e92-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e92-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e92-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e92-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2e92-129">INPUTS</span></span>

### <span data-ttu-id="d2e92-130">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d2e92-130">PSWorkspace</span></span>
<span data-ttu-id="d2e92-131">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d2e92-131">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="d2e92-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2e92-132">OUTPUTS</span></span>

### <span data-ttu-id="d2e92-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d2e92-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d2e92-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2e92-134">NOTES</span></span>

## <span data-ttu-id="d2e92-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2e92-135">RELATED LINKS</span></span>

