---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: 01f22e069e1e5d664ceac5c6cef7698cf9ffa980
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524069"
---
# <span data-ttu-id="0bae5-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="0bae5-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="0bae5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0bae5-102">SYNOPSIS</span></span>
<span data-ttu-id="0bae5-103">Kontrollerar att databasens namn är giltigt och att det inte redan används.</span><span class="sxs-lookup"><span data-stu-id="0bae5-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="0bae5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0bae5-104">SYNTAX</span></span>

### <span data-ttu-id="0bae5-105">CheckExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="0bae5-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0bae5-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0bae5-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0bae5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0bae5-107">DESCRIPTION</span></span>
<span data-ttu-id="0bae5-108">Kontrollerar att databasens namn är giltigt och att det inte redan används.</span><span class="sxs-lookup"><span data-stu-id="0bae5-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="0bae5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0bae5-109">EXAMPLES</span></span>

### <span data-ttu-id="0bae5-110">Exempel 1: kontrol lera tillgänglighet för ett Kusto databas namn som används</span><span class="sxs-lookup"><span data-stu-id="0bae5-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="0bae5-111">Kommandot ovan returnerar om en Kusto-databas med namnet "mykustodatabase" finns i "testnewkustocluster"-klustret.</span><span class="sxs-lookup"><span data-stu-id="0bae5-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="0bae5-112">Exempel 2: kontrol lera tillgänglighet för ett Kusto-databas namn som inte används</span><span class="sxs-lookup"><span data-stu-id="0bae5-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="0bae5-113">Kommandot ovan returnerar om en Kusto-databas med namnet "mykustodatabase2" finns i "testnewkustocluster"-klustret.</span><span class="sxs-lookup"><span data-stu-id="0bae5-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="0bae5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0bae5-114">PARAMETERS</span></span>

### <span data-ttu-id="0bae5-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="0bae5-115">-ClusterName</span></span>
<span data-ttu-id="0bae5-116">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0bae5-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bae5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bae5-117">-DefaultProfile</span></span>
<span data-ttu-id="0bae5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0bae5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bae5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bae5-119">-InputObject</span></span>
<span data-ttu-id="0bae5-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0bae5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bae5-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="0bae5-121">-Name</span></span>
<span data-ttu-id="0bae5-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0bae5-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bae5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bae5-123">-ResourceGroupName</span></span>
<span data-ttu-id="0bae5-124">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0bae5-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bae5-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0bae5-125">-SubscriptionId</span></span>
<span data-ttu-id="0bae5-126">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0bae5-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0bae5-127">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0bae5-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bae5-128">– Skriv</span><span class="sxs-lookup"><span data-stu-id="0bae5-128">-Type</span></span>
<span data-ttu-id="0bae5-129">Typ av resurs, till exempel Microsoft. Kusto/kluster/databaser.</span><span class="sxs-lookup"><span data-stu-id="0bae5-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bae5-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0bae5-130">-Confirm</span></span>
<span data-ttu-id="0bae5-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0bae5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bae5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bae5-132">-WhatIf</span></span>
<span data-ttu-id="0bae5-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0bae5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bae5-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0bae5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bae5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bae5-135">CommonParameters</span></span>
<span data-ttu-id="0bae5-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bae5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bae5-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bae5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bae5-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0bae5-138">INPUTS</span></span>

### <span data-ttu-id="0bae5-139">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0bae5-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0bae5-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0bae5-140">OUTPUTS</span></span>

### <span data-ttu-id="0bae5-141">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200918. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="0bae5-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="0bae5-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0bae5-142">NOTES</span></span>

<span data-ttu-id="0bae5-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0bae5-143">ALIASES</span></span>

<span data-ttu-id="0bae5-144">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0bae5-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0bae5-145">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0bae5-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0bae5-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0bae5-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0bae5-147">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="0bae5-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0bae5-148">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="0bae5-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0bae5-149">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0bae5-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0bae5-150">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="0bae5-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0bae5-151">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0bae5-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0bae5-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="0bae5-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0bae5-153">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="0bae5-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0bae5-154">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0bae5-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0bae5-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="0bae5-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0bae5-156">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0bae5-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0bae5-157">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="0bae5-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0bae5-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0bae5-158">RELATED LINKS</span></span>

