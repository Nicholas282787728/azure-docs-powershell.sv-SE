---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a95f8a00578ccf917a55cdfd9685dedf9a20734f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272252"
---
# <span data-ttu-id="0323d-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="0323d-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="0323d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0323d-102">SYNOPSIS</span></span>
<span data-ttu-id="0323d-103">Får ett Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="0323d-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="0323d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0323d-104">SYNTAX</span></span>

### <span data-ttu-id="0323d-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="0323d-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0323d-106">Lära</span><span class="sxs-lookup"><span data-stu-id="0323d-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0323d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0323d-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0323d-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="0323d-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0323d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0323d-109">DESCRIPTION</span></span>
<span data-ttu-id="0323d-110">Får ett Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="0323d-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="0323d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0323d-111">EXAMPLES</span></span>

### <span data-ttu-id="0323d-112">Exempel 1: lista alla Kusto-kluster i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="0323d-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="0323d-113">Kommandot ovan visar alla Kusto-kluster i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="0323d-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="0323d-114">Exempel 2: skaffa ett specifikt Kusto-kluster med namn</span><span class="sxs-lookup"><span data-stu-id="0323d-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="0323d-115">Kommandot ovan returnerar Kusto-klustret med namnet "testnewkustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="0323d-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="0323d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0323d-116">PARAMETERS</span></span>

### <span data-ttu-id="0323d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0323d-117">-DefaultProfile</span></span>
<span data-ttu-id="0323d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0323d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0323d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0323d-119">-InputObject</span></span>
<span data-ttu-id="0323d-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0323d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0323d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0323d-121">-Name</span></span>
<span data-ttu-id="0323d-122">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0323d-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0323d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0323d-123">-ResourceGroupName</span></span>
<span data-ttu-id="0323d-124">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0323d-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0323d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0323d-125">-SubscriptionId</span></span>
<span data-ttu-id="0323d-126">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0323d-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0323d-127">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0323d-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0323d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0323d-128">CommonParameters</span></span>
<span data-ttu-id="0323d-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0323d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0323d-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0323d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0323d-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0323d-131">INPUTS</span></span>

### <span data-ttu-id="0323d-132">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0323d-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0323d-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0323d-133">OUTPUTS</span></span>

### <span data-ttu-id="0323d-134">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="0323d-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="0323d-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0323d-135">NOTES</span></span>

<span data-ttu-id="0323d-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0323d-136">ALIASES</span></span>

<span data-ttu-id="0323d-137">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0323d-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0323d-138">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0323d-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0323d-139">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0323d-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0323d-140">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0323d-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0323d-141">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="0323d-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0323d-142">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0323d-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0323d-143">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="0323d-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0323d-144">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0323d-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0323d-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0323d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0323d-146">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="0323d-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0323d-147">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0323d-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0323d-148">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0323d-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0323d-149">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0323d-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0323d-150">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0323d-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0323d-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0323d-151">RELATED LINKS</span></span>
