---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/25/2020
ms.locfileid: "94093115"
---
# <span data-ttu-id="5b519-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="5b519-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="5b519-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5b519-102">SYNOPSIS</span></span>


## <span data-ttu-id="5b519-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5b519-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5b519-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5b519-104">DESCRIPTION</span></span>


## <span data-ttu-id="5b519-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5b519-105">EXAMPLES</span></span>

### <span data-ttu-id="5b519-106">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="5b519-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="5b519-107">Uppdatera lagrings inställningarna.</span><span class="sxs-lookup"><span data-stu-id="5b519-107">Update the storage settings.</span></span>

## <span data-ttu-id="5b519-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5b519-108">PARAMETERS</span></span>

### <span data-ttu-id="5b519-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b519-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="5b519-110">-Force</span><span class="sxs-lookup"><span data-stu-id="5b519-110">-Force</span></span>


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

### <span data-ttu-id="5b519-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="5b519-111">-Location</span></span>


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

### <span data-ttu-id="5b519-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="5b519-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5b519-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b519-113">-SubscriptionId</span></span>


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

### <span data-ttu-id="5b519-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5b519-114">-Confirm</span></span>
<span data-ttu-id="5b519-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5b519-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b519-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b519-116">-WhatIf</span></span>
<span data-ttu-id="5b519-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5b519-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b519-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5b519-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b519-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b519-119">CommonParameters</span></span>
<span data-ttu-id="5b519-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b519-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b519-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b519-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b519-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5b519-122">INPUTS</span></span>

## <span data-ttu-id="5b519-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5b519-123">OUTPUTS</span></span>

### <span data-ttu-id="5b519-124">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="5b519-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="5b519-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5b519-125">NOTES</span></span>

## <span data-ttu-id="5b519-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5b519-126">RELATED LINKS</span></span>

