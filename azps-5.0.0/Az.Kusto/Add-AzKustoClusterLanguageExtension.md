---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/add-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Add-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 11789a16186d0f7c8358371ace2a454d78d932df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272263"
---
# <span data-ttu-id="76100-101">Add-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="76100-101">Add-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="76100-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76100-102">SYNOPSIS</span></span>
<span data-ttu-id="76100-103">Lägga till en lista över språk tillägg som kan köras i Keyword-frågor.</span><span class="sxs-lookup"><span data-stu-id="76100-103">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="76100-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76100-104">SYNTAX</span></span>

### <span data-ttu-id="76100-105">AddExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="76100-105">AddExpanded (Default)</span></span>
```
Add-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <ILanguageExtension[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76100-106">AddViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="76100-106">AddViaIdentityExpanded</span></span>
```
Add-AzKustoClusterLanguageExtension -InputObject <IKustoIdentity> [-Value <ILanguageExtension[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76100-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76100-107">DESCRIPTION</span></span>
<span data-ttu-id="76100-108">Lägga till en lista över språk tillägg som kan köras i Keyword-frågor.</span><span class="sxs-lookup"><span data-stu-id="76100-108">Add a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="76100-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76100-109">EXAMPLES</span></span>

### <span data-ttu-id="76100-110">Exempel 1: lägga till en lista över språk tillägg</span><span class="sxs-lookup"><span data-stu-id="76100-110">Example 1: Add a list of language extensions</span></span>
```powershell
PS C:\> Add-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster -Value (@{Name="R"}, @{Name="PYTHON"})
```

<span data-ttu-id="76100-111">Kommandot ovan lägger till en lista över språk tillägg som kan köras i Keyword-frågor</span><span class="sxs-lookup"><span data-stu-id="76100-111">The above command adds a list of language extensions that can run within KQL queries</span></span>

## <span data-ttu-id="76100-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76100-112">PARAMETERS</span></span>

### <span data-ttu-id="76100-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76100-113">-AsJob</span></span>
<span data-ttu-id="76100-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="76100-114">Run the command as a job</span></span>

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

### <span data-ttu-id="76100-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="76100-115">-ClusterName</span></span>
<span data-ttu-id="76100-116">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="76100-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76100-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76100-117">-DefaultProfile</span></span>
<span data-ttu-id="76100-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76100-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76100-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76100-119">-InputObject</span></span>
<span data-ttu-id="76100-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="76100-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: AddViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76100-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="76100-121">-NoWait</span></span>
<span data-ttu-id="76100-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="76100-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="76100-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76100-123">-PassThru</span></span>
<span data-ttu-id="76100-124">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="76100-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="76100-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76100-125">-ResourceGroupName</span></span>
<span data-ttu-id="76100-126">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="76100-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76100-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76100-127">-SubscriptionId</span></span>
<span data-ttu-id="76100-128">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="76100-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="76100-129">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="76100-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: AddExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76100-130">-Värde</span><span class="sxs-lookup"><span data-stu-id="76100-130">-Value</span></span>
<span data-ttu-id="76100-131">Listan över språk tillägg.</span><span class="sxs-lookup"><span data-stu-id="76100-131">The list of language extensions.</span></span>
<span data-ttu-id="76100-132">Om du vill skapa läser du avsnittet anteckningar för värde egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="76100-132">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76100-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="76100-133">-Confirm</span></span>
<span data-ttu-id="76100-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="76100-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76100-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76100-135">-WhatIf</span></span>
<span data-ttu-id="76100-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="76100-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76100-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="76100-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76100-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76100-138">CommonParameters</span></span>
<span data-ttu-id="76100-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76100-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76100-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76100-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76100-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76100-141">INPUTS</span></span>

### <span data-ttu-id="76100-142">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="76100-142">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="76100-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76100-143">OUTPUTS</span></span>

### <span data-ttu-id="76100-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76100-144">System.Boolean</span></span>

## <span data-ttu-id="76100-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76100-145">NOTES</span></span>

<span data-ttu-id="76100-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="76100-146">ALIASES</span></span>

<span data-ttu-id="76100-147">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="76100-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76100-148">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="76100-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76100-149">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76100-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76100-150">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="76100-150">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76100-151">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="76100-151">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="76100-152">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="76100-152">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="76100-153">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="76100-153">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="76100-154">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="76100-154">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="76100-155">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="76100-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76100-156">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="76100-156">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="76100-157">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="76100-157">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="76100-158">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="76100-158">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="76100-159">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="76100-159">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="76100-160">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="76100-160">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="76100-161">VÄRDE <ILanguageExtension [] >: listan med språk tillägg.</span><span class="sxs-lookup"><span data-stu-id="76100-161">VALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="76100-162">`[Name <LanguageExtensionName?>]`: Namnet på språk tillägget.</span><span class="sxs-lookup"><span data-stu-id="76100-162">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

## <span data-ttu-id="76100-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76100-163">RELATED LINKS</span></span>

