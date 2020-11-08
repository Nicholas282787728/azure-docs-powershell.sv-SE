---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 8f2a0cd576c3fe7f184d3f016f6666aa8749b5c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261274"
---
# <span data-ttu-id="9a450-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="9a450-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="9a450-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a450-102">SYNOPSIS</span></span>
<span data-ttu-id="9a450-103">Skapa ett Kusto kluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="9a450-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="9a450-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a450-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9a450-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a450-105">DESCRIPTION</span></span>
<span data-ttu-id="9a450-106">Skapa ett Kusto kluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="9a450-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="9a450-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a450-107">EXAMPLES</span></span>

### <span data-ttu-id="9a450-108">Exempel 1: skapa ett Kusto kluster principalAssignment</span><span class="sxs-lookup"><span data-stu-id="9a450-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="9a450-109">Med kommandot ovan skapas ett Kusto kluster-principalAssignment</span><span class="sxs-lookup"><span data-stu-id="9a450-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="9a450-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a450-110">PARAMETERS</span></span>

### <span data-ttu-id="9a450-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a450-111">-AsJob</span></span>
<span data-ttu-id="9a450-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="9a450-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9a450-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="9a450-113">-ClusterName</span></span>
<span data-ttu-id="9a450-114">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="9a450-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="9a450-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a450-115">-DefaultProfile</span></span>
<span data-ttu-id="9a450-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a450-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a450-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9a450-117">-NoWait</span></span>
<span data-ttu-id="9a450-118">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="9a450-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9a450-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="9a450-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="9a450-120">Namnet på Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="9a450-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="9a450-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="9a450-121">-PrincipalId</span></span>
<span data-ttu-id="9a450-122">Huvud-ID som tilldelats till klustrets huvud konto.</span><span class="sxs-lookup"><span data-stu-id="9a450-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="9a450-123">Det kan vara ett e-postmeddelande, ett program-ID eller ett säkerhets grupp namn.</span><span class="sxs-lookup"><span data-stu-id="9a450-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="9a450-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="9a450-124">-PrincipalType</span></span>
<span data-ttu-id="9a450-125">Huvud typ.</span><span class="sxs-lookup"><span data-stu-id="9a450-125">Principal type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.PrincipalType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a450-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a450-126">-ResourceGroupName</span></span>
<span data-ttu-id="9a450-127">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="9a450-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9a450-128">-Roll</span><span class="sxs-lookup"><span data-stu-id="9a450-128">-Role</span></span>
<span data-ttu-id="9a450-129">Kluster huvud roll.</span><span class="sxs-lookup"><span data-stu-id="9a450-129">Cluster principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.ClusterPrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a450-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9a450-130">-SubscriptionId</span></span>
<span data-ttu-id="9a450-131">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9a450-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9a450-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9a450-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9a450-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="9a450-133">-TenantId</span></span>
<span data-ttu-id="9a450-134">Innehavarens ID för huvud kontot</span><span class="sxs-lookup"><span data-stu-id="9a450-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="9a450-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9a450-135">-Confirm</span></span>
<span data-ttu-id="9a450-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9a450-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a450-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a450-137">-WhatIf</span></span>
<span data-ttu-id="9a450-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9a450-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a450-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9a450-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a450-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a450-140">CommonParameters</span></span>
<span data-ttu-id="9a450-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a450-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a450-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a450-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a450-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a450-143">INPUTS</span></span>

## <span data-ttu-id="9a450-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a450-144">OUTPUTS</span></span>

### <span data-ttu-id="9a450-145">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="9a450-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="9a450-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a450-146">NOTES</span></span>

<span data-ttu-id="9a450-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9a450-147">ALIASES</span></span>

## <span data-ttu-id="9a450-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a450-148">RELATED LINKS</span></span>

