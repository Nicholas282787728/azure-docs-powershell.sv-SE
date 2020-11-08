---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272229"
---
# <span data-ttu-id="dbd63-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dbd63-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="dbd63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbd63-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd63-103">Diagnostiserar nätverks anslutnings status för externa resurser som tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="dbd63-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="dbd63-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbd63-104">SYNTAX</span></span>

### <span data-ttu-id="dbd63-105">Diagnosticera (standard)</span><span class="sxs-lookup"><span data-stu-id="dbd63-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="dbd63-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dbd63-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dbd63-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbd63-107">DESCRIPTION</span></span>
<span data-ttu-id="dbd63-108">Diagnostiserar nätverks anslutnings status för externa resurser som tjänsten är beroende av.</span><span class="sxs-lookup"><span data-stu-id="dbd63-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="dbd63-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbd63-109">EXAMPLES</span></span>

### <span data-ttu-id="dbd63-110">Exempel 1: Visa nätverks anslutnings diagnos för externa resurser</span><span class="sxs-lookup"><span data-stu-id="dbd63-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="dbd63-111">Ovanstående kommando diagnostiserar nätverks anslutnings status för externa resurser där klustret "testnewkustocluster" är beroende av</span><span class="sxs-lookup"><span data-stu-id="dbd63-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="dbd63-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbd63-112">PARAMETERS</span></span>

### <span data-ttu-id="dbd63-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbd63-113">-AsJob</span></span>
<span data-ttu-id="dbd63-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="dbd63-114">Run the command as a job</span></span>

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

### <span data-ttu-id="dbd63-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="dbd63-115">-ClusterName</span></span>
<span data-ttu-id="dbd63-116">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="dbd63-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd63-117">-DefaultProfile</span></span>
<span data-ttu-id="dbd63-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dbd63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbd63-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbd63-119">-InputObject</span></span>
<span data-ttu-id="dbd63-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="dbd63-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DiagnoseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd63-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="dbd63-121">-NoWait</span></span>
<span data-ttu-id="dbd63-122">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="dbd63-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dbd63-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbd63-123">-ResourceGroupName</span></span>
<span data-ttu-id="dbd63-124">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="dbd63-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd63-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dbd63-125">-SubscriptionId</span></span>
<span data-ttu-id="dbd63-126">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="dbd63-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dbd63-127">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="dbd63-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd63-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dbd63-128">-Confirm</span></span>
<span data-ttu-id="dbd63-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dbd63-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbd63-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbd63-130">-WhatIf</span></span>
<span data-ttu-id="dbd63-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dbd63-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbd63-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dbd63-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbd63-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd63-133">CommonParameters</span></span>
<span data-ttu-id="dbd63-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd63-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd63-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbd63-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd63-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbd63-136">INPUTS</span></span>

### <span data-ttu-id="dbd63-137">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="dbd63-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="dbd63-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbd63-138">OUTPUTS</span></span>

### <span data-ttu-id="dbd63-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dbd63-139">System.String</span></span>

## <span data-ttu-id="dbd63-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbd63-140">NOTES</span></span>

<span data-ttu-id="dbd63-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dbd63-141">ALIASES</span></span>

<span data-ttu-id="dbd63-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="dbd63-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dbd63-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="dbd63-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dbd63-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dbd63-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dbd63-145">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="dbd63-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dbd63-146">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="dbd63-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="dbd63-147">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="dbd63-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="dbd63-148">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="dbd63-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="dbd63-149">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="dbd63-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="dbd63-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="dbd63-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dbd63-151">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="dbd63-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="dbd63-152">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="dbd63-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="dbd63-153">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="dbd63-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="dbd63-154">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="dbd63-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dbd63-155">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="dbd63-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dbd63-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbd63-156">RELATED LINKS</span></span>

