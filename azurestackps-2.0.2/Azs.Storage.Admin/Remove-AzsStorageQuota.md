---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/remove-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: 258c7057b8f78ea6de1db506d23c60f679e1ca39
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099980"
---
# <span data-ttu-id="aa3df-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="aa3df-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="aa3df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa3df-102">SYNOPSIS</span></span>


## <span data-ttu-id="aa3df-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa3df-103">SYNTAX</span></span>

### <span data-ttu-id="aa3df-104">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="aa3df-104">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aa3df-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aa3df-105">DeleteViaIdentity</span></span>
```
Remove-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aa3df-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa3df-106">DESCRIPTION</span></span>


## <span data-ttu-id="aa3df-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa3df-107">EXAMPLES</span></span>

### <span data-ttu-id="aa3df-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="aa3df-108">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsStorageQuota -Name 'TestQuota'
```

<span data-ttu-id="aa3df-109">Ta bort en lagrings kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="aa3df-109">Remove a storage quota by name.</span></span>

### <span data-ttu-id="aa3df-110">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="aa3df-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestQuota' | Remove-AzsStorageQuota
```

<span data-ttu-id="aa3df-111">Ta bort en lagrings kvot efter överföring.</span><span class="sxs-lookup"><span data-stu-id="aa3df-111">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="aa3df-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa3df-112">PARAMETERS</span></span>

### <span data-ttu-id="aa3df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa3df-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="aa3df-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa3df-114">-InputObject</span></span>
<span data-ttu-id="aa3df-115">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="aa3df-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="aa3df-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="aa3df-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aa3df-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="aa3df-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aa3df-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa3df-118">-PassThru</span></span>


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

### <span data-ttu-id="aa3df-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa3df-119">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aa3df-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aa3df-120">-Confirm</span></span>
<span data-ttu-id="aa3df-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aa3df-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa3df-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa3df-122">-WhatIf</span></span>
<span data-ttu-id="aa3df-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aa3df-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa3df-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aa3df-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa3df-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa3df-125">CommonParameters</span></span>
<span data-ttu-id="aa3df-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa3df-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa3df-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa3df-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa3df-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa3df-128">INPUTS</span></span>

### <span data-ttu-id="aa3df-129">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="aa3df-129">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="aa3df-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa3df-130">OUTPUTS</span></span>

### <span data-ttu-id="aa3df-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa3df-131">System.Boolean</span></span>



## <span data-ttu-id="aa3df-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa3df-132">NOTES</span></span>

<span data-ttu-id="aa3df-133">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="aa3df-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa3df-134">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aa3df-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="aa3df-135">INPUTOBJECT <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="aa3df-135">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="aa3df-136">`[AccountId <String>]`: Internt lagrings konto-ID som inte är synligt för klient organisationen.</span><span class="sxs-lookup"><span data-stu-id="aa3df-136">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="aa3df-137">`[AsyncOperationId <String>]`: Asynkron åtgärds-ID.</span><span class="sxs-lookup"><span data-stu-id="aa3df-137">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="aa3df-138">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="aa3df-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aa3df-139">`[Location <String>]`: Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="aa3df-139">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="aa3df-140">`[QuotaName <String>]`: Namnet på lagrings kvoten.</span><span class="sxs-lookup"><span data-stu-id="aa3df-140">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="aa3df-141">`[ResourceGroup <String>]`: Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="aa3df-141">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="aa3df-142">`[ServiceName <String>]`: Namn på lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="aa3df-142">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="aa3df-143">`[SubscriptionId <String>]`: Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="aa3df-143">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="aa3df-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa3df-144">RELATED LINKS</span></span>

