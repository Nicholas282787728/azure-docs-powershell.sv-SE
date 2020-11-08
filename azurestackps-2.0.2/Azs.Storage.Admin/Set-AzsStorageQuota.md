---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: b89bef906cf54378719c7c6b83dcaff484ced282
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099977"
---
# <span data-ttu-id="7cac5-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="7cac5-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="7cac5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cac5-102">SYNOPSIS</span></span>


## <span data-ttu-id="7cac5-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cac5-103">SYNTAX</span></span>

### <span data-ttu-id="7cac5-104">Namn (standard)</span><span class="sxs-lookup"><span data-stu-id="7cac5-104">Name (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7cac5-105">QuotaObject</span><span class="sxs-lookup"><span data-stu-id="7cac5-105">QuotaObject</span></span>
```
Set-AzsStorageQuota -QuotaObject <IStorageQuota> [-Location <String>] [-SubscriptionId <String>]
 [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7cac5-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cac5-106">DESCRIPTION</span></span>


## <span data-ttu-id="7cac5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cac5-107">EXAMPLES</span></span>

### <span data-ttu-id="7cac5-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="7cac5-108">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -NumberOfStorageAccounts 11 -CapacityInGb 22
```

<span data-ttu-id="7cac5-109">Uppdatera en befintlig lagrings kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="7cac5-109">Update an existing storage quota by name.</span></span>

### <span data-ttu-id="7cac5-110">Exempel 2:</span><span class="sxs-lookup"><span data-stu-id="7cac5-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestUpdateStorageQuota' | Set-AzsStorageQuota -NumberOfStorageAccounts 22 -CapacityInGb 33
```

<span data-ttu-id="7cac5-111">Uppdatera en befintlig lagrings kvot efter överföring.</span><span class="sxs-lookup"><span data-stu-id="7cac5-111">Update an existing storage quota by piping.</span></span>

## <span data-ttu-id="7cac5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cac5-112">PARAMETERS</span></span>

### <span data-ttu-id="7cac5-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="7cac5-113">-CapacityInGb</span></span>


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

### <span data-ttu-id="7cac5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cac5-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="7cac5-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="7cac5-115">-Location</span></span>


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

### <span data-ttu-id="7cac5-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="7cac5-116">-Name</span></span>


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

### <span data-ttu-id="7cac5-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="7cac5-117">-NumberOfStorageAccounts</span></span>


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

### <span data-ttu-id="7cac5-118">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="7cac5-118">-QuotaObject</span></span>
<span data-ttu-id="7cac5-119">För att konstruera kan du läsa avsnittet anteckningar för QUOTAOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7cac5-119">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7cac5-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cac5-120">-SubscriptionId</span></span>


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

### <span data-ttu-id="7cac5-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7cac5-121">-Confirm</span></span>
<span data-ttu-id="7cac5-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7cac5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cac5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cac5-123">-WhatIf</span></span>
<span data-ttu-id="7cac5-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7cac5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cac5-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7cac5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cac5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cac5-126">CommonParameters</span></span>
<span data-ttu-id="7cac5-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cac5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cac5-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cac5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cac5-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cac5-129">INPUTS</span></span>

### <span data-ttu-id="7cac5-130">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="7cac5-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="7cac5-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cac5-131">OUTPUTS</span></span>

### <span data-ttu-id="7cac5-132">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="7cac5-132">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="7cac5-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cac5-133">NOTES</span></span>

<span data-ttu-id="7cac5-134">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7cac5-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7cac5-135">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7cac5-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7cac5-136">QUOTAOBJECT <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="7cac5-136">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="7cac5-137">`[CapacityInGb <Int32?>]`: Maximal kapacitet (GB).</span><span class="sxs-lookup"><span data-stu-id="7cac5-137">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="7cac5-138">`[NumberOfStorageAccounts <Int32?>]`: Totalt antal lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="7cac5-138">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="7cac5-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cac5-139">RELATED LINKS</span></span>

