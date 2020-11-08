---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7B2CDFF-D9A2-48C7-B331-132A6A6843CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 10fdb8920164857b42ac57a3c989417c2a967ab9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093340"
---
# <span data-ttu-id="00505-101">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="00505-101">Get-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="00505-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00505-102">SYNOPSIS</span></span>
<span data-ttu-id="00505-103">Hämtar Service Bus-auktoriseringsregler.</span><span class="sxs-lookup"><span data-stu-id="00505-103">Gets Service bus authorization rules.</span></span>


## <span data-ttu-id="00505-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00505-104">SYNTAX</span></span>

### <span data-ttu-id="00505-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="00505-105">EntitySAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="00505-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="00505-106">NamespaceSAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="00505-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00505-107">DESCRIPTION</span></span>
<span data-ttu-id="00505-108">Hämtar Service Bus-auktoriseringsregler.</span><span class="sxs-lookup"><span data-stu-id="00505-108">Gets Service bus authorization rules.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="00505-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00505-109">EXAMPLES</span></span>

### <span data-ttu-id="00505-110">Exempel 1: Hämta auktoriseringsregel på namn områdes nivå</span><span class="sxs-lookup"><span data-stu-id="00505-110">Example 1: Get authorization rule at namespace level</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace
```

<span data-ttu-id="00505-111">Hämtar alla tillgängliga auktoriseringsregler vid ett namn område.</span><span class="sxs-lookup"><span data-stu-id="00505-111">Gets all available authorization rules at MyNamespace.</span></span>

### <span data-ttu-id="00505-112">Exempel 2: Hämta auktoriseringsregel för en kö</span><span class="sxs-lookup"><span data-stu-id="00505-112">Example 2: Get authorization rule for a Queue</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="00505-113">Hämtar alla tillgängliga auktoriseringsregler en kö för mina enheter i ett namn område.</span><span class="sxs-lookup"><span data-stu-id="00505-113">Gets all available authorization rules a MyEntity Queue on MyNamespace.</span></span>

### <span data-ttu-id="00505-114">Exempel 3: Hämta auktoriseringsregel efter namn</span><span class="sxs-lookup"><span data-stu-id="00505-114">Example 3: Get authorization rule by name</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="00505-115">Hämtar en auktoriseringsregel som heter min regel på en bevarad nivå.</span><span class="sxs-lookup"><span data-stu-id="00505-115">Gets an authorization rule called MyRule on MyNamespace level.</span></span>

### <span data-ttu-id="00505-116">Exempel 4: Hämta auktoriseringsregel efter behörighet</span><span class="sxs-lookup"><span data-stu-id="00505-116">Example 4: Get authorization rule by permission</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="00505-117">Hämtar alla auktoriseringsregler som har behörigheten skicka på namn områdes nivån.</span><span class="sxs-lookup"><span data-stu-id="00505-117">Gets all authorization rules that have send permission on namespace level.</span></span>

## <span data-ttu-id="00505-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00505-118">PARAMETERS</span></span>

### <span data-ttu-id="00505-119">-EntityName</span><span class="sxs-lookup"><span data-stu-id="00505-119">-EntityName</span></span>
<span data-ttu-id="00505-120">Entitetsnamnet som regeln ska tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="00505-120">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="00505-121">-EntityType</span><span class="sxs-lookup"><span data-stu-id="00505-121">-EntityType</span></span>
<span data-ttu-id="00505-122">Entitetstypen (kö, ämne, relä, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="00505-122">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="00505-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="00505-123">-Name</span></span>
<span data-ttu-id="00505-124">Namnet på den unika auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="00505-124">The unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00505-125">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="00505-125">-Namespace</span></span>
<span data-ttu-id="00505-126">Namn områdes namnet som används för auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="00505-126">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="00505-127">Om inget EntityName anges kommer regeln att finnas på namn områdes nivån.</span><span class="sxs-lookup"><span data-stu-id="00505-127">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="00505-128">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="00505-128">-Permission</span></span>
<span data-ttu-id="00505-129">Behörighet att filtrera (skicka, hantera, lyssna).</span><span class="sxs-lookup"><span data-stu-id="00505-129">The authorization permissions to filter (Send, Manage, Listen).</span></span>
<span data-ttu-id="00505-130">Detta använder exakt matchning.</span><span class="sxs-lookup"><span data-stu-id="00505-130">This uses exact match.</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00505-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="00505-131">-Profile</span></span>
<span data-ttu-id="00505-132">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="00505-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="00505-133">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="00505-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="00505-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00505-134">CommonParameters</span></span>
<span data-ttu-id="00505-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00505-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00505-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00505-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00505-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00505-137">INPUTS</span></span>

## <span data-ttu-id="00505-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00505-138">OUTPUTS</span></span>

## <span data-ttu-id="00505-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00505-139">NOTES</span></span>

## <span data-ttu-id="00505-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00505-140">RELATED LINKS</span></span>

[<span data-ttu-id="00505-141">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="00505-141">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="00505-142">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="00505-142">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="00505-143">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="00505-143">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


