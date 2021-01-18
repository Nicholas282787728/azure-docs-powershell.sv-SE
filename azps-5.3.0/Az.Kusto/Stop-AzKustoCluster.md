---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/stop-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
ms.openlocfilehash: 1dd67a5a3557ba38267f570c77b5117466e4260b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524077"
---
# <span data-ttu-id="d0aba-101">Stop-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d0aba-101">Stop-AzKustoCluster</span></span>

## <span data-ttu-id="d0aba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0aba-102">SYNOPSIS</span></span>
<span data-ttu-id="d0aba-103">Stoppar ett Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="d0aba-103">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="d0aba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0aba-104">SYNTAX</span></span>

### <span data-ttu-id="d0aba-105">Stopp (standard)</span><span class="sxs-lookup"><span data-stu-id="d0aba-105">Stop (Default)</span></span>
```
Stop-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d0aba-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d0aba-106">StopViaIdentity</span></span>
```
Stop-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d0aba-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0aba-107">DESCRIPTION</span></span>
<span data-ttu-id="d0aba-108">Stoppar ett Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="d0aba-108">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="d0aba-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0aba-109">EXAMPLES</span></span>

### <span data-ttu-id="d0aba-110">Exempel 1: stoppa ett Kusto-kluster</span><span class="sxs-lookup"><span data-stu-id="d0aba-110">Example 1: Stop a Kusto cluster</span></span>
```powershell
PS C:\> Stop-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="d0aba-111">Kommandot ovan stoppar ett Kusto-kluster</span><span class="sxs-lookup"><span data-stu-id="d0aba-111">The above command stops a Kusto cluster</span></span>

## <span data-ttu-id="d0aba-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0aba-112">PARAMETERS</span></span>

### <span data-ttu-id="d0aba-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0aba-113">-AsJob</span></span>
<span data-ttu-id="d0aba-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="d0aba-114">Run the command as a job</span></span>

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

### <span data-ttu-id="d0aba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0aba-115">-DefaultProfile</span></span>
<span data-ttu-id="d0aba-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0aba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0aba-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0aba-117">-InputObject</span></span>
<span data-ttu-id="d0aba-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d0aba-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0aba-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0aba-119">-Name</span></span>
<span data-ttu-id="d0aba-120">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d0aba-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0aba-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d0aba-121">-NoWait</span></span>
<span data-ttu-id="d0aba-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="d0aba-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d0aba-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0aba-123">-PassThru</span></span>
<span data-ttu-id="d0aba-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="d0aba-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d0aba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0aba-125">-ResourceGroupName</span></span>
<span data-ttu-id="d0aba-126">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d0aba-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0aba-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0aba-127">-SubscriptionId</span></span>
<span data-ttu-id="d0aba-128">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d0aba-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d0aba-129">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="d0aba-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0aba-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0aba-130">-Confirm</span></span>
<span data-ttu-id="d0aba-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0aba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0aba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0aba-132">-WhatIf</span></span>
<span data-ttu-id="d0aba-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0aba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0aba-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0aba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0aba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0aba-135">CommonParameters</span></span>
<span data-ttu-id="d0aba-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0aba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0aba-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0aba-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0aba-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0aba-138">INPUTS</span></span>

### <span data-ttu-id="d0aba-139">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d0aba-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d0aba-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0aba-140">OUTPUTS</span></span>

### <span data-ttu-id="d0aba-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0aba-141">System.Boolean</span></span>

## <span data-ttu-id="d0aba-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0aba-142">NOTES</span></span>

<span data-ttu-id="d0aba-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d0aba-143">ALIASES</span></span>

<span data-ttu-id="d0aba-144">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="d0aba-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d0aba-145">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="d0aba-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d0aba-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d0aba-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d0aba-147">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="d0aba-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d0aba-148">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="d0aba-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d0aba-149">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d0aba-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d0aba-150">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="d0aba-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d0aba-151">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d0aba-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d0aba-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="d0aba-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d0aba-153">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="d0aba-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d0aba-154">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d0aba-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d0aba-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d0aba-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d0aba-156">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d0aba-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d0aba-157">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="d0aba-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d0aba-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0aba-158">RELATED LINKS</span></span>

