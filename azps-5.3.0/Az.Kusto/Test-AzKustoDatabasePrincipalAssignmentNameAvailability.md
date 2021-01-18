---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: b4a670046403aafb4b40740c34f27d7c81bcf8e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524068"
---
# <span data-ttu-id="80172-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="80172-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="80172-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80172-102">SYNOPSIS</span></span>
<span data-ttu-id="80172-103">Kontrollerar att tilldelningen av databasens huvud objekt är giltig och att den inte redan används.</span><span class="sxs-lookup"><span data-stu-id="80172-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="80172-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80172-104">SYNTAX</span></span>

### <span data-ttu-id="80172-105">CheckExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="80172-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="80172-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="80172-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80172-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80172-107">DESCRIPTION</span></span>
<span data-ttu-id="80172-108">Kontrollerar att tilldelningen av databasens huvud objekt är giltig och att den inte redan används.</span><span class="sxs-lookup"><span data-stu-id="80172-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="80172-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80172-109">EXAMPLES</span></span>

### <span data-ttu-id="80172-110">Exempel 1: kontrol lera tillgänglighet för ett databas principalassignment namn som används</span><span class="sxs-lookup"><span data-stu-id="80172-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="80172-111">Kommandot ovan returnerar om en PrincipalAssignment med namnet "UPN" finns i databasen "mykustodatabase" från kluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="80172-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="80172-112">Exempel 2: kontrol lera tillgänglighet för ett databas principalassignment namn som inte används</span><span class="sxs-lookup"><span data-stu-id="80172-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="80172-113">Kommandot ovan returnerar om en PrincipalAssignment med namnet "UPN" finns i databasen "mykustodatabase" från kluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="80172-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="80172-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80172-114">PARAMETERS</span></span>

### <span data-ttu-id="80172-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="80172-115">-ClusterName</span></span>
<span data-ttu-id="80172-116">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="80172-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="80172-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="80172-117">-DatabaseName</span></span>
<span data-ttu-id="80172-118">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="80172-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="80172-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80172-119">-DefaultProfile</span></span>
<span data-ttu-id="80172-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80172-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80172-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80172-121">-InputObject</span></span>
<span data-ttu-id="80172-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="80172-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="80172-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="80172-123">-Name</span></span>
<span data-ttu-id="80172-124">Resurs namn för huvud tilldelning.</span><span class="sxs-lookup"><span data-stu-id="80172-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="80172-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80172-125">-ResourceGroupName</span></span>
<span data-ttu-id="80172-126">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="80172-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="80172-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80172-127">-SubscriptionId</span></span>
<span data-ttu-id="80172-128">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="80172-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="80172-129">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="80172-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="80172-130">– Skriv</span><span class="sxs-lookup"><span data-stu-id="80172-130">-Type</span></span>
<span data-ttu-id="80172-131">Typ av resurs, Microsoft. Kusto/kluster/databaser/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="80172-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="80172-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="80172-132">-Confirm</span></span>
<span data-ttu-id="80172-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="80172-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80172-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80172-134">-WhatIf</span></span>
<span data-ttu-id="80172-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="80172-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80172-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="80172-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80172-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80172-137">CommonParameters</span></span>
<span data-ttu-id="80172-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80172-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80172-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80172-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80172-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80172-140">INPUTS</span></span>

### <span data-ttu-id="80172-141">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="80172-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="80172-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80172-142">OUTPUTS</span></span>

### <span data-ttu-id="80172-143">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200918. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="80172-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="80172-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80172-144">NOTES</span></span>

<span data-ttu-id="80172-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="80172-145">ALIASES</span></span>

<span data-ttu-id="80172-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="80172-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80172-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="80172-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80172-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80172-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80172-149">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="80172-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80172-150">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="80172-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="80172-151">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="80172-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="80172-152">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="80172-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="80172-153">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="80172-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="80172-154">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="80172-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80172-155">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="80172-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="80172-156">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="80172-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="80172-157">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="80172-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="80172-158">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="80172-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="80172-159">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="80172-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="80172-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80172-160">RELATED LINKS</span></span>

