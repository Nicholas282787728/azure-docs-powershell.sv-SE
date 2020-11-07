---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 01ca3c42db57760f23e49f93fc7e4d533b4047b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744404"
---
# <span data-ttu-id="db5bf-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="db5bf-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="db5bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="db5bf-103">Stoppar pågående synkronisering för en resurs prenumeration.</span><span class="sxs-lookup"><span data-stu-id="db5bf-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="db5bf-104">Ett resurs-abonnemang kan anges via dess resurs-ID eller dess namn.</span><span class="sxs-lookup"><span data-stu-id="db5bf-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="db5bf-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db5bf-105">SYNTAX</span></span>

### <span data-ttu-id="db5bf-106">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="db5bf-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5bf-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5bf-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5bf-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5bf-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db5bf-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db5bf-109">DESCRIPTION</span></span>
<span data-ttu-id="db5bf-110">Cmdleten **Stop-AzDataShareSubscriptionSynchronization** stoppar pågående synkronisering för en resurs prenumeration</span><span class="sxs-lookup"><span data-stu-id="db5bf-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="db5bf-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db5bf-111">EXAMPLES</span></span>

### <span data-ttu-id="db5bf-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="db5bf-112">Example 1</span></span>
```
PS C:\> Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId 20a4416b-b33b-4539-a908-71dc8ef698fb

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Canceled
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="db5bf-113">Stoppar pågående synkronisering som identifieras av ID-20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="db5bf-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="db5bf-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db5bf-114">PARAMETERS</span></span>

### <span data-ttu-id="db5bf-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="db5bf-115">-AccountName</span></span>
<span data-ttu-id="db5bf-116">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="db5bf-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5bf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db5bf-117">-AsJob</span></span>
<span data-ttu-id="db5bf-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="db5bf-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="db5bf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db5bf-119">-DefaultProfile</span></span>
<span data-ttu-id="db5bf-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db5bf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db5bf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db5bf-121">-InputObject</span></span>
<span data-ttu-id="db5bf-122">Abonnemang för Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="db5bf-122">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db5bf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db5bf-123">-ResourceGroupName</span></span>
<span data-ttu-id="db5bf-124">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="db5bf-124">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5bf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db5bf-125">-ResourceId</span></span>
<span data-ttu-id="db5bf-126">Resurs-ID för Azure Share-prenumerationen</span><span class="sxs-lookup"><span data-stu-id="db5bf-126">The resource id of the azure share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db5bf-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="db5bf-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="db5bf-128">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="db5bf-128">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5bf-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="db5bf-129">-SynchronizationId</span></span>
<span data-ttu-id="db5bf-130">Synkroniserings-ID som måste avbrytas</span><span class="sxs-lookup"><span data-stu-id="db5bf-130">Synchronization id that needs to be stopped</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5bf-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db5bf-131">-Confirm</span></span>
<span data-ttu-id="db5bf-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db5bf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db5bf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db5bf-133">-WhatIf</span></span>
<span data-ttu-id="db5bf-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db5bf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db5bf-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db5bf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db5bf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db5bf-136">CommonParameters</span></span>
<span data-ttu-id="db5bf-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db5bf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db5bf-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db5bf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db5bf-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db5bf-139">INPUTS</span></span>

### <span data-ttu-id="db5bf-140">System. String</span><span class="sxs-lookup"><span data-stu-id="db5bf-140">System.String</span></span>

### <span data-ttu-id="db5bf-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="db5bf-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="db5bf-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db5bf-142">OUTPUTS</span></span>

### <span data-ttu-id="db5bf-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="db5bf-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="db5bf-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db5bf-144">NOTES</span></span>

## <span data-ttu-id="db5bf-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db5bf-145">RELATED LINKS</span></span>