---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: ab15d7a9da10e7e7a024d3af332f449cd011a290
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102810"
---
# <span data-ttu-id="e3d2a-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="e3d2a-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="e3d2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d2a-103">Kontrollerar att databasens namn är giltigt och att det inte redan används.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="e3d2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3d2a-104">SYNTAX</span></span>

### <span data-ttu-id="e3d2a-105">CheckExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="e3d2a-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e3d2a-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e3d2a-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e3d2a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3d2a-107">DESCRIPTION</span></span>
<span data-ttu-id="e3d2a-108">Kontrollerar att databasens namn är giltigt och att det inte redan används.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="e3d2a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3d2a-109">EXAMPLES</span></span>

### <span data-ttu-id="e3d2a-110">Exempel 1: kontrol lera tillgänglighet för ett Kusto databas namn som används</span><span class="sxs-lookup"><span data-stu-id="e3d2a-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="e3d2a-111">Kommandot ovan returnerar om en Kusto-databas med namnet "mykustodatabase" finns i "testnewkustocluster"-klustret.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="e3d2a-112">Exempel 2: kontrol lera tillgänglighet för ett Kusto-databas namn som inte används</span><span class="sxs-lookup"><span data-stu-id="e3d2a-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="e3d2a-113">Kommandot ovan returnerar om en Kusto-databas med namnet "mykustodatabase2" finns i "testnewkustocluster"-klustret.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="e3d2a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3d2a-114">PARAMETERS</span></span>

### <span data-ttu-id="e3d2a-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="e3d2a-115">-ClusterName</span></span>
<span data-ttu-id="e3d2a-116">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e3d2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d2a-117">-DefaultProfile</span></span>
<span data-ttu-id="e3d2a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3d2a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3d2a-119">-InputObject</span></span>
<span data-ttu-id="e3d2a-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e3d2a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3d2a-121">-Name</span></span>
<span data-ttu-id="e3d2a-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-122">Resource name.</span></span>

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

### <span data-ttu-id="e3d2a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3d2a-123">-ResourceGroupName</span></span>
<span data-ttu-id="e3d2a-124">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e3d2a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3d2a-125">-SubscriptionId</span></span>
<span data-ttu-id="e3d2a-126">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e3d2a-127">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e3d2a-128">– Skriv</span><span class="sxs-lookup"><span data-stu-id="e3d2a-128">-Type</span></span>
<span data-ttu-id="e3d2a-129">Typ av resurs, till exempel Microsoft. Kusto/kluster/databaser.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

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

### <span data-ttu-id="e3d2a-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3d2a-130">-Confirm</span></span>
<span data-ttu-id="e3d2a-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3d2a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3d2a-132">-WhatIf</span></span>
<span data-ttu-id="e3d2a-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3d2a-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3d2a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d2a-135">CommonParameters</span></span>
<span data-ttu-id="e3d2a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d2a-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3d2a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d2a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3d2a-138">INPUTS</span></span>

### <span data-ttu-id="e3d2a-139">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e3d2a-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e3d2a-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3d2a-140">OUTPUTS</span></span>

### <span data-ttu-id="e3d2a-141">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="e3d2a-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="e3d2a-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3d2a-142">NOTES</span></span>

<span data-ttu-id="e3d2a-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e3d2a-143">ALIASES</span></span>

<span data-ttu-id="e3d2a-144">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="e3d2a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3d2a-145">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3d2a-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3d2a-147">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e3d2a-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3d2a-148">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e3d2a-149">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e3d2a-150">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e3d2a-151">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e3d2a-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e3d2a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3d2a-153">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e3d2a-154">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e3d2a-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e3d2a-156">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e3d2a-157">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e3d2a-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e3d2a-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3d2a-158">RELATED LINKS</span></span>

