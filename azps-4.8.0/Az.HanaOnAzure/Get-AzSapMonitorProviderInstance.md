---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 55ca24a7213dea4e9d0743689c080ebbb439430a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261108"
---
# <span data-ttu-id="cb939-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="cb939-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="cb939-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb939-102">SYNOPSIS</span></span>
<span data-ttu-id="cb939-103">Hämtar egenskaper för en tjänste instans för angiven prenumeration, resurs grupp, SapMonitor namn och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="cb939-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="cb939-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb939-104">SYNTAX</span></span>

### <span data-ttu-id="cb939-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="cb939-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cb939-106">Lära</span><span class="sxs-lookup"><span data-stu-id="cb939-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cb939-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cb939-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb939-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb939-108">DESCRIPTION</span></span>
<span data-ttu-id="cb939-109">Hämtar egenskaper för en tjänste instans för angiven prenumeration, resurs grupp, SapMonitor namn och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="cb939-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="cb939-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb939-110">EXAMPLES</span></span>

### <span data-ttu-id="cb939-111">Exempel 1: Hämta alla instanser under en SAP-bildskärm</span><span class="sxs-lookup"><span data-stu-id="cb939-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="cb939-112">Det här kommandot får alla instanser under en SAP-skärm.</span><span class="sxs-lookup"><span data-stu-id="cb939-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="cb939-113">Exempel 2: Hämta en instans av SAP monitor med namn</span><span class="sxs-lookup"><span data-stu-id="cb939-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="cb939-114">Det här kommandot får en instans av SAP monitor med namn.</span><span class="sxs-lookup"><span data-stu-id="cb939-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="cb939-115">Exempel 3: Hämta en instans av SAP Monitor by objekt</span><span class="sxs-lookup"><span data-stu-id="cb939-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="cb939-116">Det här kommandot får en instans av SAP Monitor by objekt.</span><span class="sxs-lookup"><span data-stu-id="cb939-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="cb939-117">Exempel 4: Hämta en instans av SAP Monitor by pipeline</span><span class="sxs-lookup"><span data-stu-id="cb939-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="cb939-118">Det här kommandot får en instans av SAP monitor via pipeline.</span><span class="sxs-lookup"><span data-stu-id="cb939-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="cb939-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb939-119">PARAMETERS</span></span>

### <span data-ttu-id="cb939-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb939-120">-DefaultProfile</span></span>
<span data-ttu-id="cb939-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb939-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb939-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb939-122">-InputObject</span></span>
<span data-ttu-id="cb939-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="cb939-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb939-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb939-124">-Name</span></span>
<span data-ttu-id="cb939-125">Namn på leverantörs instansen.</span><span class="sxs-lookup"><span data-stu-id="cb939-125">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb939-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb939-126">-ResourceGroupName</span></span>
<span data-ttu-id="cb939-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cb939-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="cb939-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="cb939-128">-SapMonitorName</span></span>
<span data-ttu-id="cb939-129">Namnet på SAP Monitor-resursen.</span><span class="sxs-lookup"><span data-stu-id="cb939-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="cb939-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb939-130">-SubscriptionId</span></span>
<span data-ttu-id="cb939-131">Abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cb939-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cb939-132">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="cb939-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb939-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb939-133">CommonParameters</span></span>
<span data-ttu-id="cb939-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb939-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb939-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb939-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb939-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb939-136">INPUTS</span></span>

### <span data-ttu-id="cb939-137">Microsoft. Azure. PowerShell. cmdletar. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="cb939-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="cb939-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb939-138">OUTPUTS</span></span>

### <span data-ttu-id="cb939-139">Microsoft. Azure. PowerShell. cmdletar. HanaOnAzure. Models. Api20200207Preview. IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="cb939-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="cb939-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb939-140">NOTES</span></span>

<span data-ttu-id="cb939-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cb939-141">ALIASES</span></span>

<span data-ttu-id="cb939-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="cb939-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cb939-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="cb939-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb939-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb939-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cb939-145">INPUTOBJECT <IHanaOnAzureIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="cb939-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb939-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="cb939-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb939-147">`[Location <String>]`: Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="cb939-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="cb939-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Åtgärdens namn</span><span class="sxs-lookup"><span data-stu-id="cb939-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="cb939-149">`[ProviderInstanceName <String>]`: Namnet på leverantörs instansen.</span><span class="sxs-lookup"><span data-stu-id="cb939-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="cb939-150">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="cb939-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="cb939-151">`[ResourceName <String>]`: Namnet på identitets resursen.</span><span class="sxs-lookup"><span data-stu-id="cb939-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="cb939-152">`[SapMonitorName <String>]`: Namnet på SAP Monitor-resursen.</span><span class="sxs-lookup"><span data-stu-id="cb939-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="cb939-153">`[Scope <String>]`: Resursens resurs leverantörs omfattning.</span><span class="sxs-lookup"><span data-stu-id="cb939-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="cb939-154">Överordnad resurs som utökas av hanterade identiteter.</span><span class="sxs-lookup"><span data-stu-id="cb939-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="cb939-155">`[SubscriptionId <String>]`: Prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cb939-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cb939-156">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="cb939-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cb939-157">`[VaultName <String>]`: Namnet på valvet</span><span class="sxs-lookup"><span data-stu-id="cb939-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="cb939-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb939-158">RELATED LINKS</span></span>

