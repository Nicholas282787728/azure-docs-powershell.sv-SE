---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: e264dce6c99aaee7803881ab5eaa0ef529a53b48
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420611"
---
# <span data-ttu-id="3d733-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="3d733-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="3d733-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d733-102">SYNOPSIS</span></span>
<span data-ttu-id="3d733-103">Skapar en trigger för Share-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="3d733-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="3d733-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d733-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d733-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d733-105">DESCRIPTION</span></span>
<span data-ttu-id="3d733-106">Cmdleten **New-AzDataShareTrigger** skapar en trigger för Share-prenumeration för det angivna upprepnings intervallet och synkroniseringstid under Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="3d733-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="3d733-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d733-107">EXAMPLES</span></span>

### <span data-ttu-id="3d733-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3d733-108">Example 1</span></span>
```
PS C:\> New-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger" -RecurrenceInterval "Day" -SynchronizationTime "9:00"
CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="3d733-109">Det här kommandot skapar ett nytt utlösare-AdsTrigger för dela abonnemang AdsShareSubscription med ett dagligt upprepnings intervall på 9 am.</span><span class="sxs-lookup"><span data-stu-id="3d733-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="3d733-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d733-110">PARAMETERS</span></span>

### <span data-ttu-id="3d733-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3d733-111">-AccountName</span></span>
<span data-ttu-id="3d733-112">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="3d733-112">Azure data share account name</span></span>

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

### <span data-ttu-id="3d733-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d733-113">-AsJob</span></span>
<span data-ttu-id="3d733-114">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="3d733-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="3d733-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d733-115">-DefaultProfile</span></span>
<span data-ttu-id="3d733-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d733-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d733-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d733-117">-Name</span></span>
<span data-ttu-id="3d733-118">Namn på Azure Data Share-avtryckare</span><span class="sxs-lookup"><span data-stu-id="3d733-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="3d733-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="3d733-119">-RecurrenceInterval</span></span>
<span data-ttu-id="3d733-120">Upprepnings intervall för utlösaren (dag eller timme)</span><span class="sxs-lookup"><span data-stu-id="3d733-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="3d733-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d733-121">-ResourceGroupName</span></span>
<span data-ttu-id="3d733-122">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="3d733-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="3d733-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3d733-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="3d733-124">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="3d733-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="3d733-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="3d733-125">-SynchronizationTime</span></span>
<span data-ttu-id="3d733-126">Start tiden för den schemalagda synkroniseringen för utlösaren</span><span class="sxs-lookup"><span data-stu-id="3d733-126">The start time of the scheduled synchronization for the trigger</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d733-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d733-127">-Confirm</span></span>
<span data-ttu-id="3d733-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d733-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d733-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d733-129">-WhatIf</span></span>
<span data-ttu-id="3d733-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d733-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d733-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d733-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d733-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d733-132">CommonParameters</span></span>
<span data-ttu-id="3d733-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d733-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d733-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d733-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d733-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d733-135">INPUTS</span></span>

### <span data-ttu-id="3d733-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="3d733-136">None</span></span>

## <span data-ttu-id="3d733-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d733-137">OUTPUTS</span></span>

### <span data-ttu-id="3d733-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="3d733-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="3d733-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d733-139">NOTES</span></span>

## <span data-ttu-id="3d733-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d733-140">RELATED LINKS</span></span>
