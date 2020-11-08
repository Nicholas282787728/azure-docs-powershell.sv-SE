---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: 15c052eedb0174b71581a390610274e10379035a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259577"
---
# <span data-ttu-id="7117b-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="7117b-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="7117b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7117b-102">SYNOPSIS</span></span>
<span data-ttu-id="7117b-103">Kontrollerar att kluster namnet är giltigt och inte redan används.</span><span class="sxs-lookup"><span data-stu-id="7117b-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="7117b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7117b-104">SYNTAX</span></span>

### <span data-ttu-id="7117b-105">CheckExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="7117b-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7117b-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7117b-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7117b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7117b-107">DESCRIPTION</span></span>
<span data-ttu-id="7117b-108">Kontrollerar att kluster namnet är giltigt och inte redan används.</span><span class="sxs-lookup"><span data-stu-id="7117b-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="7117b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7117b-109">EXAMPLES</span></span>

### <span data-ttu-id="7117b-110">Exempel 1: kontrol lera tillgänglighet för ett Kusto kluster namn som används</span><span class="sxs-lookup"><span data-stu-id="7117b-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="7117b-111">Kommandot ovan returnerar om ett Kusto-kluster med namnet "testnewkustocluster" finns i regionen "östra USA".</span><span class="sxs-lookup"><span data-stu-id="7117b-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="7117b-112">Exempel 2: kontrol lera tillgänglighet för ett Kusto kluster namn som inte används</span><span class="sxs-lookup"><span data-stu-id="7117b-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="7117b-113">Kommandot ovan returnerar om ett Kusto-kluster med namnet "availablekustocluster" finns i regionen "östra USA".</span><span class="sxs-lookup"><span data-stu-id="7117b-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="7117b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7117b-114">PARAMETERS</span></span>

### <span data-ttu-id="7117b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7117b-115">-DefaultProfile</span></span>
<span data-ttu-id="7117b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7117b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7117b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7117b-117">-InputObject</span></span>
<span data-ttu-id="7117b-118">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7117b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7117b-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="7117b-119">-Location</span></span>
<span data-ttu-id="7117b-120">Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="7117b-120">Azure location.</span></span>

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

### <span data-ttu-id="7117b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="7117b-121">-Name</span></span>
<span data-ttu-id="7117b-122">Kluster namn.</span><span class="sxs-lookup"><span data-stu-id="7117b-122">Cluster name.</span></span>

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

### <span data-ttu-id="7117b-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7117b-123">-SubscriptionId</span></span>
<span data-ttu-id="7117b-124">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7117b-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7117b-125">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="7117b-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7117b-126">– Skriv</span><span class="sxs-lookup"><span data-stu-id="7117b-126">-Type</span></span>
<span data-ttu-id="7117b-127">Typ av resurs, Microsoft. Kusto/kluster.</span><span class="sxs-lookup"><span data-stu-id="7117b-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

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

### <span data-ttu-id="7117b-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7117b-128">-Confirm</span></span>
<span data-ttu-id="7117b-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7117b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7117b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7117b-130">-WhatIf</span></span>
<span data-ttu-id="7117b-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7117b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7117b-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7117b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7117b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7117b-133">CommonParameters</span></span>
<span data-ttu-id="7117b-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7117b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7117b-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7117b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7117b-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7117b-136">INPUTS</span></span>

### <span data-ttu-id="7117b-137">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="7117b-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="7117b-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7117b-138">OUTPUTS</span></span>

### <span data-ttu-id="7117b-139">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="7117b-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="7117b-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7117b-140">NOTES</span></span>

<span data-ttu-id="7117b-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7117b-141">ALIASES</span></span>

<span data-ttu-id="7117b-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="7117b-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7117b-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="7117b-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7117b-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7117b-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7117b-145">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="7117b-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7117b-146">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="7117b-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="7117b-147">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="7117b-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="7117b-148">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="7117b-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="7117b-149">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="7117b-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="7117b-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="7117b-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7117b-151">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="7117b-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="7117b-152">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="7117b-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="7117b-153">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="7117b-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="7117b-154">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7117b-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7117b-155">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="7117b-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7117b-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7117b-156">RELATED LINKS</span></span>

