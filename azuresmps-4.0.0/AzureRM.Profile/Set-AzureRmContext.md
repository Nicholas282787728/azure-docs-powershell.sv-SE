---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e141e2af2dea2a07a9a64ab25c2417ffb6842837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571903"
---
# <span data-ttu-id="1efc5-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="1efc5-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="1efc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1efc5-102">SYNOPSIS</span></span>
<span data-ttu-id="1efc5-103">Anger klient organisation, prenumeration och miljö för cmdlets som ska användas i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="1efc5-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="1efc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1efc5-104">SYNTAX</span></span>

### <span data-ttu-id="1efc5-105">SubscriptionName (standard)</span><span class="sxs-lookup"><span data-stu-id="1efc5-105">SubscriptionName (Default)</span></span>
```
Set-AzureRmContext [-SubscriptionName <String>] [-TenantId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1efc5-106">Snabb</span><span class="sxs-lookup"><span data-stu-id="1efc5-106">Context</span></span>
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1efc5-107">SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1efc5-107">SubscriptionId</span></span>
```
Set-AzureRmContext [-TenantId <String>] [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1efc5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1efc5-108">DESCRIPTION</span></span>
<span data-ttu-id="1efc5-109">Med Set-AzureRmContext cmdlet anges autentiseringsinformation för de cmdlets som du kör i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="1efc5-109">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="1efc5-110">Kontexten inkluderar klient organisation, prenumeration och miljö information.</span><span class="sxs-lookup"><span data-stu-id="1efc5-110">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="1efc5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1efc5-111">EXAMPLES</span></span>

### <span data-ttu-id="1efc5-112">Exempel 1: Ange prenumerationens kontext</span><span class="sxs-lookup"><span data-stu-id="1efc5-112">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="1efc5-113">Det här kommandot anger sammanhanget för att använda den angivna prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1efc5-113">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="1efc5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1efc5-114">PARAMETERS</span></span>

### <span data-ttu-id="1efc5-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="1efc5-115">-Context</span></span>
<span data-ttu-id="1efc5-116">Anger sammanhanget för den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="1efc5-116">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1efc5-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1efc5-117">-SubscriptionId</span></span>
<span data-ttu-id="1efc5-118">Anger det prenumerations-ID för kontext som denna cmdlet ställer in för den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="1efc5-118">Specifies the subscription ID for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1efc5-119">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1efc5-119">-SubscriptionName</span></span>
<span data-ttu-id="1efc5-120">Anger prenumerations namnet för den kontext som denna cmdlet ställer in för den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="1efc5-120">Specifies the subscription name for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1efc5-121">-TenantId</span><span class="sxs-lookup"><span data-stu-id="1efc5-121">-TenantId</span></span>
<span data-ttu-id="1efc5-122">Anger ID för klient organisationen för den kontext som denna cmdlet ställer in för den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="1efc5-122">Specifies the ID of the tenant for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1efc5-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1efc5-123">-Confirm</span></span>
<span data-ttu-id="1efc5-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1efc5-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1efc5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1efc5-125">-WhatIf</span></span>
<span data-ttu-id="1efc5-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1efc5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1efc5-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1efc5-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1efc5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1efc5-128">CommonParameters</span></span>
<span data-ttu-id="1efc5-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1efc5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1efc5-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1efc5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1efc5-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1efc5-131">INPUTS</span></span>

## <span data-ttu-id="1efc5-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1efc5-132">OUTPUTS</span></span>

### <span data-ttu-id="1efc5-133">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="1efc5-133">PSAzureContext</span></span>

## <span data-ttu-id="1efc5-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1efc5-134">NOTES</span></span>

## <span data-ttu-id="1efc5-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1efc5-135">RELATED LINKS</span></span>

[<span data-ttu-id="1efc5-136">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="1efc5-136">Get-AzureRMContext</span></span>]()

