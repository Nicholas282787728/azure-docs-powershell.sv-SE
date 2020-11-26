---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272510"
---
# <span data-ttu-id="a0c03-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0c03-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="a0c03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0c03-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c03-103">Skapa eller uppdatera en åtkomst princip i den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="a0c03-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="a0c03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0c03-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a0c03-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0c03-105">DESCRIPTION</span></span>
<span data-ttu-id="a0c03-106">Skapa eller uppdatera en åtkomst princip i den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="a0c03-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="a0c03-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0c03-107">EXAMPLES</span></span>

### <span data-ttu-id="a0c03-108">Exempel 1: skapa en åtkomst princip för en angiven miljö</span><span class="sxs-lookup"><span data-stu-id="a0c03-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="a0c03-109">Det här kommandot skapar en åtkomst princip för en angiven miljö.</span><span class="sxs-lookup"><span data-stu-id="a0c03-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="a0c03-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0c03-110">PARAMETERS</span></span>

### <span data-ttu-id="a0c03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c03-111">-DefaultProfile</span></span>
<span data-ttu-id="a0c03-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0c03-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c03-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a0c03-113">-Description</span></span>
<span data-ttu-id="a0c03-114">En beskrivning av åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="a0c03-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="a0c03-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a0c03-115">-EnvironmentName</span></span>
<span data-ttu-id="a0c03-116">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a0c03-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="a0c03-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a0c03-117">-Name</span></span>
<span data-ttu-id="a0c03-118">Namn på åtkomst policyn.</span><span class="sxs-lookup"><span data-stu-id="a0c03-118">Name of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c03-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="a0c03-119">-PrincipalObjectId</span></span>
<span data-ttu-id="a0c03-120">Objektets objectId i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a0c03-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="a0c03-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0c03-121">-ResourceGroupName</span></span>
<span data-ttu-id="a0c03-122">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a0c03-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a0c03-123">-Roll</span><span class="sxs-lookup"><span data-stu-id="a0c03-123">-Role</span></span>
<span data-ttu-id="a0c03-124">Listan med roller som huvud kontot har tilldelats i miljön.</span><span class="sxs-lookup"><span data-stu-id="a0c03-124">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c03-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0c03-125">-SubscriptionId</span></span>
<span data-ttu-id="a0c03-126">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a0c03-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0c03-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a0c03-127">-Confirm</span></span>
<span data-ttu-id="a0c03-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a0c03-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0c03-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0c03-129">-WhatIf</span></span>
<span data-ttu-id="a0c03-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0c03-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0c03-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a0c03-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0c03-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c03-132">CommonParameters</span></span>
<span data-ttu-id="a0c03-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0c03-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c03-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0c03-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c03-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0c03-135">INPUTS</span></span>

## <span data-ttu-id="a0c03-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0c03-136">OUTPUTS</span></span>

### <span data-ttu-id="a0c03-137">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="a0c03-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="a0c03-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0c03-138">NOTES</span></span>

<span data-ttu-id="a0c03-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a0c03-139">ALIASES</span></span>

## <span data-ttu-id="a0c03-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0c03-140">RELATED LINKS</span></span>
