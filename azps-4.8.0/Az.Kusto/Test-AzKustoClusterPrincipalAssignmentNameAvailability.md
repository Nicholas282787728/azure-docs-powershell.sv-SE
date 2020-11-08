---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: cb4f375632626ee3c3428e6a990a228dacecd288
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262220"
---
# <span data-ttu-id="9e3a6-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9e3a6-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="9e3a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3a6-103">Kontrollerar att huvud tilldelningens namn är giltigt och inte redan används.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="9e3a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e3a6-104">SYNTAX</span></span>

### <span data-ttu-id="9e3a6-105">CheckExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="9e3a6-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9e3a6-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9e3a6-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9e3a6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e3a6-107">DESCRIPTION</span></span>
<span data-ttu-id="9e3a6-108">Kontrollerar att huvud tilldelningens namn är giltigt och inte redan används.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="9e3a6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e3a6-109">EXAMPLES</span></span>

### <span data-ttu-id="9e3a6-110">Exempel 1: kontrol lera tillgänglighet för ett kluster principalassignment namn som används</span><span class="sxs-lookup"><span data-stu-id="9e3a6-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="9e3a6-111">Kommandot ovan returnerar om en PrincipalAssignment med namnet "UPN" finns i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="9e3a6-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="9e3a6-112">Exempel 2: kontrol lera tillgänglighet för ett kluster principalassignment namn som inte används</span><span class="sxs-lookup"><span data-stu-id="9e3a6-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="9e3a6-113">Kommandot ovan returnerar om en PrincipalAssignment med namnet "NewPrincipal" finns i klustret "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="9e3a6-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="9e3a6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e3a6-114">PARAMETERS</span></span>

### <span data-ttu-id="9e3a6-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="9e3a6-115">-ClusterName</span></span>
<span data-ttu-id="9e3a6-116">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="9e3a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3a6-117">-DefaultProfile</span></span>
<span data-ttu-id="9e3a6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e3a6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e3a6-119">-InputObject</span></span>
<span data-ttu-id="9e3a6-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9e3a6-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9e3a6-121">-Name</span></span>
<span data-ttu-id="9e3a6-122">Resurs namn för huvud tilldelning.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="9e3a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e3a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="9e3a6-124">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9e3a6-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e3a6-125">-SubscriptionId</span></span>
<span data-ttu-id="9e3a6-126">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9e3a6-127">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9e3a6-128">– Skriv</span><span class="sxs-lookup"><span data-stu-id="9e3a6-128">-Type</span></span>
<span data-ttu-id="9e3a6-129">Typ av resurs, Microsoft. Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="9e3a6-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e3a6-130">-Confirm</span></span>
<span data-ttu-id="9e3a6-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e3a6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e3a6-132">-WhatIf</span></span>
<span data-ttu-id="9e3a6-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e3a6-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e3a6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3a6-135">CommonParameters</span></span>
<span data-ttu-id="9e3a6-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3a6-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e3a6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3a6-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e3a6-138">INPUTS</span></span>

### <span data-ttu-id="9e3a6-139">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9e3a6-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9e3a6-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e3a6-140">OUTPUTS</span></span>

### <span data-ttu-id="9e3a6-141">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="9e3a6-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="9e3a6-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e3a6-142">NOTES</span></span>

<span data-ttu-id="9e3a6-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9e3a6-143">ALIASES</span></span>

<span data-ttu-id="9e3a6-144">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="9e3a6-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9e3a6-145">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e3a6-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9e3a6-147">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="9e3a6-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e3a6-148">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9e3a6-149">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9e3a6-150">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9e3a6-151">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9e3a6-152">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="9e3a6-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e3a6-153">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9e3a6-154">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9e3a6-155">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9e3a6-156">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9e3a6-157">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="9e3a6-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9e3a6-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e3a6-158">RELATED LINKS</span></span>

