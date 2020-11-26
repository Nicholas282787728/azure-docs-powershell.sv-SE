---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: 6cfc5cdae87512245a573ed5c7ff9c746036c815
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272244"
---
# <span data-ttu-id="27ea7-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="27ea7-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="27ea7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="27ea7-103">Returnerar en data anslutning.</span><span class="sxs-lookup"><span data-stu-id="27ea7-103">Returns a data connection.</span></span>

## <span data-ttu-id="27ea7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27ea7-104">SYNTAX</span></span>

### <span data-ttu-id="27ea7-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="27ea7-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="27ea7-106">Lära</span><span class="sxs-lookup"><span data-stu-id="27ea7-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="27ea7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="27ea7-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="27ea7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27ea7-108">DESCRIPTION</span></span>
<span data-ttu-id="27ea7-109">Returnerar en data anslutning.</span><span class="sxs-lookup"><span data-stu-id="27ea7-109">Returns a data connection.</span></span>

## <span data-ttu-id="27ea7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27ea7-110">EXAMPLES</span></span>

### <span data-ttu-id="27ea7-111">Exempel 1: lista alla data anslutningar i en viss databas</span><span class="sxs-lookup"><span data-stu-id="27ea7-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="27ea7-112">Kommandot ovan returnerar alla Kusto-databaser i klustret "testnewkustocluster" som finns i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="27ea7-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="27ea7-113">Exempel 2: Hämta en specifik data anslutning utifrån namn</span><span class="sxs-lookup"><span data-stu-id="27ea7-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="27ea7-114">Kommandot ovan returnerar data anslutningen "mykustodataconnection" i databasen "mykustodatabase" för det befintliga klustret "testnewkustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="27ea7-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="27ea7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27ea7-115">PARAMETERS</span></span>

### <span data-ttu-id="27ea7-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="27ea7-116">-ClusterName</span></span>
<span data-ttu-id="27ea7-117">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="27ea7-117">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea7-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="27ea7-118">-DatabaseName</span></span>
<span data-ttu-id="27ea7-119">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="27ea7-119">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ea7-120">-DefaultProfile</span></span>
<span data-ttu-id="27ea7-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27ea7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27ea7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27ea7-122">-InputObject</span></span>
<span data-ttu-id="27ea7-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="27ea7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27ea7-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="27ea7-124">-Name</span></span>
<span data-ttu-id="27ea7-125">Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="27ea7-125">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ea7-126">-ResourceGroupName</span></span>
<span data-ttu-id="27ea7-127">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="27ea7-127">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea7-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27ea7-128">-SubscriptionId</span></span>
<span data-ttu-id="27ea7-129">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="27ea7-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="27ea7-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="27ea7-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ea7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ea7-131">CommonParameters</span></span>
<span data-ttu-id="27ea7-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27ea7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ea7-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27ea7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ea7-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27ea7-134">INPUTS</span></span>

### <span data-ttu-id="27ea7-135">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="27ea7-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="27ea7-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27ea7-136">OUTPUTS</span></span>

### <span data-ttu-id="27ea7-137">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="27ea7-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="27ea7-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27ea7-138">NOTES</span></span>

<span data-ttu-id="27ea7-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="27ea7-139">ALIASES</span></span>

<span data-ttu-id="27ea7-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="27ea7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="27ea7-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="27ea7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="27ea7-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="27ea7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="27ea7-143">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="27ea7-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="27ea7-144">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="27ea7-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="27ea7-145">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="27ea7-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="27ea7-146">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="27ea7-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="27ea7-147">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="27ea7-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="27ea7-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="27ea7-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="27ea7-149">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="27ea7-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="27ea7-150">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="27ea7-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="27ea7-151">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="27ea7-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="27ea7-152">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="27ea7-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="27ea7-153">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="27ea7-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="27ea7-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27ea7-154">RELATED LINKS</span></span>
