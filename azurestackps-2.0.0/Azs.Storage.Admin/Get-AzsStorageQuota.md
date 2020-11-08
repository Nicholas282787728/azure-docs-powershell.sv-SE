---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94092811"
---
# <span data-ttu-id="4c957-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="4c957-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="4c957-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c957-102">SYNOPSIS</span></span>


## <span data-ttu-id="4c957-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c957-103">SYNTAX</span></span>

### <span data-ttu-id="4c957-104">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="4c957-104">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c957-105">Lära</span><span class="sxs-lookup"><span data-stu-id="4c957-105">Get</span></span>
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4c957-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4c957-106">GetViaIdentity</span></span>
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4c957-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c957-107">DESCRIPTION</span></span>


## <span data-ttu-id="4c957-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c957-108">EXAMPLES</span></span>

### <span data-ttu-id="4c957-109">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="4c957-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota
```

<span data-ttu-id="4c957-110">Hämta listan med lagrings kvoter.</span><span class="sxs-lookup"><span data-stu-id="4c957-110">Get the list of storage quotas.</span></span>

### <span data-ttu-id="4c957-111">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="4c957-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

<span data-ttu-id="4c957-112">Få information om den angivna lagrings kvoten efter namn.</span><span class="sxs-lookup"><span data-stu-id="4c957-112">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="4c957-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c957-113">PARAMETERS</span></span>

### <span data-ttu-id="4c957-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c957-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="4c957-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c957-115">-InputObject</span></span>
<span data-ttu-id="4c957-116">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="4c957-116">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: System.String
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4c957-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="4c957-117">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4c957-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4c957-118">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4c957-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c957-119">-SubscriptionId</span></span>


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

### <span data-ttu-id="4c957-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c957-120">CommonParameters</span></span>
<span data-ttu-id="4c957-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c957-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c957-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c957-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c957-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c957-123">INPUTS</span></span>

### <span data-ttu-id="4c957-124">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="4c957-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="4c957-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c957-125">OUTPUTS</span></span>

### <span data-ttu-id="4c957-126">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="4c957-126">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="4c957-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c957-127">NOTES</span></span>

<span data-ttu-id="4c957-128">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="4c957-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4c957-129">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4c957-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4c957-130">INPUTOBJECT <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="4c957-130">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="4c957-131">`[AccountId <String>]`: Internt lagrings konto-ID som inte är synligt för klient organisationen.</span><span class="sxs-lookup"><span data-stu-id="4c957-131">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="4c957-132">`[AsyncOperationId <String>]`: Asynkron åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="4c957-132">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="4c957-133">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="4c957-133">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4c957-134">`[Location <String>]`: Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="4c957-134">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="4c957-135">`[QuotaName <String>]`: Namnet på lagrings kvoten.</span><span class="sxs-lookup"><span data-stu-id="4c957-135">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="4c957-136">`[ResourceGroup <String>]`: Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4c957-136">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="4c957-137">`[ServiceName <String>]`: Namn på lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="4c957-137">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="4c957-138">`[SubscriptionId <String>]`: Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="4c957-138">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="4c957-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c957-139">RELATED LINKS</span></span>
