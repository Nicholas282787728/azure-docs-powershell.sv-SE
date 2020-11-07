---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/new-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: bd97eff2a0ed37c309ad0b50927f8231a2da27a6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925402"
---
# <span data-ttu-id="c743e-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="c743e-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="c743e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c743e-102">SYNOPSIS</span></span>


## <span data-ttu-id="c743e-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c743e-103">SYNTAX</span></span>

### <span data-ttu-id="c743e-104">CreateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="c743e-104">CreateExpanded (Default)</span></span>
```
New-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c743e-105">Göra</span><span class="sxs-lookup"><span data-stu-id="c743e-105">Create</span></span>
```
New-AzsStorageQuota -Name <String> -QuotaObject <IStorageQuota> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c743e-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c743e-106">DESCRIPTION</span></span>


## <span data-ttu-id="c743e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c743e-107">EXAMPLES</span></span>

### <span data-ttu-id="c743e-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="c743e-108">Example 1:</span></span>
```powershell
PS C:\> New-AzsStorageQuota -Name TestQuota -CapacityInGb 123 -NumberOfStorageAccounts 456
```

<span data-ttu-id="c743e-109">Skapa en ny lagrings kvot med angivna värden.</span><span class="sxs-lookup"><span data-stu-id="c743e-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="c743e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c743e-110">PARAMETERS</span></span>

### <span data-ttu-id="c743e-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="c743e-111">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c743e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c743e-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="c743e-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="c743e-113">-Location</span></span>


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

### <span data-ttu-id="c743e-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="c743e-114">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c743e-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="c743e-115">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c743e-116">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="c743e-116">-QuotaObject</span></span>
<span data-ttu-id="c743e-117">För att konstruera kan du läsa avsnittet anteckningar för QUOTAOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c743e-117">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c743e-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c743e-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="c743e-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c743e-119">-Confirm</span></span>
<span data-ttu-id="c743e-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c743e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c743e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c743e-121">-WhatIf</span></span>
<span data-ttu-id="c743e-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c743e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c743e-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c743e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c743e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c743e-124">CommonParameters</span></span>
<span data-ttu-id="c743e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c743e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c743e-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c743e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c743e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c743e-127">INPUTS</span></span>

### <span data-ttu-id="c743e-128">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="c743e-128">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="c743e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c743e-129">OUTPUTS</span></span>

### <span data-ttu-id="c743e-130">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="c743e-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="c743e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c743e-131">NOTES</span></span>

<span data-ttu-id="c743e-132">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="c743e-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c743e-133">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c743e-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c743e-134">QUOTAOBJECT <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="c743e-134">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="c743e-135">`[CapacityInGb <Int32?>]`: Maximal kapacitet (GB).</span><span class="sxs-lookup"><span data-stu-id="c743e-135">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="c743e-136">`[NumberOfStorageAccounts <Int32?>]`: Totalt antal lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="c743e-136">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="c743e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c743e-137">RELATED LINKS</span></span>

