---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 17065902-97EA-4F5F-926B-B7CBEE3EAF84
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab76cf3052f28b0ff89e3e41aaa08127cc33411e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099050"
---
# <span data-ttu-id="ce3ac-101">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ce3ac-101">Set-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="ce3ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce3ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ce3ac-103">Uppdaterar en befintlig Service Bus-auktoriseringsregel.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-103">Updates existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="ce3ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce3ac-104">SYNTAX</span></span>

### <span data-ttu-id="ce3ac-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="ce3ac-105">EntitySAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ce3ac-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="ce3ac-106">NamespaceSAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ce3ac-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce3ac-107">DESCRIPTION</span></span>
<span data-ttu-id="ce3ac-108">Uppdaterar en befintlig Service Bus-auktoriseringsregel.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-108">Updates existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="ce3ac-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce3ac-109">EXAMPLES</span></span>

### <span data-ttu-id="ce3ac-110">Exempel 1: förnya primärt för auktoriseringsregeln på namn områdes nivå</span><span class="sxs-lookup"><span data-stu-id="ce3ac-110">Example 1: Renew primary key for authorization rule at namespace level</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="ce3ac-111">Primär nycklarna förnyas.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-111">The primary key is renewed.</span></span>

### <span data-ttu-id="ce3ac-112">Exempel 2: behörigheten Uppdatera auktoriseringsregel</span><span class="sxs-lookup"><span data-stu-id="ce3ac-112">Example 2: Update authorization rule permission</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Listen", "Send") -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="ce3ac-113">Uppdaterar behörigheterna.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-113">Updates the permissions.</span></span>

## <span data-ttu-id="ce3ac-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce3ac-114">PARAMETERS</span></span>

### <span data-ttu-id="ce3ac-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="ce3ac-115">-EntityName</span></span>
<span data-ttu-id="ce3ac-116">Entitetsnamnet som regeln ska tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="ce3ac-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="ce3ac-117">-EntityType</span></span>
<span data-ttu-id="ce3ac-118">Entitetstypen (kö, ämne, relä, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="ce3ac-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="ce3ac-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ce3ac-119">-Name</span></span>
<span data-ttu-id="ce3ac-120">Namnet på den unika auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="ce3ac-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ce3ac-121">-Namespace</span></span>
<span data-ttu-id="ce3ac-122">Namn områdes namnet som används för auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="ce3ac-123">Om inget EntityName anges kommer regeln att finnas på namn områdes nivån.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="ce3ac-124">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="ce3ac-124">-Permission</span></span>
<span data-ttu-id="ce3ac-125">Behörighets behörigheter (skicka, hantera, lyssna).</span><span class="sxs-lookup"><span data-stu-id="ce3ac-125">The authorization permissions (Send, Manage, Listen).</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3ac-126">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ce3ac-126">-PrimaryKey</span></span>
<span data-ttu-id="ce3ac-127">Den delade Access-signaturens primär nycklar.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-127">The Shared Access Signature primary key.</span></span>
<span data-ttu-id="ce3ac-128">Kommer att genereras om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-128">Will be generated if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3ac-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="ce3ac-129">-Profile</span></span>
<span data-ttu-id="ce3ac-130">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ce3ac-131">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ce3ac-132">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="ce3ac-132">-SecondaryKey</span></span>
<span data-ttu-id="ce3ac-133">Sekundär nycklarna för signaturen för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-133">The Shared Access Signature secondary key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3ac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce3ac-134">CommonParameters</span></span>
<span data-ttu-id="ce3ac-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce3ac-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce3ac-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce3ac-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce3ac-137">INPUTS</span></span>

## <span data-ttu-id="ce3ac-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce3ac-138">OUTPUTS</span></span>

## <span data-ttu-id="ce3ac-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce3ac-139">NOTES</span></span>

## <span data-ttu-id="ce3ac-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce3ac-140">RELATED LINKS</span></span>

[<span data-ttu-id="ce3ac-141">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ce3ac-141">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="ce3ac-142">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ce3ac-142">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="ce3ac-143">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ce3ac-143">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)


