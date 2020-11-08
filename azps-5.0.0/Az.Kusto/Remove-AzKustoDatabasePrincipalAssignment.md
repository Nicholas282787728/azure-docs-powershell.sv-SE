---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: cd29af9ac8569683e6447a51f4d4f6784139f735
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272203"
---
# <span data-ttu-id="f6144-101">Remove-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f6144-101">Remove-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="f6144-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6144-102">SYNOPSIS</span></span>
<span data-ttu-id="f6144-103">Tar bort en Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f6144-103">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="f6144-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6144-104">SYNTAX</span></span>

### <span data-ttu-id="f6144-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="f6144-105">Delete (Default)</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f6144-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f6144-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f6144-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6144-107">DESCRIPTION</span></span>
<span data-ttu-id="f6144-108">Tar bort en Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f6144-108">Deletes a Kusto principalAssignment.</span></span>

## <span data-ttu-id="f6144-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6144-109">EXAMPLES</span></span>

### <span data-ttu-id="f6144-110">Exempel 1: ta bort en befintlig Kusto-databas PrincipalAssignment efter namn</span><span class="sxs-lookup"><span data-stu-id="f6144-110">Example 1: Delete an existing Kusto database PrincipalAssignment by name</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1
```

<span data-ttu-id="f6144-111">Kommandot ovan tar bort PrincipalAssignment med namnet "kustoprincipal1" i Kusto-databasen "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="f6144-111">The above command deletes the PrincipalAssignment named "kustoprincipal1" in the Kusto database  "mykustodatabase".</span></span>

## <span data-ttu-id="f6144-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6144-112">PARAMETERS</span></span>

### <span data-ttu-id="f6144-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6144-113">-AsJob</span></span>
<span data-ttu-id="f6144-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="f6144-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f6144-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="f6144-115">-ClusterName</span></span>
<span data-ttu-id="f6144-116">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="f6144-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f6144-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f6144-117">-DatabaseName</span></span>
<span data-ttu-id="f6144-118">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="f6144-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f6144-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6144-119">-DefaultProfile</span></span>
<span data-ttu-id="f6144-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6144-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6144-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6144-121">-InputObject</span></span>
<span data-ttu-id="f6144-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f6144-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f6144-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f6144-123">-NoWait</span></span>
<span data-ttu-id="f6144-124">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="f6144-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f6144-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6144-125">-PassThru</span></span>
<span data-ttu-id="f6144-126">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="f6144-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f6144-127">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f6144-127">-PrincipalAssignmentName</span></span>
<span data-ttu-id="f6144-128">Namnet på Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f6144-128">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="f6144-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6144-129">-ResourceGroupName</span></span>
<span data-ttu-id="f6144-130">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="f6144-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f6144-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6144-131">-SubscriptionId</span></span>
<span data-ttu-id="f6144-132">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f6144-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f6144-133">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="f6144-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f6144-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f6144-134">-Confirm</span></span>
<span data-ttu-id="f6144-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6144-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6144-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6144-136">-WhatIf</span></span>
<span data-ttu-id="f6144-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f6144-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6144-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f6144-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6144-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6144-139">CommonParameters</span></span>
<span data-ttu-id="f6144-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6144-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6144-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6144-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6144-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6144-142">INPUTS</span></span>

### <span data-ttu-id="f6144-143">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f6144-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f6144-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6144-144">OUTPUTS</span></span>

### <span data-ttu-id="f6144-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f6144-145">System.Boolean</span></span>

## <span data-ttu-id="f6144-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6144-146">NOTES</span></span>

<span data-ttu-id="f6144-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f6144-147">ALIASES</span></span>

<span data-ttu-id="f6144-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="f6144-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6144-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="f6144-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6144-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f6144-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6144-151">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="f6144-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6144-152">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f6144-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f6144-153">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="f6144-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f6144-154">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="f6144-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f6144-155">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="f6144-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f6144-156">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="f6144-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6144-157">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="f6144-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f6144-158">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f6144-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f6144-159">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="f6144-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f6144-160">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f6144-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f6144-161">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="f6144-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f6144-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6144-162">RELATED LINKS</span></span>

