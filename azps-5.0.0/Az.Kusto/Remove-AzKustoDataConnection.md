---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: c04cbc2a92e6fa80c718cb32d95cc4059e4e3a6d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272208"
---
# <span data-ttu-id="9f5ce-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="9f5ce-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="9f5ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5ce-103">Tar bort data anslutningen med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="9f5ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f5ce-104">SYNTAX</span></span>

### <span data-ttu-id="9f5ce-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="9f5ce-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9f5ce-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9f5ce-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9f5ce-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f5ce-107">DESCRIPTION</span></span>
<span data-ttu-id="9f5ce-108">Tar bort data anslutningen med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="9f5ce-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f5ce-109">EXAMPLES</span></span>

### <span data-ttu-id="9f5ce-110">Exempel 1: ta bort en befintlig data anslutning med namn</span><span class="sxs-lookup"><span data-stu-id="9f5ce-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="9f5ce-111">Kommandot ovan tar bort data anslutningen "mykustodataconnection" i databasen "mykustodatabase" för det befintliga klustret "testnewkustocluster" i resurs gruppen "testrg"</span><span class="sxs-lookup"><span data-stu-id="9f5ce-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="9f5ce-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f5ce-112">PARAMETERS</span></span>

### <span data-ttu-id="9f5ce-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f5ce-113">-AsJob</span></span>
<span data-ttu-id="9f5ce-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="9f5ce-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9f5ce-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="9f5ce-115">-ClusterName</span></span>
<span data-ttu-id="9f5ce-116">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="9f5ce-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9f5ce-117">-DatabaseName</span></span>
<span data-ttu-id="9f5ce-118">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="9f5ce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5ce-119">-DefaultProfile</span></span>
<span data-ttu-id="9f5ce-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f5ce-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f5ce-121">-InputObject</span></span>
<span data-ttu-id="9f5ce-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9f5ce-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="9f5ce-123">-Name</span></span>
<span data-ttu-id="9f5ce-124">Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5ce-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9f5ce-125">-NoWait</span></span>
<span data-ttu-id="9f5ce-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="9f5ce-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9f5ce-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f5ce-127">-PassThru</span></span>
<span data-ttu-id="9f5ce-128">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="9f5ce-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9f5ce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f5ce-129">-ResourceGroupName</span></span>
<span data-ttu-id="9f5ce-130">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9f5ce-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f5ce-131">-SubscriptionId</span></span>
<span data-ttu-id="9f5ce-132">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9f5ce-133">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9f5ce-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9f5ce-134">-Confirm</span></span>
<span data-ttu-id="9f5ce-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f5ce-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f5ce-136">-WhatIf</span></span>
<span data-ttu-id="9f5ce-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f5ce-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f5ce-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f5ce-139">CommonParameters</span></span>
<span data-ttu-id="9f5ce-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f5ce-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f5ce-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f5ce-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f5ce-142">INPUTS</span></span>

### <span data-ttu-id="9f5ce-143">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9f5ce-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9f5ce-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f5ce-144">OUTPUTS</span></span>

### <span data-ttu-id="9f5ce-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f5ce-145">System.Boolean</span></span>

## <span data-ttu-id="9f5ce-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f5ce-146">NOTES</span></span>

<span data-ttu-id="9f5ce-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9f5ce-147">ALIASES</span></span>

<span data-ttu-id="9f5ce-148">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="9f5ce-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9f5ce-149">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9f5ce-150">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9f5ce-151">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="9f5ce-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9f5ce-152">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9f5ce-153">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9f5ce-154">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9f5ce-155">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9f5ce-156">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="9f5ce-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9f5ce-157">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9f5ce-158">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9f5ce-159">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9f5ce-160">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9f5ce-161">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9f5ce-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9f5ce-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f5ce-162">RELATED LINKS</span></span>
