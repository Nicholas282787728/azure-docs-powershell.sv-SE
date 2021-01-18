---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: 3101ca2b120860dfa6df95786e235fc88fd0fc78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527067"
---
# <span data-ttu-id="e1449-101">Get-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="e1449-101">Get-AzCommunicationService</span></span>

## <span data-ttu-id="e1449-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1449-102">SYNOPSIS</span></span>
<span data-ttu-id="e1449-103">Hämta CommunicationService och dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e1449-103">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="e1449-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1449-104">SYNTAX</span></span>

### <span data-ttu-id="e1449-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="e1449-105">List (Default)</span></span>
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e1449-106">Lära</span><span class="sxs-lookup"><span data-stu-id="e1449-106">Get</span></span>
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e1449-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e1449-107">GetViaIdentity</span></span>
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1449-108">List1</span><span class="sxs-lookup"><span data-stu-id="e1449-108">List1</span></span>
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e1449-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1449-109">DESCRIPTION</span></span>
<span data-ttu-id="e1449-110">Hämta CommunicationService och dess egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e1449-110">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="e1449-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1449-111">EXAMPLES</span></span>

### <span data-ttu-id="e1449-112">Exempel 1: Visa en lista över befintliga CommunicationServices för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="e1449-112">Example 1: List existing CommunicationServices for a Subscription</span></span>
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

<span data-ttu-id="e1449-113">Returnerar en lista över alla ACS-resurser under det abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e1449-113">Returns a list of all ACS resources under that subscription.</span></span>

### <span data-ttu-id="e1449-114">Exempel 2: Hämta information om den angivna Azure Communication-resursen</span><span class="sxs-lookup"><span data-stu-id="e1449-114">Example 2: Get infomation on specified Azure Communication resource</span></span>
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="e1449-115">Returnerar informationen på en ACS-resurs, om en matchande angiven parameter hittas.</span><span class="sxs-lookup"><span data-stu-id="e1449-115">Returns the information on an ACS resource, if one matching provided parameters is found.</span></span>

## <span data-ttu-id="e1449-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1449-116">PARAMETERS</span></span>

### <span data-ttu-id="e1449-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1449-117">-DefaultProfile</span></span>
<span data-ttu-id="e1449-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1449-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1449-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1449-119">-InputObject</span></span>
<span data-ttu-id="e1449-120">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e1449-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1449-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="e1449-121">-Name</span></span>
<span data-ttu-id="e1449-122">Namnet på CommunicationService-resursen.</span><span class="sxs-lookup"><span data-stu-id="e1449-122">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1449-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1449-123">-ResourceGroupName</span></span>
<span data-ttu-id="e1449-124">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="e1449-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e1449-125">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="e1449-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1449-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1449-126">-SubscriptionId</span></span>
<span data-ttu-id="e1449-127">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e1449-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e1449-128">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e1449-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e1449-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1449-129">CommonParameters</span></span>
<span data-ttu-id="e1449-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1449-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1449-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1449-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1449-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1449-132">INPUTS</span></span>

### <span data-ttu-id="e1449-133">Microsoft. Azure. PowerShell. cmdletar. Communication. Models. ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="e1449-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="e1449-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1449-134">OUTPUTS</span></span>

### <span data-ttu-id="e1449-135">Microsoft. Azure. PowerShell. cmdletar. Communication. Models. Api20200820Preview. ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="e1449-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="e1449-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1449-136">NOTES</span></span>

<span data-ttu-id="e1449-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e1449-137">ALIASES</span></span>

<span data-ttu-id="e1449-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="e1449-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e1449-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="e1449-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e1449-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e1449-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e1449-141">INPUTOBJECT <ICommunicationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="e1449-141">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e1449-142">`[CommunicationServiceName <String>]`: Namnet på CommunicationService-resursen.</span><span class="sxs-lookup"><span data-stu-id="e1449-142">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="e1449-143">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="e1449-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e1449-144">`[Location <String>]`: Azure-regionen</span><span class="sxs-lookup"><span data-stu-id="e1449-144">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="e1449-145">`[OperationId <String>]`: ID för pågående asynkron åtgärd</span><span class="sxs-lookup"><span data-stu-id="e1449-145">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="e1449-146">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="e1449-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e1449-147">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="e1449-147">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e1449-148">`[SubscriptionId <String>]`: Hämtar prenumerations-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e1449-148">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="e1449-149">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="e1449-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e1449-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1449-150">RELATED LINKS</span></span>

