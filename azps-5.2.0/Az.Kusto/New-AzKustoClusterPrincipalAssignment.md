---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 8f2a0cd576c3fe7f184d3f016f6666aa8749b5c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395768"
---
# <span data-ttu-id="a06c0-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="a06c0-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="a06c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a06c0-102">SYNOPSIS</span></span>
<span data-ttu-id="a06c0-103">Skapa ett Kusto kluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a06c0-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="a06c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a06c0-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a06c0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a06c0-105">DESCRIPTION</span></span>
<span data-ttu-id="a06c0-106">Skapa ett Kusto kluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a06c0-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="a06c0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a06c0-107">EXAMPLES</span></span>

### <span data-ttu-id="a06c0-108">Exempel 1: skapa ett Kusto kluster principalAssignment</span><span class="sxs-lookup"><span data-stu-id="a06c0-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="a06c0-109">Med kommandot ovan skapas ett Kusto kluster-principalAssignment</span><span class="sxs-lookup"><span data-stu-id="a06c0-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="a06c0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a06c0-110">PARAMETERS</span></span>

### <span data-ttu-id="a06c0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a06c0-111">-AsJob</span></span>
<span data-ttu-id="a06c0-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="a06c0-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a06c0-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="a06c0-113">-ClusterName</span></span>
<span data-ttu-id="a06c0-114">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a06c0-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a06c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06c0-115">-DefaultProfile</span></span>
<span data-ttu-id="a06c0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a06c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a06c0-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a06c0-117">-NoWait</span></span>
<span data-ttu-id="a06c0-118">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="a06c0-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a06c0-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="a06c0-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="a06c0-120">Namnet på Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a06c0-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="a06c0-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="a06c0-121">-PrincipalId</span></span>
<span data-ttu-id="a06c0-122">Huvud-ID som tilldelats till klustrets huvud konto.</span><span class="sxs-lookup"><span data-stu-id="a06c0-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="a06c0-123">Det kan vara ett e-postmeddelande, ett program-ID eller ett säkerhets grupp namn.</span><span class="sxs-lookup"><span data-stu-id="a06c0-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="a06c0-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="a06c0-124">-PrincipalType</span></span>
<span data-ttu-id="a06c0-125">Huvud typ.</span><span class="sxs-lookup"><span data-stu-id="a06c0-125">Principal type.</span></span>

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

### <span data-ttu-id="a06c0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a06c0-126">-ResourceGroupName</span></span>
<span data-ttu-id="a06c0-127">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a06c0-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a06c0-128">-Roll</span><span class="sxs-lookup"><span data-stu-id="a06c0-128">-Role</span></span>
<span data-ttu-id="a06c0-129">Kluster huvud roll.</span><span class="sxs-lookup"><span data-stu-id="a06c0-129">Cluster principal role.</span></span>

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

### <span data-ttu-id="a06c0-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a06c0-130">-SubscriptionId</span></span>
<span data-ttu-id="a06c0-131">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a06c0-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a06c0-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="a06c0-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a06c0-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="a06c0-133">-TenantId</span></span>
<span data-ttu-id="a06c0-134">Innehavarens ID för huvud kontot</span><span class="sxs-lookup"><span data-stu-id="a06c0-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="a06c0-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a06c0-135">-Confirm</span></span>
<span data-ttu-id="a06c0-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a06c0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a06c0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a06c0-137">-WhatIf</span></span>
<span data-ttu-id="a06c0-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a06c0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a06c0-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a06c0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a06c0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06c0-140">CommonParameters</span></span>
<span data-ttu-id="a06c0-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a06c0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06c0-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a06c0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06c0-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a06c0-143">INPUTS</span></span>

## <span data-ttu-id="a06c0-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a06c0-144">OUTPUTS</span></span>

### <span data-ttu-id="a06c0-145">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="a06c0-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="a06c0-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a06c0-146">NOTES</span></span>

<span data-ttu-id="a06c0-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a06c0-147">ALIASES</span></span>

## <span data-ttu-id="a06c0-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a06c0-148">RELATED LINKS</span></span>

