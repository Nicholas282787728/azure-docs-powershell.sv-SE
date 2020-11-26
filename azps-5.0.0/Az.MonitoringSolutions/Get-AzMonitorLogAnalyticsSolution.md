---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273253"
---
# <span data-ttu-id="e9aac-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="e9aac-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="e9aac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9aac-102">SYNOPSIS</span></span>
<span data-ttu-id="e9aac-103">Hämtar användar lösningen.</span><span class="sxs-lookup"><span data-stu-id="e9aac-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="e9aac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9aac-104">SYNTAX</span></span>

### <span data-ttu-id="e9aac-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="e9aac-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9aac-106">Lära</span><span class="sxs-lookup"><span data-stu-id="e9aac-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e9aac-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e9aac-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9aac-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="e9aac-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e9aac-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9aac-109">DESCRIPTION</span></span>
<span data-ttu-id="e9aac-110">Hämtar användar lösningen.</span><span class="sxs-lookup"><span data-stu-id="e9aac-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="e9aac-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9aac-111">EXAMPLES</span></span>

### <span data-ttu-id="e9aac-112">Exempel 1: skaffa en övervaka logganalys-lösning efter namn</span><span class="sxs-lookup"><span data-stu-id="e9aac-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="e9aac-113">Det här kommandot får en övervaka logganalys-lösning efter namn.</span><span class="sxs-lookup"><span data-stu-id="e9aac-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="e9aac-114">Exempel 2: skaffa en monitor logganalys-lösning via resurs-ID</span><span class="sxs-lookup"><span data-stu-id="e9aac-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="e9aac-115">Med det här kommandot får du en övervaka Log Analytics-lösning efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e9aac-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="e9aac-116">Exempel 3: skaffa en övervaka logg analys med objekt</span><span class="sxs-lookup"><span data-stu-id="e9aac-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="e9aac-117">Med det här kommandot får du en övervaka logg analys med objekt.</span><span class="sxs-lookup"><span data-stu-id="e9aac-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="e9aac-118">Exempel 4: Hämta alla övervakarens logg analys lösningar under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="e9aac-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="e9aac-119">Det här kommandot får alla övervaka logg analys lösningar under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e9aac-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="e9aac-120">Exempel 5: Hämta alla övervakarens logg analys lösningar under ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="e9aac-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="e9aac-121">Det här kommandot får alla övervaka logg analys lösningar under ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="e9aac-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="e9aac-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9aac-122">PARAMETERS</span></span>

### <span data-ttu-id="e9aac-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9aac-123">-DefaultProfile</span></span>
<span data-ttu-id="e9aac-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9aac-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9aac-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9aac-125">-InputObject</span></span>
<span data-ttu-id="e9aac-126">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e9aac-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9aac-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9aac-127">-Name</span></span>
<span data-ttu-id="e9aac-128">Namn på användar lösning.</span><span class="sxs-lookup"><span data-stu-id="e9aac-128">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aac-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9aac-129">-ResourceGroupName</span></span>
<span data-ttu-id="e9aac-130">Namnet på resurs gruppen som ska visas.</span><span class="sxs-lookup"><span data-stu-id="e9aac-130">The name of the resource group to get.</span></span>
<span data-ttu-id="e9aac-131">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="e9aac-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e9aac-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e9aac-132">-SubscriptionId</span></span>
<span data-ttu-id="e9aac-133">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e9aac-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e9aac-134">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e9aac-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9aac-135">CommonParameters</span></span>
<span data-ttu-id="e9aac-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9aac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9aac-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9aac-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9aac-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9aac-138">INPUTS</span></span>

### <span data-ttu-id="e9aac-139">Microsoft. Azure. PowerShell. cmdletar. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="e9aac-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="e9aac-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9aac-140">OUTPUTS</span></span>

### <span data-ttu-id="e9aac-141">Microsoft. Azure. PowerShell. cmdletar. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="e9aac-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="e9aac-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9aac-142">NOTES</span></span>

<span data-ttu-id="e9aac-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e9aac-143">ALIASES</span></span>

<span data-ttu-id="e9aac-144">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="e9aac-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e9aac-145">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="e9aac-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e9aac-146">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e9aac-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e9aac-147">INPUTOBJECT <IMonitoringSolutionsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e9aac-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e9aac-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e9aac-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e9aac-149">`[ManagementAssociationName <String>]`: Användar namnet ManagementAssociation.</span><span class="sxs-lookup"><span data-stu-id="e9aac-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="e9aac-150">`[ManagementConfigurationName <String>]`: Konfigurations namn för användar hantering.</span><span class="sxs-lookup"><span data-stu-id="e9aac-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="e9aac-151">`[ProviderName <String>]`: Leverantörens namn för den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="e9aac-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="e9aac-152">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som ska visas.</span><span class="sxs-lookup"><span data-stu-id="e9aac-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="e9aac-153">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="e9aac-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="e9aac-154">`[ResourceName <String>]`: Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="e9aac-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="e9aac-155">`[ResourceType <String>]`: Resurs typ för den överordnade resursen</span><span class="sxs-lookup"><span data-stu-id="e9aac-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="e9aac-156">`[SolutionName <String>]`: Användar lösningens namn.</span><span class="sxs-lookup"><span data-stu-id="e9aac-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="e9aac-157">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e9aac-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e9aac-158">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e9aac-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e9aac-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9aac-159">RELATED LINKS</span></span>
