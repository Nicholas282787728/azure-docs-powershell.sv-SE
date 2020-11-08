---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 0a6643a4909bb2125e419e28fe3d7a8494760d8d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103198"
---
# <span data-ttu-id="2eea7-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="2eea7-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="2eea7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2eea7-102">SYNOPSIS</span></span>
<span data-ttu-id="2eea7-103">Hämtar ett Kusto kluster-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="2eea7-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="2eea7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2eea7-104">SYNTAX</span></span>

### <span data-ttu-id="2eea7-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="2eea7-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2eea7-106">Lära</span><span class="sxs-lookup"><span data-stu-id="2eea7-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2eea7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2eea7-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2eea7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2eea7-108">DESCRIPTION</span></span>
<span data-ttu-id="2eea7-109">Hämtar ett Kusto kluster-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="2eea7-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="2eea7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2eea7-110">EXAMPLES</span></span>

### <span data-ttu-id="2eea7-111">Exempel 1: lista alla Kusto-principalAssignment</span><span class="sxs-lookup"><span data-stu-id="2eea7-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="2eea7-112">Kommandot ovan visar alla principalAssignment i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="2eea7-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2eea7-113">Exempel 2: hämtar ett Kusto kluster principalAssignment efter namn</span><span class="sxs-lookup"><span data-stu-id="2eea7-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="2eea7-114">Kommandot ovan returnerar Kusto kluster principalAssignment med namnet "kustoprincipal1" i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="2eea7-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="2eea7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2eea7-115">PARAMETERS</span></span>

### <span data-ttu-id="2eea7-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="2eea7-116">-ClusterName</span></span>
<span data-ttu-id="2eea7-117">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="2eea7-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="2eea7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eea7-118">-DefaultProfile</span></span>
<span data-ttu-id="2eea7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2eea7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eea7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eea7-120">-InputObject</span></span>
<span data-ttu-id="2eea7-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="2eea7-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2eea7-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="2eea7-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="2eea7-123">Namnet på Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="2eea7-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="2eea7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eea7-124">-ResourceGroupName</span></span>
<span data-ttu-id="2eea7-125">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="2eea7-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="2eea7-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2eea7-126">-SubscriptionId</span></span>
<span data-ttu-id="2eea7-127">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2eea7-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2eea7-128">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="2eea7-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2eea7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eea7-129">CommonParameters</span></span>
<span data-ttu-id="2eea7-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eea7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eea7-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2eea7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eea7-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2eea7-132">INPUTS</span></span>

### <span data-ttu-id="2eea7-133">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="2eea7-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2eea7-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2eea7-134">OUTPUTS</span></span>

### <span data-ttu-id="2eea7-135">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="2eea7-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="2eea7-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2eea7-136">NOTES</span></span>

<span data-ttu-id="2eea7-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2eea7-137">ALIASES</span></span>

<span data-ttu-id="2eea7-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="2eea7-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2eea7-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="2eea7-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2eea7-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2eea7-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2eea7-141">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="2eea7-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2eea7-142">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="2eea7-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2eea7-143">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="2eea7-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2eea7-144">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="2eea7-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2eea7-145">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="2eea7-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2eea7-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="2eea7-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2eea7-147">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="2eea7-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2eea7-148">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="2eea7-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2eea7-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="2eea7-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2eea7-150">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2eea7-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2eea7-151">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="2eea7-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2eea7-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2eea7-152">RELATED LINKS</span></span>

