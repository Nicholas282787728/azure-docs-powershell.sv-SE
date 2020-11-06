---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6b3009a37a314b70d258f597823f8da062970450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574873"
---
# <span data-ttu-id="bbf2e-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="bbf2e-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="bbf2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bbf2e-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf2e-103">Samla in Azure aktivitets logg från angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="bbf2e-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbf2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bbf2e-104">SYNTAX</span></span>

### <span data-ttu-id="bbf2e-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="bbf2e-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbf2e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bbf2e-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbf2e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bbf2e-107">DESCRIPTION</span></span>
<span data-ttu-id="bbf2e-108">New-AzureRmOperationalInsightsAzureActivityLogDataSource Aktivera logg analys för att samla in Azure aktivitets logg från angiven prenumeration.</span><span class="sxs-lookup"><span data-stu-id="bbf2e-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="bbf2e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bbf2e-109">EXAMPLES</span></span>

### <span data-ttu-id="bbf2e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bbf2e-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="bbf2e-111">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="bbf2e-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="bbf2e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bbf2e-112">PARAMETERS</span></span>

### <span data-ttu-id="bbf2e-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="bbf2e-113">-BackfillStartTime</span></span>
<span data-ttu-id="bbf2e-114">Du kan välja att använda alla slutfyllnings loggar från en vecka sedan.</span><span class="sxs-lookup"><span data-stu-id="bbf2e-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf2e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf2e-115">-DefaultProfile</span></span>
<span data-ttu-id="bbf2e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bbf2e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf2e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bbf2e-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf2e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="bbf2e-118">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf2e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbf2e-119">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf2e-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bbf2e-120">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf2e-121">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="bbf2e-121">-Workspace</span></span>
```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf2e-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bbf2e-122">-WorkspaceName</span></span>
```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf2e-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bbf2e-123">-Confirm</span></span>
<span data-ttu-id="bbf2e-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bbf2e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf2e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbf2e-125">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf2e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf2e-126">CommonParameters</span></span>
<span data-ttu-id="bbf2e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbf2e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf2e-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbf2e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf2e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bbf2e-129">INPUTS</span></span>

### <span data-ttu-id="bbf2e-130">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bbf2e-130">PSWorkspace</span></span>
<span data-ttu-id="bbf2e-131">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="bbf2e-131">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="bbf2e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bbf2e-132">OUTPUTS</span></span>

### <span data-ttu-id="bbf2e-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bbf2e-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bbf2e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bbf2e-134">NOTES</span></span>

## <span data-ttu-id="bbf2e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bbf2e-135">RELATED LINKS</span></span>

