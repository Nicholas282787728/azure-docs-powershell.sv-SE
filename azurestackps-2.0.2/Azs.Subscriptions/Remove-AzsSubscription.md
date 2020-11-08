---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/remove-azssubscription
schema: 2.0.0
ms.openlocfilehash: b6fddf677cd619dad577b7bca8286671b85d0791
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100251"
---
# <span data-ttu-id="97040-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="97040-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="97040-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97040-102">SYNOPSIS</span></span>


## <span data-ttu-id="97040-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97040-103">SYNTAX</span></span>

### <span data-ttu-id="97040-104">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="97040-104">Delete (Default)</span></span>
```
Remove-AzsSubscription -SubscriptionId <String> [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="97040-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97040-105">DeleteViaIdentity</span></span>
```
Remove-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [-Force] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="97040-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97040-106">DESCRIPTION</span></span>


## <span data-ttu-id="97040-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97040-107">EXAMPLES</span></span>

### <span data-ttu-id="97040-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="97040-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9

```

<span data-ttu-id="97040-109">Ta bort det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="97040-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="97040-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97040-110">PARAMETERS</span></span>

### <span data-ttu-id="97040-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97040-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="97040-112">-Force</span><span class="sxs-lookup"><span data-stu-id="97040-112">-Force</span></span>


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

### <span data-ttu-id="97040-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97040-113">-InputObject</span></span>
<span data-ttu-id="97040-114">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="97040-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="97040-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97040-115">-PassThru</span></span>


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

### <span data-ttu-id="97040-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97040-116">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="97040-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="97040-117">-Confirm</span></span>
<span data-ttu-id="97040-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="97040-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97040-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97040-119">-WhatIf</span></span>
<span data-ttu-id="97040-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="97040-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97040-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="97040-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97040-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97040-122">CommonParameters</span></span>
<span data-ttu-id="97040-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97040-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97040-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97040-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97040-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97040-125">INPUTS</span></span>

### <span data-ttu-id="97040-126">Microsoft. Azure. PowerShell. cmdletar. Subscription. Models. ISubscriptionIdentity</span><span class="sxs-lookup"><span data-stu-id="97040-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="97040-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97040-127">OUTPUTS</span></span>

### <span data-ttu-id="97040-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97040-128">System.Boolean</span></span>



## <span data-ttu-id="97040-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97040-129">NOTES</span></span>

<span data-ttu-id="97040-130">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="97040-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97040-131">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97040-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="97040-132">INPUTOBJECT <ISubscriptionIdentity> :</span><span class="sxs-lookup"><span data-stu-id="97040-132">INPUTOBJECT <ISubscriptionIdentity>:</span></span> 
  - <span data-ttu-id="97040-133">`[DelegatedProviderId <String>]`: ID för den delegerade providern.</span><span class="sxs-lookup"><span data-stu-id="97040-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="97040-134">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="97040-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97040-135">`[OfferName <String>]`: Namnet på offerter.</span><span class="sxs-lookup"><span data-stu-id="97040-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="97040-136">`[SubscriptionId <String>]`: ID för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="97040-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="97040-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97040-137">RELATED LINKS</span></span>

