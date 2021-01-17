---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: fd735b1d343c046f9ca2f0528bff4bf7ce8a403d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411688"
---
# <span data-ttu-id="45dad-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="45dad-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="45dad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45dad-102">SYNOPSIS</span></span>
<span data-ttu-id="45dad-103">Returnerar en ansluten databas konfiguration.</span><span class="sxs-lookup"><span data-stu-id="45dad-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="45dad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45dad-104">SYNTAX</span></span>

### <span data-ttu-id="45dad-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="45dad-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="45dad-106">Lära</span><span class="sxs-lookup"><span data-stu-id="45dad-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="45dad-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="45dad-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="45dad-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45dad-108">DESCRIPTION</span></span>
<span data-ttu-id="45dad-109">Returnerar en ansluten databas konfiguration.</span><span class="sxs-lookup"><span data-stu-id="45dad-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="45dad-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45dad-110">EXAMPLES</span></span>

### <span data-ttu-id="45dad-111">Exempel 1: lista alla AttachedDatabaseConfigurations i ett kluster</span><span class="sxs-lookup"><span data-stu-id="45dad-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="45dad-112">Kommandot ovan visar alla AttachedDatabaseConfigurations i klustret "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="45dad-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="45dad-113">Exempel 2: skaffa en specifik AttachedDatabaseConfiguration i ett kluster</span><span class="sxs-lookup"><span data-stu-id="45dad-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="45dad-114">Kommandot ovan returnerar AttachedDatabaseConfigurations med namnet "myfollowerconfiguration" i klustret "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="45dad-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="45dad-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45dad-115">PARAMETERS</span></span>

### <span data-ttu-id="45dad-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="45dad-116">-ClusterName</span></span>
<span data-ttu-id="45dad-117">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="45dad-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="45dad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45dad-118">-DefaultProfile</span></span>
<span data-ttu-id="45dad-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45dad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45dad-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45dad-120">-InputObject</span></span>
<span data-ttu-id="45dad-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="45dad-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="45dad-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="45dad-122">-Name</span></span>
<span data-ttu-id="45dad-123">Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="45dad-123">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45dad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45dad-124">-ResourceGroupName</span></span>
<span data-ttu-id="45dad-125">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="45dad-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="45dad-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45dad-126">-SubscriptionId</span></span>
<span data-ttu-id="45dad-127">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="45dad-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="45dad-128">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="45dad-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="45dad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45dad-129">CommonParameters</span></span>
<span data-ttu-id="45dad-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45dad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45dad-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45dad-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45dad-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45dad-132">INPUTS</span></span>

### <span data-ttu-id="45dad-133">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="45dad-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="45dad-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45dad-134">OUTPUTS</span></span>

### <span data-ttu-id="45dad-135">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="45dad-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="45dad-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45dad-136">NOTES</span></span>

<span data-ttu-id="45dad-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="45dad-137">ALIASES</span></span>

<span data-ttu-id="45dad-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="45dad-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="45dad-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="45dad-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45dad-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45dad-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="45dad-141">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="45dad-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45dad-142">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="45dad-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="45dad-143">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="45dad-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="45dad-144">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="45dad-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="45dad-145">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="45dad-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="45dad-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="45dad-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45dad-147">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="45dad-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="45dad-148">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="45dad-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="45dad-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="45dad-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="45dad-150">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="45dad-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="45dad-151">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="45dad-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="45dad-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45dad-152">RELATED LINKS</span></span>

