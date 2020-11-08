---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272527"
---
# <span data-ttu-id="4eb39-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="4eb39-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="4eb39-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4eb39-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb39-103">Skapar ett nytt alias och en ny prenumeration</span><span class="sxs-lookup"><span data-stu-id="4eb39-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="4eb39-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4eb39-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb39-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4eb39-105">DESCRIPTION</span></span>
<span data-ttu-id="4eb39-106">**New-AzSubscriptionAlias** cmdlet skapar ett nytt alias och en ny prenumeration</span><span class="sxs-lookup"><span data-stu-id="4eb39-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="4eb39-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4eb39-107">EXAMPLES</span></span>

### <span data-ttu-id="4eb39-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4eb39-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="4eb39-109">Skapar ett nytt alias och en ny prenumeration</span><span class="sxs-lookup"><span data-stu-id="4eb39-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="4eb39-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4eb39-110">PARAMETERS</span></span>

### <span data-ttu-id="4eb39-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="4eb39-111">-AliasName</span></span>
<span data-ttu-id="4eb39-112">Alias för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="4eb39-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="4eb39-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4eb39-113">-AsJob</span></span>
<span data-ttu-id="4eb39-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4eb39-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4eb39-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="4eb39-115">-BillingScope</span></span>
<span data-ttu-id="4eb39-116">Fakturerings omfattning</span><span class="sxs-lookup"><span data-stu-id="4eb39-116">Billing Scope</span></span>

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

### <span data-ttu-id="4eb39-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb39-117">-DefaultProfile</span></span>
<span data-ttu-id="4eb39-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4eb39-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eb39-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="4eb39-119">-ResellerId</span></span>
<span data-ttu-id="4eb39-120">Åter försäljar-ID</span><span class="sxs-lookup"><span data-stu-id="4eb39-120">Reseller Id</span></span>

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

### <span data-ttu-id="4eb39-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4eb39-121">-SubscriptionId</span></span>
<span data-ttu-id="4eb39-122">Befintligt abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="4eb39-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="4eb39-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4eb39-123">-SubscriptionName</span></span>
<span data-ttu-id="4eb39-124">Namnet på abonnemanget</span><span class="sxs-lookup"><span data-stu-id="4eb39-124">Name of the subscription</span></span>

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

### <span data-ttu-id="4eb39-125">-Arbets belastning</span><span class="sxs-lookup"><span data-stu-id="4eb39-125">-Workload</span></span>
<span data-ttu-id="4eb39-126">Typ av arbets belastning</span><span class="sxs-lookup"><span data-stu-id="4eb39-126">Type of Workload</span></span>

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

### <span data-ttu-id="4eb39-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4eb39-127">-Confirm</span></span>
<span data-ttu-id="4eb39-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4eb39-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb39-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb39-129">-WhatIf</span></span>
<span data-ttu-id="4eb39-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4eb39-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb39-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4eb39-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb39-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb39-132">CommonParameters</span></span>
<span data-ttu-id="4eb39-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb39-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb39-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4eb39-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb39-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4eb39-135">INPUTS</span></span>

### <span data-ttu-id="4eb39-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="4eb39-136">None</span></span>

## <span data-ttu-id="4eb39-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4eb39-137">OUTPUTS</span></span>

### <span data-ttu-id="4eb39-138">Microsoft. Azure. commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="4eb39-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="4eb39-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4eb39-139">NOTES</span></span>

## <span data-ttu-id="4eb39-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4eb39-140">RELATED LINKS</span></span>
