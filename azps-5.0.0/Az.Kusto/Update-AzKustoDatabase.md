---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: eb4c4e8318cf091662a9348ef9e786ec25d5436f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270945"
---
# <span data-ttu-id="a6843-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="a6843-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="a6843-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6843-102">SYNOPSIS</span></span>
<span data-ttu-id="a6843-103">Uppdaterar en databas.</span><span class="sxs-lookup"><span data-stu-id="a6843-103">Updates a database.</span></span>

## <span data-ttu-id="a6843-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6843-104">SYNTAX</span></span>

### <span data-ttu-id="a6843-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="a6843-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6843-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a6843-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6843-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6843-107">DESCRIPTION</span></span>
<span data-ttu-id="a6843-108">Uppdaterar en databas.</span><span class="sxs-lookup"><span data-stu-id="a6843-108">Updates a database.</span></span>

## <span data-ttu-id="a6843-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6843-109">EXAMPLES</span></span>

### <span data-ttu-id="a6843-110">Exempel 1: uppdatera en befintlig databas med namn</span><span class="sxs-lookup"><span data-stu-id="a6843-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="a6843-111">Kommandot ovan uppdaterar den mjuka borttagnings perioden och Kusto-databasen "mykustodatabase" i klustret "testnewkustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="a6843-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="a6843-112">Exempel 2: uppdatera en befintlig databas via identitet</span><span class="sxs-lookup"><span data-stu-id="a6843-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="a6843-113">Kommandot ovan uppdaterar den mjuka borttagnings perioden och Kusto-databasen "mykustodatabase" i klustret "testnewkustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="a6843-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="a6843-114">Exempel 3: uppdatera en befintlig skrivskyddad databas efter namn</span><span class="sxs-lookup"><span data-stu-id="a6843-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="a6843-115">Kommandot ovan uppdaterar under tiden för cacheminnet för Kusto-databasen "mykustodatabase" i klustret "myfollowercluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="a6843-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="a6843-116">Exempel 4: uppdatera en befintlig ReadOnly-databas via identitet</span><span class="sxs-lookup"><span data-stu-id="a6843-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="a6843-117">Kommandot ovan uppdaterar under tiden för cacheminnet för Kusto-databasen "mykustodatabase" i klustret "myfollowercluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="a6843-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="a6843-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6843-118">PARAMETERS</span></span>

### <span data-ttu-id="a6843-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6843-119">-AsJob</span></span>
<span data-ttu-id="a6843-120">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="a6843-120">Run the command as a job</span></span>

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

### <span data-ttu-id="a6843-121">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="a6843-121">-ClusterName</span></span>
<span data-ttu-id="a6843-122">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a6843-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6843-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6843-123">-DefaultProfile</span></span>
<span data-ttu-id="a6843-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a6843-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6843-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="a6843-125">-HotCachePeriod</span></span>
<span data-ttu-id="a6843-126">Tiden som data ska behållas i cacheminnet för snabba frågor i TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="a6843-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6843-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6843-127">-InputObject</span></span>
<span data-ttu-id="a6843-128">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a6843-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6843-129">-Sort</span><span class="sxs-lookup"><span data-stu-id="a6843-129">-Kind</span></span>
<span data-ttu-id="a6843-130">Typ av databas</span><span class="sxs-lookup"><span data-stu-id="a6843-130">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6843-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="a6843-131">-Location</span></span>
<span data-ttu-id="a6843-132">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="a6843-132">Resource location.</span></span>

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

### <span data-ttu-id="a6843-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="a6843-133">-Name</span></span>
<span data-ttu-id="a6843-134">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a6843-134">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6843-135">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a6843-135">-NoWait</span></span>
<span data-ttu-id="a6843-136">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="a6843-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a6843-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6843-137">-ResourceGroupName</span></span>
<span data-ttu-id="a6843-138">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a6843-138">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6843-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="a6843-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="a6843-140">Den tid då informationen ska behållas innan den inte längre är tillgänglig för frågor i TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="a6843-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6843-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6843-141">-SubscriptionId</span></span>
<span data-ttu-id="a6843-142">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a6843-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a6843-143">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="a6843-143">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6843-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a6843-144">-Confirm</span></span>
<span data-ttu-id="a6843-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a6843-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6843-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6843-146">-WhatIf</span></span>
<span data-ttu-id="a6843-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a6843-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6843-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a6843-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6843-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6843-149">CommonParameters</span></span>
<span data-ttu-id="a6843-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6843-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6843-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6843-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6843-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6843-152">INPUTS</span></span>

### <span data-ttu-id="a6843-153">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a6843-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a6843-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6843-154">OUTPUTS</span></span>

### <span data-ttu-id="a6843-155">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="a6843-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="a6843-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6843-156">NOTES</span></span>

<span data-ttu-id="a6843-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a6843-157">ALIASES</span></span>

<span data-ttu-id="a6843-158">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="a6843-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6843-159">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="a6843-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6843-160">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6843-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6843-161">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="a6843-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a6843-162">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="a6843-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a6843-163">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a6843-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a6843-164">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="a6843-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a6843-165">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a6843-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a6843-166">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="a6843-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a6843-167">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="a6843-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a6843-168">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a6843-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a6843-169">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a6843-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a6843-170">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a6843-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a6843-171">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="a6843-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a6843-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6843-172">RELATED LINKS</span></span>
