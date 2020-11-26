---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 4becbb8285685c923fe6b0ec2174e7e84824a106
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102811"
---
# <span data-ttu-id="212a9-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="212a9-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="212a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="212a9-102">SYNOPSIS</span></span>
<span data-ttu-id="212a9-103">Hämtar en Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="212a9-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="212a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="212a9-104">SYNTAX</span></span>

### <span data-ttu-id="212a9-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="212a9-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="212a9-106">Lära</span><span class="sxs-lookup"><span data-stu-id="212a9-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="212a9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="212a9-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="212a9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="212a9-108">DESCRIPTION</span></span>
<span data-ttu-id="212a9-109">Hämtar en Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="212a9-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="212a9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="212a9-110">EXAMPLES</span></span>

### <span data-ttu-id="212a9-111">Exempel 1: lista alla PrincipalAssignment i en databas efter namn</span><span class="sxs-lookup"><span data-stu-id="212a9-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="212a9-112">Kommandot ovan returnerar alla PrincipalAssignment i databasen "mykustodatabase" som finns i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="212a9-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="212a9-113">Exempel 2: Hämta en specifik PrincipalAssignment i en databas efter namn</span><span class="sxs-lookup"><span data-stu-id="212a9-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="212a9-114">Kommandot ovan returnerar alla PrincipalAssignment med namnet "kustoprincipal1" i databasen "mykustodatabase" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="212a9-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="212a9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="212a9-115">PARAMETERS</span></span>

### <span data-ttu-id="212a9-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="212a9-116">-ClusterName</span></span>
<span data-ttu-id="212a9-117">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="212a9-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="212a9-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="212a9-118">-DatabaseName</span></span>
<span data-ttu-id="212a9-119">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="212a9-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="212a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="212a9-120">-DefaultProfile</span></span>
<span data-ttu-id="212a9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="212a9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="212a9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="212a9-122">-InputObject</span></span>
<span data-ttu-id="212a9-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="212a9-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="212a9-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="212a9-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="212a9-125">Namnet på Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="212a9-125">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212a9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="212a9-126">-ResourceGroupName</span></span>
<span data-ttu-id="212a9-127">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="212a9-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="212a9-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="212a9-128">-SubscriptionId</span></span>
<span data-ttu-id="212a9-129">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="212a9-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="212a9-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="212a9-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="212a9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="212a9-131">CommonParameters</span></span>
<span data-ttu-id="212a9-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="212a9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="212a9-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="212a9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="212a9-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="212a9-134">INPUTS</span></span>

### <span data-ttu-id="212a9-135">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="212a9-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="212a9-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="212a9-136">OUTPUTS</span></span>

### <span data-ttu-id="212a9-137">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="212a9-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="212a9-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="212a9-138">NOTES</span></span>

<span data-ttu-id="212a9-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="212a9-139">ALIASES</span></span>

<span data-ttu-id="212a9-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="212a9-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="212a9-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="212a9-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="212a9-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="212a9-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="212a9-143">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="212a9-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="212a9-144">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="212a9-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="212a9-145">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="212a9-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="212a9-146">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="212a9-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="212a9-147">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="212a9-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="212a9-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="212a9-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="212a9-149">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="212a9-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="212a9-150">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="212a9-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="212a9-151">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="212a9-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="212a9-152">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="212a9-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="212a9-153">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="212a9-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="212a9-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="212a9-154">RELATED LINKS</span></span>
