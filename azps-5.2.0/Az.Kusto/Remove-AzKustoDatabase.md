---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: cfb5eb3c65434f0f62af03bcca57174010041e58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399315"
---
# <span data-ttu-id="d2359-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="d2359-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="d2359-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2359-102">SYNOPSIS</span></span>
<span data-ttu-id="d2359-103">Tar bort databasen med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="d2359-103">Deletes the database with the given name.</span></span>

## <span data-ttu-id="d2359-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2359-104">SYNTAX</span></span>

### <span data-ttu-id="d2359-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="d2359-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d2359-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2359-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2359-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2359-107">DESCRIPTION</span></span>
<span data-ttu-id="d2359-108">Tar bort databasen med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="d2359-108">Deletes the database with the given name.</span></span>

## <span data-ttu-id="d2359-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2359-109">EXAMPLES</span></span>

### <span data-ttu-id="d2359-110">Exempel 1: ta bort en befintlig Kusto-databas efter namn</span><span class="sxs-lookup"><span data-stu-id="d2359-110">Example 1: Delete an existing Kusto database by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
```

<span data-ttu-id="d2359-111">Kommandot ovan tar bort Kusto-databasen med namnet "mykustodatabase" i klustret "testnewkustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="d2359-111">The above command deletes the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="d2359-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2359-112">PARAMETERS</span></span>

### <span data-ttu-id="d2359-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2359-113">-AsJob</span></span>
<span data-ttu-id="d2359-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="d2359-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d2359-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="d2359-115">-ClusterName</span></span>
<span data-ttu-id="d2359-116">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d2359-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d2359-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2359-117">-DefaultProfile</span></span>
<span data-ttu-id="d2359-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2359-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2359-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2359-119">-InputObject</span></span>
<span data-ttu-id="d2359-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d2359-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2359-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d2359-121">-Name</span></span>
<span data-ttu-id="d2359-122">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d2359-122">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2359-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d2359-123">-NoWait</span></span>
<span data-ttu-id="d2359-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="d2359-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d2359-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2359-125">-PassThru</span></span>
<span data-ttu-id="d2359-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="d2359-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d2359-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2359-127">-ResourceGroupName</span></span>
<span data-ttu-id="d2359-128">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d2359-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d2359-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2359-129">-SubscriptionId</span></span>
<span data-ttu-id="d2359-130">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d2359-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d2359-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="d2359-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d2359-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d2359-132">-Confirm</span></span>
<span data-ttu-id="d2359-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d2359-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2359-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2359-134">-WhatIf</span></span>
<span data-ttu-id="d2359-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d2359-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2359-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d2359-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2359-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2359-137">CommonParameters</span></span>
<span data-ttu-id="d2359-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2359-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2359-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2359-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2359-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2359-140">INPUTS</span></span>

### <span data-ttu-id="d2359-141">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d2359-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d2359-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2359-142">OUTPUTS</span></span>

### <span data-ttu-id="d2359-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2359-143">System.Boolean</span></span>

## <span data-ttu-id="d2359-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2359-144">NOTES</span></span>

<span data-ttu-id="d2359-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d2359-145">ALIASES</span></span>

<span data-ttu-id="d2359-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="d2359-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2359-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="d2359-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2359-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d2359-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2359-149">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="d2359-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2359-150">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="d2359-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d2359-151">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d2359-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d2359-152">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="d2359-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d2359-153">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d2359-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d2359-154">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="d2359-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2359-155">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="d2359-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d2359-156">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d2359-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d2359-157">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d2359-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d2359-158">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d2359-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d2359-159">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="d2359-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d2359-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2359-160">RELATED LINKS</span></span>

