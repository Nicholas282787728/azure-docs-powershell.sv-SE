---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: a0f8651bab30cf5a439b6e16110b34e7d256aa3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089553"
---
# <span data-ttu-id="dfcaf-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="dfcaf-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="dfcaf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfcaf-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcaf-103">Skapar en trigger för Share-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="dfcaf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfcaf-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfcaf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfcaf-105">DESCRIPTION</span></span>
<span data-ttu-id="dfcaf-106">Cmdleten **New-AzDataShareTrigger** skapar en trigger för Share-prenumeration för det angivna upprepnings intervallet och synkroniseringstid under Azure Data Share-konto.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="dfcaf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfcaf-107">EXAMPLES</span></span>

### <span data-ttu-id="dfcaf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dfcaf-108">Example 1</span></span>
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

<span data-ttu-id="dfcaf-109">Det här kommandot skapar ett nytt utlösare-AdsTrigger för dela abonnemang AdsShareSubscription med ett dagligt upprepnings intervall på 9 am.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="dfcaf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfcaf-110">PARAMETERS</span></span>

### <span data-ttu-id="dfcaf-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dfcaf-111">-AccountName</span></span>
<span data-ttu-id="dfcaf-112">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="dfcaf-112">Azure data share account name</span></span>

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

### <span data-ttu-id="dfcaf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfcaf-113">-AsJob</span></span>
<span data-ttu-id="dfcaf-114">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="dfcaf-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="dfcaf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcaf-115">-DefaultProfile</span></span>
<span data-ttu-id="dfcaf-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfcaf-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="dfcaf-117">-Name</span></span>
<span data-ttu-id="dfcaf-118">Namn på Azure Data Share-avtryckare</span><span class="sxs-lookup"><span data-stu-id="dfcaf-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="dfcaf-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="dfcaf-119">-RecurrenceInterval</span></span>
<span data-ttu-id="dfcaf-120">Upprepnings intervall för utlösaren (dag eller timme)</span><span class="sxs-lookup"><span data-stu-id="dfcaf-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="dfcaf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfcaf-121">-ResourceGroupName</span></span>
<span data-ttu-id="dfcaf-122">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="dfcaf-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="dfcaf-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="dfcaf-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="dfcaf-124">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="dfcaf-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="dfcaf-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="dfcaf-125">-SynchronizationTime</span></span>
<span data-ttu-id="dfcaf-126">Start tiden för den schemalagda synkroniseringen för utlösaren</span><span class="sxs-lookup"><span data-stu-id="dfcaf-126">The start time of the scheduled synchronization for the trigger</span></span>

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

### <span data-ttu-id="dfcaf-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dfcaf-127">-Confirm</span></span>
<span data-ttu-id="dfcaf-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfcaf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfcaf-129">-WhatIf</span></span>
<span data-ttu-id="dfcaf-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfcaf-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfcaf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcaf-132">CommonParameters</span></span>
<span data-ttu-id="dfcaf-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcaf-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfcaf-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcaf-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfcaf-135">INPUTS</span></span>

### <span data-ttu-id="dfcaf-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="dfcaf-136">None</span></span>

## <span data-ttu-id="dfcaf-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfcaf-137">OUTPUTS</span></span>

### <span data-ttu-id="dfcaf-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="dfcaf-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="dfcaf-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfcaf-139">NOTES</span></span>

## <span data-ttu-id="dfcaf-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfcaf-140">RELATED LINKS</span></span>
