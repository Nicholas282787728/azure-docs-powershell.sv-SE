---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E246C177-EAEE-4D7A-A544-664F47862FC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92d450a10628ea7e85a49962ac262d4dece8e4c8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099361"
---
# <span data-ttu-id="d905e-101">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d905e-101">Remove-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="d905e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d905e-102">SYNOPSIS</span></span>
<span data-ttu-id="d905e-103">Tar bort den befintliga Service Bus-auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="d905e-103">Removes existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="d905e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d905e-104">SYNTAX</span></span>

### <span data-ttu-id="d905e-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="d905e-105">EntitySAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> -EntityName <String>
 -EntityType <ServiceBusEntityType> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d905e-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="d905e-106">NamespaceSAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d905e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d905e-107">DESCRIPTION</span></span>
<span data-ttu-id="d905e-108">Tar bort den befintliga Service Bus-auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="d905e-108">Removes existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="d905e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d905e-109">EXAMPLES</span></span>

### <span data-ttu-id="d905e-110">Exempel 1: ta bort auktoriseringsregel på namn områdes nivå</span><span class="sxs-lookup"><span data-stu-id="d905e-110">Example 1: Remove authorization rule at namespace level</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="d905e-111">Tar bort regeln för auktoriseringsregler från ett namn område.</span><span class="sxs-lookup"><span data-stu-id="d905e-111">Removes authorization rule MyRule from MyNamespace.</span></span>

### <span data-ttu-id="d905e-112">Exempel 2: ta bort en auktoriseringsregel för en kö</span><span class="sxs-lookup"><span data-stu-id="d905e-112">Example 2: Remove authorization rule for a Queue</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="d905e-113">Tar bort auktoriseringsregeln som heter min regel för en kö för mina enheter i ett namn område.</span><span class="sxs-lookup"><span data-stu-id="d905e-113">Removes authorization rule called MyRule for a MyEntity Queue on MyNamespace.</span></span>

## <span data-ttu-id="d905e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d905e-114">PARAMETERS</span></span>

### <span data-ttu-id="d905e-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="d905e-115">-EntityName</span></span>
<span data-ttu-id="d905e-116">Entitetsnamnet som regeln ska tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="d905e-116">The entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905e-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="d905e-117">-EntityType</span></span>
<span data-ttu-id="d905e-118">Entitetstypen (kö, ämne, relä, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="d905e-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d905e-119">-Name</span></span>
<span data-ttu-id="d905e-120">Namnet på den unika auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="d905e-120">The unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905e-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="d905e-121">-Namespace</span></span>
<span data-ttu-id="d905e-122">Namn områdes namnet som används för auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="d905e-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="d905e-123">Om inget EntityName anges kommer regeln att finnas på namn områdes nivån.</span><span class="sxs-lookup"><span data-stu-id="d905e-123">If no EntityName provided the rule will be on the namespace level.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d905e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d905e-124">-PassThru</span></span>
<span data-ttu-id="d905e-125">Anger att den här cmdleten returnerar ett objekt som representerar det objekt som den körs på.</span><span class="sxs-lookup"><span data-stu-id="d905e-125">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="d905e-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d905e-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d905e-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="d905e-127">-Profile</span></span>
<span data-ttu-id="d905e-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d905e-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d905e-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d905e-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d905e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d905e-130">CommonParameters</span></span>
<span data-ttu-id="d905e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d905e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d905e-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d905e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d905e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d905e-133">INPUTS</span></span>

## <span data-ttu-id="d905e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d905e-134">OUTPUTS</span></span>

## <span data-ttu-id="d905e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d905e-135">NOTES</span></span>

## <span data-ttu-id="d905e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d905e-136">RELATED LINKS</span></span>

[<span data-ttu-id="d905e-137">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d905e-137">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="d905e-138">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d905e-138">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="d905e-139">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d905e-139">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


