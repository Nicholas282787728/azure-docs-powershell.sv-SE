---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 8bfcb3a96ee8db53a6a869a01441739ee9c503bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272221"
---
# <span data-ttu-id="fbeb4-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="fbeb4-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="fbeb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fbeb4-102">SYNOPSIS</span></span>
<span data-ttu-id="fbeb4-103">Skapar en Kusto med kluster databas principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="fbeb4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fbeb4-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fbeb4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fbeb4-105">DESCRIPTION</span></span>
<span data-ttu-id="fbeb4-106">Skapar en Kusto med kluster databas principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="fbeb4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fbeb4-107">EXAMPLES</span></span>

### <span data-ttu-id="fbeb4-108">Exempel 1: skapa en Kusto-principalAssignment</span><span class="sxs-lookup"><span data-stu-id="fbeb4-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="fbeb4-109">Med kommandot ovan skapas en Kusto-principalAssignment</span><span class="sxs-lookup"><span data-stu-id="fbeb4-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="fbeb4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fbeb4-110">PARAMETERS</span></span>

### <span data-ttu-id="fbeb4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbeb4-111">-AsJob</span></span>
<span data-ttu-id="fbeb4-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="fbeb4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="fbeb4-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="fbeb4-113">-ClusterName</span></span>
<span data-ttu-id="fbeb4-114">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="fbeb4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fbeb4-115">-DatabaseName</span></span>
<span data-ttu-id="fbeb4-116">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="fbeb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbeb4-117">-DefaultProfile</span></span>
<span data-ttu-id="fbeb4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbeb4-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="fbeb4-119">-NoWait</span></span>
<span data-ttu-id="fbeb4-120">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="fbeb4-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fbeb4-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="fbeb4-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="fbeb4-122">Namnet på Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="fbeb4-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="fbeb4-123">-PrincipalId</span></span>
<span data-ttu-id="fbeb4-124">Huvud-ID som tilldelats till databasens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="fbeb4-125">Det kan vara ett e-postmeddelande, ett program-ID eller ett säkerhets grupp namn.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="fbeb4-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="fbeb4-126">-PrincipalType</span></span>
<span data-ttu-id="fbeb4-127">Huvud typ.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-127">Principal type.</span></span>

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

### <span data-ttu-id="fbeb4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbeb4-128">-ResourceGroupName</span></span>
<span data-ttu-id="fbeb4-129">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="fbeb4-130">-Roll</span><span class="sxs-lookup"><span data-stu-id="fbeb4-130">-Role</span></span>
<span data-ttu-id="fbeb4-131">Rollen som databas säkerhets objekt.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-131">Database principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DatabasePrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbeb4-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fbeb4-132">-SubscriptionId</span></span>
<span data-ttu-id="fbeb4-133">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fbeb4-134">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fbeb4-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="fbeb4-135">-TenantId</span></span>
<span data-ttu-id="fbeb4-136">Innehavarens ID för huvud kontot</span><span class="sxs-lookup"><span data-stu-id="fbeb4-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="fbeb4-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fbeb4-137">-Confirm</span></span>
<span data-ttu-id="fbeb4-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbeb4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbeb4-139">-WhatIf</span></span>
<span data-ttu-id="fbeb4-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbeb4-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbeb4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbeb4-142">CommonParameters</span></span>
<span data-ttu-id="fbeb4-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbeb4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbeb4-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbeb4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbeb4-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fbeb4-145">INPUTS</span></span>

## <span data-ttu-id="fbeb4-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fbeb4-146">OUTPUTS</span></span>

### <span data-ttu-id="fbeb4-147">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="fbeb4-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="fbeb4-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fbeb4-148">NOTES</span></span>

<span data-ttu-id="fbeb4-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fbeb4-149">ALIASES</span></span>

## <span data-ttu-id="fbeb4-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fbeb4-150">RELATED LINKS</span></span>
