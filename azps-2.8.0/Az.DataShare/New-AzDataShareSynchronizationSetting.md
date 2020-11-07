---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: ba8f51832aada036363dea95a8f604b24966e76b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744428"
---
# <span data-ttu-id="ed4a2-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="ed4a2-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="ed4a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed4a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ed4a2-103">Skapar synkroniseringsinställningar för en resurs.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="ed4a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed4a2-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed4a2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed4a2-105">DESCRIPTION</span></span>
<span data-ttu-id="ed4a2-106">Den **nya-AzDataShareSynchronizationSetting** skapar en synkroniseringsinställningar för dela på dela konto för ett upprepnings intervall på antingen varje dag eller varje timme vid en viss tidpunkt.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="ed4a2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed4a2-107">EXAMPLES</span></span>

### <span data-ttu-id="ed4a2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ed4a2-108">Example 1</span></span>
```
PS C:\>  New-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization" -RecurrenceInterval "Day" -SynchronizationTime 9:00
RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : Ads Company
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="ed4a2-109">Med de här kommandona skapar du en synkroniseringsinställningar för varje dagligt upprepnings intervall på 9:00 am för Share AdsShare i WikiAds för data delning.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="ed4a2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed4a2-110">PARAMETERS</span></span>

### <span data-ttu-id="ed4a2-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed4a2-111">-AccountName</span></span>
<span data-ttu-id="ed4a2-112">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="ed4a2-112">Azure data share account name</span></span>

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

### <span data-ttu-id="ed4a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed4a2-113">-DefaultProfile</span></span>
<span data-ttu-id="ed4a2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed4a2-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed4a2-115">-Name</span></span>
<span data-ttu-id="ed4a2-116">Inställnings namn för synkronisering</span><span class="sxs-lookup"><span data-stu-id="ed4a2-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="ed4a2-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="ed4a2-117">-RecurrenceInterval</span></span>
<span data-ttu-id="ed4a2-118">Upprepnings intervallet för synkroniseringsinställningarna (dag eller timme)</span><span class="sxs-lookup"><span data-stu-id="ed4a2-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="ed4a2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed4a2-119">-ResourceGroupName</span></span>
<span data-ttu-id="ed4a2-120">Resurs grupp namn för Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="ed4a2-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="ed4a2-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ed4a2-121">-ShareName</span></span>
<span data-ttu-id="ed4a2-122">Azure Data Share-namn</span><span class="sxs-lookup"><span data-stu-id="ed4a2-122">Azure data share name</span></span>

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

### <span data-ttu-id="ed4a2-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="ed4a2-123">-SynchronizationTime</span></span>
<span data-ttu-id="ed4a2-124">Start tiden för den schemalagda synkroniseringen</span><span class="sxs-lookup"><span data-stu-id="ed4a2-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="ed4a2-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed4a2-125">-Confirm</span></span>
<span data-ttu-id="ed4a2-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed4a2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed4a2-127">-WhatIf</span></span>
<span data-ttu-id="ed4a2-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed4a2-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed4a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed4a2-130">CommonParameters</span></span>
<span data-ttu-id="ed4a2-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed4a2-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed4a2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed4a2-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed4a2-133">INPUTS</span></span>

### <span data-ttu-id="ed4a2-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="ed4a2-134">None</span></span>

## <span data-ttu-id="ed4a2-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed4a2-135">OUTPUTS</span></span>

### <span data-ttu-id="ed4a2-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="ed4a2-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="ed4a2-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed4a2-137">NOTES</span></span>

## <span data-ttu-id="ed4a2-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed4a2-138">RELATED LINKS</span></span>