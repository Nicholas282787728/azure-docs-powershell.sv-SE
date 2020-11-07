---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: b89bef906cf54378719c7c6b83dcaff484ced282
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923081"
---
# <span data-ttu-id="5393e-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="5393e-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="5393e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5393e-102">SYNOPSIS</span></span>


## <span data-ttu-id="5393e-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5393e-103">SYNTAX</span></span>

### <span data-ttu-id="5393e-104">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="5393e-104">Name (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5393e-105">QuotaObject</span><span class="sxs-lookup"><span data-stu-id="5393e-105">QuotaObject</span></span>
```
Set-AzsStorageQuota -QuotaObject <IStorageQuota> [-Location <String>] [-SubscriptionId <String>]
 [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5393e-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5393e-106">DESCRIPTION</span></span>


## <span data-ttu-id="5393e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5393e-107">EXAMPLES</span></span>

### <span data-ttu-id="5393e-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="5393e-108">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -NumberOfStorageAccounts 11 -CapacityInGb 22
```

<span data-ttu-id="5393e-109">Uppdatera en befintlig lagrings kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="5393e-109">Update an existing storage quota by name.</span></span>

### <span data-ttu-id="5393e-110">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="5393e-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestUpdateStorageQuota' | Set-AzsStorageQuota -NumberOfStorageAccounts 22 -CapacityInGb 33
```

<span data-ttu-id="5393e-111">Uppdatera en befintlig lagrings kvot efter överföring.</span><span class="sxs-lookup"><span data-stu-id="5393e-111">Update an existing storage quota by piping.</span></span>

## <span data-ttu-id="5393e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5393e-112">PARAMETERS</span></span>

### <span data-ttu-id="5393e-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="5393e-113">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5393e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5393e-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="5393e-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="5393e-115">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5393e-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="5393e-116">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Name
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5393e-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="5393e-117">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5393e-118">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="5393e-118">-QuotaObject</span></span>
<span data-ttu-id="5393e-119">För att konstruera kan du läsa avsnittet anteckningar för QUOTAOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5393e-119">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: QuotaObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5393e-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5393e-120">-SubscriptionId</span></span>


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

### <span data-ttu-id="5393e-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5393e-121">-Confirm</span></span>
<span data-ttu-id="5393e-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5393e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5393e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5393e-123">-WhatIf</span></span>
<span data-ttu-id="5393e-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5393e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5393e-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5393e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5393e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5393e-126">CommonParameters</span></span>
<span data-ttu-id="5393e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5393e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5393e-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5393e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5393e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5393e-129">INPUTS</span></span>

### <span data-ttu-id="5393e-130">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="5393e-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="5393e-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5393e-131">OUTPUTS</span></span>

### <span data-ttu-id="5393e-132">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="5393e-132">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="5393e-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5393e-133">NOTES</span></span>

<span data-ttu-id="5393e-134">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="5393e-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5393e-135">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5393e-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5393e-136">QUOTAOBJECT <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="5393e-136">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="5393e-137">`[CapacityInGb <Int32?>]`: Maximal kapacitet (GB).</span><span class="sxs-lookup"><span data-stu-id="5393e-137">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="5393e-138">`[NumberOfStorageAccounts <Int32?>]`: Totalt antal lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="5393e-138">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="5393e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5393e-139">RELATED LINKS</span></span>

