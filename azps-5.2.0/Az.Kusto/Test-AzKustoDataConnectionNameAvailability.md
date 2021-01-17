---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 556e0a7662a91c5c82bab7727bf676adf88d45d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417096"
---
# <span data-ttu-id="a4251-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="a4251-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="a4251-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4251-102">SYNOPSIS</span></span>
<span data-ttu-id="a4251-103">Kontrollerar att data anslutnings namnet är giltigt och inte redan används.</span><span class="sxs-lookup"><span data-stu-id="a4251-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="a4251-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4251-104">SYNTAX</span></span>

### <span data-ttu-id="a4251-105">CheckExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="a4251-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a4251-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a4251-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a4251-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4251-107">DESCRIPTION</span></span>
<span data-ttu-id="a4251-108">Kontrollerar att data anslutnings namnet är giltigt och inte redan används.</span><span class="sxs-lookup"><span data-stu-id="a4251-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="a4251-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4251-109">EXAMPLES</span></span>

### <span data-ttu-id="a4251-110">Exempel 1: kontrol lera tillgänglighet för ett data anslutnings namn som används</span><span class="sxs-lookup"><span data-stu-id="a4251-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="a4251-111">Kommandot ovan returnerar om en data anslutning med namnet "mykustodataconnection" finns i databasen "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="a4251-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="a4251-112">Exempel 2: kontrol lera tillgänglighet för ett namn för data anslutning som inte används</span><span class="sxs-lookup"><span data-stu-id="a4251-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="a4251-113">Kommandot ovan returnerar om en data anslutning med namnet "mydataconnection" finns i databasen "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="a4251-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="a4251-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4251-114">PARAMETERS</span></span>

### <span data-ttu-id="a4251-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="a4251-115">-ClusterName</span></span>
<span data-ttu-id="a4251-116">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4251-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a4251-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a4251-117">-DatabaseName</span></span>
<span data-ttu-id="a4251-118">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4251-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="a4251-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4251-119">-DefaultProfile</span></span>
<span data-ttu-id="a4251-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4251-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4251-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4251-121">-InputObject</span></span>
<span data-ttu-id="a4251-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a4251-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a4251-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4251-123">-Name</span></span>
<span data-ttu-id="a4251-124">Namn på data anslutning.</span><span class="sxs-lookup"><span data-stu-id="a4251-124">Data Connection name.</span></span>

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

### <span data-ttu-id="a4251-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4251-125">-ResourceGroupName</span></span>
<span data-ttu-id="a4251-126">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4251-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a4251-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4251-127">-SubscriptionId</span></span>
<span data-ttu-id="a4251-128">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a4251-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a4251-129">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="a4251-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a4251-130">– Skriv</span><span class="sxs-lookup"><span data-stu-id="a4251-130">-Type</span></span>
<span data-ttu-id="a4251-131">Typ av resurs, Microsoft. Kusto/kluster/databaser/dataConnections.</span><span class="sxs-lookup"><span data-stu-id="a4251-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

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

### <span data-ttu-id="a4251-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4251-132">-Confirm</span></span>
<span data-ttu-id="a4251-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4251-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4251-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4251-134">-WhatIf</span></span>
<span data-ttu-id="a4251-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4251-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4251-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4251-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4251-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4251-137">CommonParameters</span></span>
<span data-ttu-id="a4251-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4251-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4251-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4251-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4251-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4251-140">INPUTS</span></span>

### <span data-ttu-id="a4251-141">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a4251-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a4251-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4251-142">OUTPUTS</span></span>

### <span data-ttu-id="a4251-143">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="a4251-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="a4251-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4251-144">NOTES</span></span>

<span data-ttu-id="a4251-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a4251-145">ALIASES</span></span>

<span data-ttu-id="a4251-146">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="a4251-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4251-147">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="a4251-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4251-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a4251-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4251-149">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="a4251-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4251-150">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="a4251-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a4251-151">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4251-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a4251-152">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="a4251-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a4251-153">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4251-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a4251-154">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="a4251-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4251-155">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="a4251-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a4251-156">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a4251-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a4251-157">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="a4251-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a4251-158">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a4251-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a4251-159">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="a4251-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a4251-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4251-160">RELATED LINKS</span></span>

