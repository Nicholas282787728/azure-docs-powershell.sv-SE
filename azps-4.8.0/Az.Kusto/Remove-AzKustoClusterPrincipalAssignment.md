---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 92d6855753bdf56941d6f6ca85ec021228894a2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102266"
---
# <span data-ttu-id="0903f-101">Remove-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="0903f-101">Remove-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="0903f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0903f-102">SYNOPSIS</span></span>
<span data-ttu-id="0903f-103">Tar bort ett Kusto kluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0903f-103">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="0903f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0903f-104">SYNTAX</span></span>

### <span data-ttu-id="0903f-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="0903f-105">Delete (Default)</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0903f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0903f-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0903f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0903f-107">DESCRIPTION</span></span>
<span data-ttu-id="0903f-108">Tar bort ett Kusto kluster principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0903f-108">Deletes a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="0903f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0903f-109">EXAMPLES</span></span>

### <span data-ttu-id="0903f-110">Exempel 1: ta bort ett befintligt Kusto kluster PrincipalAssignment efter namn</span><span class="sxs-lookup"><span data-stu-id="0903f-110">Example 1: Delete an existing Kusto cluster PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="0903f-111">Kommandot ovan tar bort PrincipalAssignment med namnet "kustoprincipal1" i Kusto Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="0903f-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto cluster  "testnewkustocluster".</span></span>

## <span data-ttu-id="0903f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0903f-112">PARAMETERS</span></span>

### <span data-ttu-id="0903f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0903f-113">-AsJob</span></span>
<span data-ttu-id="0903f-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="0903f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0903f-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="0903f-115">-ClusterName</span></span>
<span data-ttu-id="0903f-116">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0903f-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0903f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0903f-117">-DefaultProfile</span></span>
<span data-ttu-id="0903f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0903f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0903f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0903f-119">-InputObject</span></span>
<span data-ttu-id="0903f-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0903f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0903f-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0903f-121">-NoWait</span></span>
<span data-ttu-id="0903f-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="0903f-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0903f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0903f-123">-PassThru</span></span>
<span data-ttu-id="0903f-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="0903f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0903f-125">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0903f-125">-PrincipalAssignmentName</span></span>
<span data-ttu-id="0903f-126">Namnet på Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0903f-126">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0903f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0903f-127">-ResourceGroupName</span></span>
<span data-ttu-id="0903f-128">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0903f-128">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0903f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0903f-129">-SubscriptionId</span></span>
<span data-ttu-id="0903f-130">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0903f-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0903f-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0903f-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0903f-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0903f-132">-Confirm</span></span>
<span data-ttu-id="0903f-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0903f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0903f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0903f-134">-WhatIf</span></span>
<span data-ttu-id="0903f-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0903f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0903f-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0903f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0903f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0903f-137">CommonParameters</span></span>
<span data-ttu-id="0903f-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0903f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0903f-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0903f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0903f-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0903f-140">INPUTS</span></span>

### <span data-ttu-id="0903f-141">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0903f-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0903f-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0903f-142">OUTPUTS</span></span>

### <span data-ttu-id="0903f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0903f-143">System.Boolean</span></span>

## <span data-ttu-id="0903f-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0903f-144">NOTES</span></span>

<span data-ttu-id="0903f-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0903f-145">ALIASES</span></span>

<span data-ttu-id="0903f-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0903f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0903f-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0903f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0903f-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0903f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0903f-149">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0903f-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0903f-150">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="0903f-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0903f-151">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0903f-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0903f-152">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="0903f-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0903f-153">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0903f-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0903f-154">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0903f-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0903f-155">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="0903f-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0903f-156">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0903f-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0903f-157">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0903f-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0903f-158">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0903f-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0903f-159">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0903f-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0903f-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0903f-160">RELATED LINKS</span></span>

