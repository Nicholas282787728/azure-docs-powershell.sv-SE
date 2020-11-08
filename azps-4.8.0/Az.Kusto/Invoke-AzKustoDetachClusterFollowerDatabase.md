---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259578"
---
# <span data-ttu-id="e2f83-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="e2f83-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="e2f83-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2f83-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f83-103">Tar bort alla följare i en databas som ägs av detta kluster.</span><span class="sxs-lookup"><span data-stu-id="e2f83-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="e2f83-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2f83-104">SYNTAX</span></span>

### <span data-ttu-id="e2f83-105">DetachExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="e2f83-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e2f83-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e2f83-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2f83-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2f83-107">DESCRIPTION</span></span>
<span data-ttu-id="e2f83-108">Tar bort alla följare i en databas som ägs av detta kluster.</span><span class="sxs-lookup"><span data-stu-id="e2f83-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="e2f83-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2f83-109">EXAMPLES</span></span>

### <span data-ttu-id="e2f83-110">Exempel 1: ta bort en uppföljnings databas</span><span class="sxs-lookup"><span data-stu-id="e2f83-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="e2f83-111">Kommandot ovan kopplar bort följar-databasen som definierats i AttachedDatabaseConfiguration "myfollowerconfiguration" från kluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="e2f83-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="e2f83-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2f83-112">PARAMETERS</span></span>

### <span data-ttu-id="e2f83-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2f83-113">-AsJob</span></span>
<span data-ttu-id="e2f83-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="e2f83-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e2f83-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e2f83-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="e2f83-116">Resurs namn för den anslutna databas konfigurationen i uppslags klustret.</span><span class="sxs-lookup"><span data-stu-id="e2f83-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="e2f83-117">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="e2f83-117">-ClusterName</span></span>
<span data-ttu-id="e2f83-118">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="e2f83-118">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f83-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="e2f83-119">-ClusterResourceId</span></span>
<span data-ttu-id="e2f83-120">Resurs-ID för klustret som följer en databas som ägs av detta kluster.</span><span class="sxs-lookup"><span data-stu-id="e2f83-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="e2f83-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f83-121">-DefaultProfile</span></span>
<span data-ttu-id="e2f83-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f83-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2f83-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2f83-123">-InputObject</span></span>
<span data-ttu-id="e2f83-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e2f83-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DetachViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f83-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e2f83-125">-NoWait</span></span>
<span data-ttu-id="e2f83-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="e2f83-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e2f83-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2f83-127">-PassThru</span></span>
<span data-ttu-id="e2f83-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="e2f83-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e2f83-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f83-129">-ResourceGroupName</span></span>
<span data-ttu-id="e2f83-130">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="e2f83-130">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f83-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2f83-131">-SubscriptionId</span></span>
<span data-ttu-id="e2f83-132">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e2f83-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e2f83-133">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e2f83-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f83-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e2f83-134">-Confirm</span></span>
<span data-ttu-id="e2f83-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2f83-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2f83-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2f83-136">-WhatIf</span></span>
<span data-ttu-id="e2f83-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2f83-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2f83-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e2f83-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2f83-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f83-139">CommonParameters</span></span>
<span data-ttu-id="e2f83-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2f83-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f83-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2f83-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f83-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2f83-142">INPUTS</span></span>

### <span data-ttu-id="e2f83-143">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e2f83-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e2f83-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2f83-144">OUTPUTS</span></span>

### <span data-ttu-id="e2f83-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2f83-145">System.Boolean</span></span>

## <span data-ttu-id="e2f83-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2f83-146">NOTES</span></span>

<span data-ttu-id="e2f83-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e2f83-147">ALIASES</span></span>

<span data-ttu-id="e2f83-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="e2f83-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e2f83-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="e2f83-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2f83-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e2f83-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e2f83-151">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e2f83-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e2f83-152">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e2f83-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e2f83-153">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="e2f83-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e2f83-154">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="e2f83-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e2f83-155">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="e2f83-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e2f83-156">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e2f83-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e2f83-157">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="e2f83-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e2f83-158">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e2f83-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e2f83-159">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="e2f83-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e2f83-160">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e2f83-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e2f83-161">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e2f83-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e2f83-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2f83-162">RELATED LINKS</span></span>

