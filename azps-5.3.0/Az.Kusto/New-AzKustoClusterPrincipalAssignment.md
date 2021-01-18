---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: fafc31700477de968c453002e903b52aa73967d8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524094"
---
# <span data-ttu-id="0e585-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="0e585-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="0e585-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e585-102">SYNOPSIS</span></span>
<span data-ttu-id="0e585-103">Skapa ett Kusto kluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0e585-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="0e585-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e585-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0e585-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e585-105">DESCRIPTION</span></span>
<span data-ttu-id="0e585-106">Skapa ett Kusto kluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0e585-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="0e585-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e585-107">EXAMPLES</span></span>

### <span data-ttu-id="0e585-108">Exempel 1: skapa ett Kusto kluster principalAssignment</span><span class="sxs-lookup"><span data-stu-id="0e585-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="0e585-109">Med kommandot ovan skapas ett Kusto kluster-principalAssignment</span><span class="sxs-lookup"><span data-stu-id="0e585-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="0e585-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e585-110">PARAMETERS</span></span>

### <span data-ttu-id="0e585-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e585-111">-AsJob</span></span>
<span data-ttu-id="0e585-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="0e585-112">Run the command as a job</span></span>

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

### <span data-ttu-id="0e585-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="0e585-113">-ClusterName</span></span>
<span data-ttu-id="0e585-114">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0e585-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0e585-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e585-115">-DefaultProfile</span></span>
<span data-ttu-id="0e585-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e585-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e585-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0e585-117">-NoWait</span></span>
<span data-ttu-id="0e585-118">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="0e585-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0e585-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0e585-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="0e585-120">Namnet på Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0e585-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="0e585-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="0e585-121">-PrincipalId</span></span>
<span data-ttu-id="0e585-122">Huvud-ID som tilldelats till klustrets huvud konto.</span><span class="sxs-lookup"><span data-stu-id="0e585-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="0e585-123">Det kan vara ett e-postmeddelande, ett program-ID eller ett säkerhets grupp namn.</span><span class="sxs-lookup"><span data-stu-id="0e585-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="0e585-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="0e585-124">-PrincipalType</span></span>
<span data-ttu-id="0e585-125">Huvud typ.</span><span class="sxs-lookup"><span data-stu-id="0e585-125">Principal type.</span></span>

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

### <span data-ttu-id="0e585-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e585-126">-ResourceGroupName</span></span>
<span data-ttu-id="0e585-127">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0e585-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0e585-128">-Roll</span><span class="sxs-lookup"><span data-stu-id="0e585-128">-Role</span></span>
<span data-ttu-id="0e585-129">Kluster huvud roll.</span><span class="sxs-lookup"><span data-stu-id="0e585-129">Cluster principal role.</span></span>

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

### <span data-ttu-id="0e585-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e585-130">-SubscriptionId</span></span>
<span data-ttu-id="0e585-131">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0e585-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0e585-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0e585-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0e585-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="0e585-133">-TenantId</span></span>
<span data-ttu-id="0e585-134">Innehavarens ID för huvud kontot</span><span class="sxs-lookup"><span data-stu-id="0e585-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="0e585-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0e585-135">-Confirm</span></span>
<span data-ttu-id="0e585-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0e585-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e585-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e585-137">-WhatIf</span></span>
<span data-ttu-id="0e585-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0e585-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e585-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0e585-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e585-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e585-140">CommonParameters</span></span>
<span data-ttu-id="0e585-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e585-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e585-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e585-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e585-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e585-143">INPUTS</span></span>

## <span data-ttu-id="0e585-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e585-144">OUTPUTS</span></span>

### <span data-ttu-id="0e585-145">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200918. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="0e585-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="0e585-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e585-146">NOTES</span></span>

<span data-ttu-id="0e585-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0e585-147">ALIASES</span></span>

## <span data-ttu-id="0e585-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e585-148">RELATED LINKS</span></span>

