---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 26da7e8b0bf3ca24edd9f4abd52f0c27aabf49e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409011"
---
# <span data-ttu-id="d4c3d-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4c3d-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="d4c3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c3d-103">Skapar eller uppdaterar en ansluten databas konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="d4c3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4c3d-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d4c3d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4c3d-105">DESCRIPTION</span></span>
<span data-ttu-id="d4c3d-106">Skapar eller uppdaterar en ansluten databas konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="d4c3d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4c3d-107">EXAMPLES</span></span>

### <span data-ttu-id="d4c3d-108">Exempel 1: skapa en ny AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4c3d-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="d4c3d-109">Kommandot ovan skapar en ReadOnly-databas "mykustodatabase" i klustret "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="d4c3d-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="d4c3d-110">Det följer databasen "mykustodatabase" från kluster "testnewkustocluster"</span><span class="sxs-lookup"><span data-stu-id="d4c3d-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="d4c3d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4c3d-111">PARAMETERS</span></span>

### <span data-ttu-id="d4c3d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4c3d-112">-AsJob</span></span>
<span data-ttu-id="d4c3d-113">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="d4c3d-113">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c3d-114">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="d4c3d-114">-ClusterName</span></span>
<span data-ttu-id="d4c3d-115">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d4c3d-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="d4c3d-116">-ClusterResourceId</span></span>
<span data-ttu-id="d4c3d-117">Resurs-ID för det kluster där databaserna som du vill ansluta finns.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c3d-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d4c3d-118">-DatabaseName</span></span>
<span data-ttu-id="d4c3d-119">Namnet på den databas som du vill bifoga, Använd \* om du vill följa alla aktuella och framtida databaser.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c3d-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="d4c3d-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="d4c3d-121">Standard principens ändrings typ</span><span class="sxs-lookup"><span data-stu-id="d4c3d-121">The default principals modification kind</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DefaultPrincipalsModificationKind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c3d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c3d-122">-DefaultProfile</span></span>
<span data-ttu-id="d4c3d-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4c3d-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="d4c3d-124">-Location</span></span>
<span data-ttu-id="d4c3d-125">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-125">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c3d-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="d4c3d-126">-Name</span></span>
<span data-ttu-id="d4c3d-127">Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-127">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c3d-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d4c3d-128">-NoWait</span></span>
<span data-ttu-id="d4c3d-129">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="d4c3d-129">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c3d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c3d-130">-ResourceGroupName</span></span>
<span data-ttu-id="d4c3d-131">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d4c3d-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4c3d-132">-SubscriptionId</span></span>
<span data-ttu-id="d4c3d-133">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d4c3d-134">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c3d-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4c3d-135">-Confirm</span></span>
<span data-ttu-id="d4c3d-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4c3d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4c3d-137">-WhatIf</span></span>
<span data-ttu-id="d4c3d-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4c3d-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4c3d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c3d-140">CommonParameters</span></span>
<span data-ttu-id="d4c3d-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4c3d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c3d-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4c3d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c3d-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4c3d-143">INPUTS</span></span>

## <span data-ttu-id="d4c3d-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4c3d-144">OUTPUTS</span></span>

### <span data-ttu-id="d4c3d-145">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4c3d-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="d4c3d-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4c3d-146">NOTES</span></span>

<span data-ttu-id="d4c3d-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d4c3d-147">ALIASES</span></span>

## <span data-ttu-id="d4c3d-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4c3d-148">RELATED LINKS</span></span>

