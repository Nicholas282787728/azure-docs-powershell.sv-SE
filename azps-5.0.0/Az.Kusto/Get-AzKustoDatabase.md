---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: cdcba65473974da6ba8d526247ca947daa97a55c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272243"
---
# <span data-ttu-id="dbf6b-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="dbf6b-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="dbf6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbf6b-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf6b-103">Returnerar en databas.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-103">Returns a database.</span></span>

## <span data-ttu-id="dbf6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbf6b-104">SYNTAX</span></span>

### <span data-ttu-id="dbf6b-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="dbf6b-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dbf6b-106">Lära</span><span class="sxs-lookup"><span data-stu-id="dbf6b-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dbf6b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dbf6b-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dbf6b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbf6b-108">DESCRIPTION</span></span>
<span data-ttu-id="dbf6b-109">Returnerar en databas.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-109">Returns a database.</span></span>

## <span data-ttu-id="dbf6b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbf6b-110">EXAMPLES</span></span>

### <span data-ttu-id="dbf6b-111">Exempel 1: lista alla Kusto-databaser i ett kluster med namn</span><span class="sxs-lookup"><span data-stu-id="dbf6b-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="dbf6b-112">Kommandot ovan returnerar alla Kusto-databaser i klustret "testnewkustocluster" som finns i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="dbf6b-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="dbf6b-113">Exempel 2: Hämta en specifik Kusto-databas med namn</span><span class="sxs-lookup"><span data-stu-id="dbf6b-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="dbf6b-114">Kommandot ovan returnerar Kusto-databasen med namnet "mykustodatabase" i klustret "testnewkustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="dbf6b-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="dbf6b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbf6b-115">PARAMETERS</span></span>

### <span data-ttu-id="dbf6b-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="dbf6b-116">-ClusterName</span></span>
<span data-ttu-id="dbf6b-117">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="dbf6b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf6b-118">-DefaultProfile</span></span>
<span data-ttu-id="dbf6b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbf6b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbf6b-120">-InputObject</span></span>
<span data-ttu-id="dbf6b-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dbf6b-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="dbf6b-122">-Name</span></span>
<span data-ttu-id="dbf6b-123">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-123">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf6b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf6b-124">-ResourceGroupName</span></span>
<span data-ttu-id="dbf6b-125">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="dbf6b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dbf6b-126">-SubscriptionId</span></span>
<span data-ttu-id="dbf6b-127">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dbf6b-128">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dbf6b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf6b-129">CommonParameters</span></span>
<span data-ttu-id="dbf6b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf6b-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbf6b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf6b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbf6b-132">INPUTS</span></span>

### <span data-ttu-id="dbf6b-133">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="dbf6b-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="dbf6b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbf6b-134">OUTPUTS</span></span>

### <span data-ttu-id="dbf6b-135">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="dbf6b-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="dbf6b-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbf6b-136">NOTES</span></span>

<span data-ttu-id="dbf6b-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dbf6b-137">ALIASES</span></span>

<span data-ttu-id="dbf6b-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="dbf6b-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dbf6b-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dbf6b-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dbf6b-141">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="dbf6b-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dbf6b-142">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="dbf6b-143">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="dbf6b-144">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="dbf6b-145">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="dbf6b-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="dbf6b-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dbf6b-147">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="dbf6b-148">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="dbf6b-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="dbf6b-150">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dbf6b-151">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="dbf6b-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dbf6b-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbf6b-152">RELATED LINKS</span></span>

