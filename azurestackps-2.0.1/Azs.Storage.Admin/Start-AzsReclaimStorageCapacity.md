---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092881"
---
# <span data-ttu-id="e311f-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="e311f-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="e311f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e311f-102">SYNOPSIS</span></span>


## <span data-ttu-id="e311f-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e311f-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e311f-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e311f-104">DESCRIPTION</span></span>


## <span data-ttu-id="e311f-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e311f-105">EXAMPLES</span></span>

### <span data-ttu-id="e311f-106">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="e311f-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="e311f-107">Starta skräp insamling.</span><span class="sxs-lookup"><span data-stu-id="e311f-107">Start garbage collection.</span></span>

## <span data-ttu-id="e311f-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e311f-108">PARAMETERS</span></span>

### <span data-ttu-id="e311f-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e311f-109">-AsJob</span></span>


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

### <span data-ttu-id="e311f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e311f-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="e311f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e311f-111">-Force</span></span>


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

### <span data-ttu-id="e311f-112">-Plats</span><span class="sxs-lookup"><span data-stu-id="e311f-112">-Location</span></span>


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

### <span data-ttu-id="e311f-113">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e311f-113">-NoWait</span></span>


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

### <span data-ttu-id="e311f-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e311f-114">-PassThru</span></span>


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

### <span data-ttu-id="e311f-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e311f-115">-SubscriptionId</span></span>


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

### <span data-ttu-id="e311f-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e311f-116">-Confirm</span></span>
<span data-ttu-id="e311f-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e311f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e311f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e311f-118">-WhatIf</span></span>
<span data-ttu-id="e311f-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e311f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e311f-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e311f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e311f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e311f-121">CommonParameters</span></span>
<span data-ttu-id="e311f-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e311f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e311f-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e311f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e311f-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e311f-124">INPUTS</span></span>

## <span data-ttu-id="e311f-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e311f-125">OUTPUTS</span></span>

### <span data-ttu-id="e311f-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e311f-126">System.Boolean</span></span>



## <span data-ttu-id="e311f-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e311f-127">NOTES</span></span>

## <span data-ttu-id="e311f-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e311f-128">RELATED LINKS</span></span>

