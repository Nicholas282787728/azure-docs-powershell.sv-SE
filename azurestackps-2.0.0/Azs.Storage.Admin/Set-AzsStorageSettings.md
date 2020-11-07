---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925398"
---
# <span data-ttu-id="3130f-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="3130f-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="3130f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3130f-102">SYNOPSIS</span></span>


## <span data-ttu-id="3130f-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3130f-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3130f-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3130f-104">DESCRIPTION</span></span>


## <span data-ttu-id="3130f-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3130f-105">EXAMPLES</span></span>

### <span data-ttu-id="3130f-106">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="3130f-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="3130f-107">Uppdatera lagrings inställningarna.</span><span class="sxs-lookup"><span data-stu-id="3130f-107">Update the storage settings.</span></span>

## <span data-ttu-id="3130f-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3130f-108">PARAMETERS</span></span>

### <span data-ttu-id="3130f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3130f-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="3130f-110">-Force</span><span class="sxs-lookup"><span data-stu-id="3130f-110">-Force</span></span>


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

### <span data-ttu-id="3130f-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="3130f-111">-Location</span></span>


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

### <span data-ttu-id="3130f-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="3130f-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


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

### <span data-ttu-id="3130f-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3130f-113">-SubscriptionId</span></span>


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

### <span data-ttu-id="3130f-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3130f-114">-Confirm</span></span>
<span data-ttu-id="3130f-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3130f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3130f-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3130f-116">-WhatIf</span></span>
<span data-ttu-id="3130f-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3130f-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3130f-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3130f-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3130f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3130f-119">CommonParameters</span></span>
<span data-ttu-id="3130f-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3130f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3130f-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3130f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3130f-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3130f-122">INPUTS</span></span>

## <span data-ttu-id="3130f-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3130f-123">OUTPUTS</span></span>

### <span data-ttu-id="3130f-124">Microsoft. Azure. PowerShell. cmdletar. StorageAdmin. Models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="3130f-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="3130f-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3130f-125">NOTES</span></span>

## <span data-ttu-id="3130f-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3130f-126">RELATED LINKS</span></span>

