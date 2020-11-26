---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263073"
---
# <span data-ttu-id="4ba6e-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="4ba6e-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="4ba6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ba6e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba6e-103">Hämtar egenskaper för en SAP-bildskärm för angiven prenumeration, resurs grupp och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="4ba6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ba6e-104">SYNTAX</span></span>

### <span data-ttu-id="4ba6e-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="4ba6e-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4ba6e-106">Lära</span><span class="sxs-lookup"><span data-stu-id="4ba6e-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4ba6e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4ba6e-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4ba6e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ba6e-108">DESCRIPTION</span></span>
<span data-ttu-id="4ba6e-109">Hämtar egenskaper för en SAP-bildskärm för angiven prenumeration, resurs grupp och resurs namn.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="4ba6e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ba6e-110">EXAMPLES</span></span>

### <span data-ttu-id="4ba6e-111">Exempel 1: Hämta alla SAP-skärmar under ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="4ba6e-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="4ba6e-112">Det här kommandot får SAP-skärmar under ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="4ba6e-113">Exempel 2: skaffa en SAP-övervakare efter namn</span><span class="sxs-lookup"><span data-stu-id="4ba6e-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="4ba6e-114">Det här kommandot får SAP-övervakaren med namn.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="4ba6e-115">Exempel 3: Hämta en SAP-övervakare efter objekt</span><span class="sxs-lookup"><span data-stu-id="4ba6e-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="4ba6e-116">Det här kommandot får en SAP-skärm per objekt.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="4ba6e-117">Exempel 4: skaffa en SAP-bildskärm via rörledning</span><span class="sxs-lookup"><span data-stu-id="4ba6e-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="4ba6e-118">Det här kommandot får en SAP-skärm via pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="4ba6e-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ba6e-119">PARAMETERS</span></span>

### <span data-ttu-id="4ba6e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba6e-120">-DefaultProfile</span></span>
<span data-ttu-id="4ba6e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ba6e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ba6e-122">-InputObject</span></span>
<span data-ttu-id="4ba6e-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4ba6e-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ba6e-124">-Name</span></span>
<span data-ttu-id="4ba6e-125">Namnet på SAP Monitor-resursen.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-125">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba6e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ba6e-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ba6e-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba6e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ba6e-128">-SubscriptionId</span></span>
<span data-ttu-id="4ba6e-129">Abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4ba6e-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4ba6e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba6e-131">CommonParameters</span></span>
<span data-ttu-id="4ba6e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba6e-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ba6e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba6e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ba6e-134">INPUTS</span></span>

### <span data-ttu-id="4ba6e-135">Microsoft. Azure. PowerShell. cmdletar. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="4ba6e-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="4ba6e-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ba6e-136">OUTPUTS</span></span>

### <span data-ttu-id="4ba6e-137">Microsoft. Azure. PowerShell. cmdletar. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="4ba6e-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="4ba6e-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ba6e-138">NOTES</span></span>

<span data-ttu-id="4ba6e-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4ba6e-139">ALIASES</span></span>

<span data-ttu-id="4ba6e-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="4ba6e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4ba6e-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ba6e-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4ba6e-143">INPUTOBJECT <IHanaOnAzureIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="4ba6e-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4ba6e-144">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="4ba6e-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4ba6e-145">`[Location <String>]`: Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="4ba6e-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Åtgärdens namn</span><span class="sxs-lookup"><span data-stu-id="4ba6e-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="4ba6e-147">`[ProviderInstanceName <String>]`: Namnet på leverantörs instansen.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="4ba6e-148">`[ResourceGroupName <String>]`: Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="4ba6e-149">`[ResourceName <String>]`: Namnet på identitets resursen.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="4ba6e-150">`[SapMonitorName <String>]`: Namnet på SAP Monitor-resursen.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="4ba6e-151">`[Scope <String>]`: Resursens resurs leverantörs omfattning.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="4ba6e-152">Överordnad resurs som utökas av hanterade identiteter.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="4ba6e-153">`[SubscriptionId <String>]`: Prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4ba6e-154">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="4ba6e-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4ba6e-155">`[VaultName <String>]`: Namnet på valvet</span><span class="sxs-lookup"><span data-stu-id="4ba6e-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="4ba6e-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ba6e-156">RELATED LINKS</span></span>
