---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: bbbcab1e4355667681acf1cc09a51ec6d6174103
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320240"
---
# <span data-ttu-id="77aa3-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="77aa3-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="77aa3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="77aa3-103">Initierar synkronisering för en resurs prenumeration.</span><span class="sxs-lookup"><span data-stu-id="77aa3-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="77aa3-104">Ett resurs-abonnemang kan anges via dess resurs-ID eller dess namn.</span><span class="sxs-lookup"><span data-stu-id="77aa3-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="77aa3-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77aa3-105">SYNTAX</span></span>

### <span data-ttu-id="77aa3-106">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="77aa3-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77aa3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77aa3-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77aa3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77aa3-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77aa3-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77aa3-109">DESCRIPTION</span></span>
<span data-ttu-id="77aa3-110">Cmdleten **Start-AzDataShareSubscriptionSynchronization** initierar synkronisering för en resurs prenumeration</span><span class="sxs-lookup"><span data-stu-id="77aa3-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="77aa3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77aa3-111">EXAMPLES</span></span>

### <span data-ttu-id="77aa3-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="77aa3-112">Example 1</span></span>
```
PS C:\> Start-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationMode Incremental

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 7/9/2019 11:44:41 PM
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Succeeded
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="77aa3-113">Det här kommandot initierar synkronisering för en sharesubscription som heter AdsShareSubscription i Account WikiAds.</span><span class="sxs-lookup"><span data-stu-id="77aa3-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="77aa3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77aa3-114">PARAMETERS</span></span>

### <span data-ttu-id="77aa3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="77aa3-115">-AccountName</span></span>
<span data-ttu-id="77aa3-116">Namn på Azure Data Share-konto</span><span class="sxs-lookup"><span data-stu-id="77aa3-116">Azure data share account name</span></span>

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

### <span data-ttu-id="77aa3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77aa3-117">-AsJob</span></span>
<span data-ttu-id="77aa3-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="77aa3-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="77aa3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77aa3-119">-DefaultProfile</span></span>
<span data-ttu-id="77aa3-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77aa3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77aa3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77aa3-121">-InputObject</span></span>
<span data-ttu-id="77aa3-122">Abonnemang för Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="77aa3-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="77aa3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77aa3-123">-ResourceGroupName</span></span>
<span data-ttu-id="77aa3-124">Resurs grupp namnet för Azure Data Share-kontot</span><span class="sxs-lookup"><span data-stu-id="77aa3-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="77aa3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77aa3-125">-ResourceId</span></span>
<span data-ttu-id="77aa3-126">Resurs-ID för Azure Share-prenumerationen</span><span class="sxs-lookup"><span data-stu-id="77aa3-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="77aa3-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="77aa3-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="77aa3-128">Namn på Azure Data Share-prenumeration</span><span class="sxs-lookup"><span data-stu-id="77aa3-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="77aa3-129">-SynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="77aa3-129">-SynchronizationMode</span></span>
<span data-ttu-id="77aa3-130">Synkroniseringsläge (FullSync eller stegvis)</span><span class="sxs-lookup"><span data-stu-id="77aa3-130">Synchronization mode (FullSync or Incremental)</span></span>

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

### <span data-ttu-id="77aa3-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77aa3-131">-Confirm</span></span>
<span data-ttu-id="77aa3-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77aa3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77aa3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77aa3-133">-WhatIf</span></span>
<span data-ttu-id="77aa3-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77aa3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77aa3-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77aa3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77aa3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77aa3-136">CommonParameters</span></span>
<span data-ttu-id="77aa3-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77aa3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77aa3-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77aa3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77aa3-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77aa3-139">INPUTS</span></span>

### <span data-ttu-id="77aa3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="77aa3-140">System.String</span></span>

### <span data-ttu-id="77aa3-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="77aa3-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="77aa3-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77aa3-142">OUTPUTS</span></span>

### <span data-ttu-id="77aa3-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="77aa3-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="77aa3-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77aa3-144">NOTES</span></span>

## <span data-ttu-id="77aa3-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77aa3-145">RELATED LINKS</span></span>
