---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 0ddf99277834e69a55b009abcb4b683eebb7a4ec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099884"
---
# <span data-ttu-id="395ba-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="395ba-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="395ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="395ba-102">SYNOPSIS</span></span>
<span data-ttu-id="395ba-103">Returnerar det begärda lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="395ba-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="395ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="395ba-104">SYNTAX</span></span>

### <span data-ttu-id="395ba-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="395ba-105">List (Default)</span></span>
```
Get-AzsStorageAccount [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Summary]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="395ba-106">Lära</span><span class="sxs-lookup"><span data-stu-id="395ba-106">Get</span></span>
```
Get-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="395ba-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="395ba-107">GetViaIdentity</span></span>
```
Get-AzsStorageAccount -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="395ba-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="395ba-108">DESCRIPTION</span></span>
<span data-ttu-id="395ba-109">Returnerar det begärda lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="395ba-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="395ba-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="395ba-110">EXAMPLES</span></span>

### <span data-ttu-id="395ba-111">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="395ba-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Summary
```

<span data-ttu-id="395ba-112">Få en lista med lagrings konton (sammanfattning).</span><span class="sxs-lookup"><span data-stu-id="395ba-112">Get a list of storage accounts (summary).</span></span>

### <span data-ttu-id="395ba-113">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="395ba-113">Example 2:</span></span>
```powershell
PS C:\> $storageAccount = Get-AzsStorageAccount
PS C:\> $storageAccount | Select Location,Name,AccountStatus,HealthState,Kind | ft
```

<span data-ttu-id="395ba-114">Få en lista med lagrings konto information och skriv ut status.</span><span class="sxs-lookup"><span data-stu-id="395ba-114">Get a list of storage account with details and print the status.</span></span>

### <span data-ttu-id="395ba-115">Exempel 3:</span><span class="sxs-lookup"><span data-stu-id="395ba-115">Example 3:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 | fl *
```

<span data-ttu-id="395ba-116">Få information om det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="395ba-116">Get details of the specified storage account.</span></span>

## <span data-ttu-id="395ba-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="395ba-117">PARAMETERS</span></span>

### <span data-ttu-id="395ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395ba-118">-DefaultProfile</span></span>
<span data-ttu-id="395ba-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="395ba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="395ba-120">-Filter</span><span class="sxs-lookup"><span data-stu-id="395ba-120">-Filter</span></span>
<span data-ttu-id="395ba-121">Filter sträng</span><span class="sxs-lookup"><span data-stu-id="395ba-121">Filter string</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="395ba-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="395ba-122">-InputObject</span></span>
<span data-ttu-id="395ba-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="395ba-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="395ba-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="395ba-124">-Location</span></span>
<span data-ttu-id="395ba-125">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="395ba-125">Resource location.</span></span>

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

### <span data-ttu-id="395ba-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="395ba-126">-Name</span></span>
<span data-ttu-id="395ba-127">Internt lagrings konto-ID som inte är synligt för klient organisationen.</span><span class="sxs-lookup"><span data-stu-id="395ba-127">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="395ba-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="395ba-128">-SubscriptionId</span></span>
<span data-ttu-id="395ba-129">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="395ba-129">Subscription Id.</span></span>

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

### <span data-ttu-id="395ba-130">-Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="395ba-130">-Summary</span></span>
<span data-ttu-id="395ba-131">Växel för om Sammanfattning eller detaljerad information ska returneras.</span><span class="sxs-lookup"><span data-stu-id="395ba-131">Switch for whether summary or detailed information is returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: $false
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="395ba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395ba-132">CommonParameters</span></span>
<span data-ttu-id="395ba-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="395ba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395ba-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="395ba-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395ba-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="395ba-135">INPUTS</span></span>

### <span data-ttu-id="395ba-136">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="395ba-136">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="395ba-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="395ba-137">OUTPUTS</span></span>

### <span data-ttu-id="395ba-138">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. Api201908Preview. IStorageAccount</span><span class="sxs-lookup"><span data-stu-id="395ba-138">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageAccount</span></span>



## <span data-ttu-id="395ba-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="395ba-139">NOTES</span></span>

<span data-ttu-id="395ba-140">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="395ba-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="395ba-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="395ba-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="395ba-142">INPUTOBJECT <IStorageAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="395ba-142">INPUTOBJECT <IStorageAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="395ba-143">`[AccountId <String>]`: Internt lagrings konto-ID som inte är synligt för klient organisationen.</span><span class="sxs-lookup"><span data-stu-id="395ba-143">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="395ba-144">`[AsyncOperationId <String>]`: Asynkron åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="395ba-144">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="395ba-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="395ba-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="395ba-146">`[Location <String>]`: Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="395ba-146">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="395ba-147">`[QuotaName <String>]`: Namnet på lagrings kvoten.</span><span class="sxs-lookup"><span data-stu-id="395ba-147">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="395ba-148">`[ResourceGroup <String>]`: Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="395ba-148">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="395ba-149">`[ServiceName <String>]`: Namn på lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="395ba-149">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="395ba-150">`[SubscriptionId <String>]`: Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="395ba-150">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="395ba-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="395ba-151">RELATED LINKS</span></span>

