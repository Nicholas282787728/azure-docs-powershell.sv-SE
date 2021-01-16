---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415320"
---
# <span data-ttu-id="3a8dc-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="3a8dc-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="3a8dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3a8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="3a8dc-103">Skapar ett nytt alias och en ny prenumeration</span><span class="sxs-lookup"><span data-stu-id="3a8dc-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="3a8dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3a8dc-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a8dc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3a8dc-105">DESCRIPTION</span></span>
<span data-ttu-id="3a8dc-106">**New-AzSubscriptionAlias** cmdlet skapar ett nytt alias och en ny prenumeration</span><span class="sxs-lookup"><span data-stu-id="3a8dc-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="3a8dc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3a8dc-107">EXAMPLES</span></span>

### <span data-ttu-id="3a8dc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3a8dc-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="3a8dc-109">Skapar ett nytt alias och en ny prenumeration</span><span class="sxs-lookup"><span data-stu-id="3a8dc-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="3a8dc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3a8dc-110">PARAMETERS</span></span>

### <span data-ttu-id="3a8dc-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="3a8dc-111">-AliasName</span></span>
<span data-ttu-id="3a8dc-112">Alias för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="3a8dc-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="3a8dc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a8dc-113">-AsJob</span></span>
<span data-ttu-id="3a8dc-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3a8dc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a8dc-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="3a8dc-115">-BillingScope</span></span>
<span data-ttu-id="3a8dc-116">Fakturerings omfattning</span><span class="sxs-lookup"><span data-stu-id="3a8dc-116">Billing Scope</span></span>

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

### <span data-ttu-id="3a8dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a8dc-117">-DefaultProfile</span></span>
<span data-ttu-id="3a8dc-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8dc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a8dc-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="3a8dc-119">-ResellerId</span></span>
<span data-ttu-id="3a8dc-120">Åter försäljar-ID</span><span class="sxs-lookup"><span data-stu-id="3a8dc-120">Reseller Id</span></span>

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

### <span data-ttu-id="3a8dc-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a8dc-121">-SubscriptionId</span></span>
<span data-ttu-id="3a8dc-122">Befintligt abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="3a8dc-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="3a8dc-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3a8dc-123">-SubscriptionName</span></span>
<span data-ttu-id="3a8dc-124">Namnet på abonnemanget</span><span class="sxs-lookup"><span data-stu-id="3a8dc-124">Name of the subscription</span></span>

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

### <span data-ttu-id="3a8dc-125">-Arbets belastning</span><span class="sxs-lookup"><span data-stu-id="3a8dc-125">-Workload</span></span>
<span data-ttu-id="3a8dc-126">Typ av arbets belastning</span><span class="sxs-lookup"><span data-stu-id="3a8dc-126">Type of Workload</span></span>

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

### <span data-ttu-id="3a8dc-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3a8dc-127">-Confirm</span></span>
<span data-ttu-id="3a8dc-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3a8dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a8dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a8dc-129">-WhatIf</span></span>
<span data-ttu-id="3a8dc-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3a8dc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a8dc-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3a8dc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a8dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a8dc-132">CommonParameters</span></span>
<span data-ttu-id="3a8dc-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a8dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a8dc-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a8dc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a8dc-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3a8dc-135">INPUTS</span></span>

### <span data-ttu-id="3a8dc-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="3a8dc-136">None</span></span>

## <span data-ttu-id="3a8dc-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3a8dc-137">OUTPUTS</span></span>

### <span data-ttu-id="3a8dc-138">Microsoft. Azure. commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="3a8dc-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="3a8dc-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3a8dc-139">NOTES</span></span>

## <span data-ttu-id="3a8dc-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3a8dc-140">RELATED LINKS</span></span>
