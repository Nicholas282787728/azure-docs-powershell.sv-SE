---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 75320133-E7B1-40D4-B16D-567686D5AE99
online version: ''
schema: 2.0.0
ms.openlocfilehash: 40d3bdc73ce6bcbb199cf99bb0586de52f05e132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099217"
---
# <span data-ttu-id="51389-101">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="51389-101">New-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="51389-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51389-102">SYNOPSIS</span></span>
<span data-ttu-id="51389-103">Skapar en ny Service Bus-auktoriseringsregel.</span><span class="sxs-lookup"><span data-stu-id="51389-103">Creates new Service Bus authorization rule.</span></span>

## <span data-ttu-id="51389-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51389-104">SYNTAX</span></span>

### <span data-ttu-id="51389-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="51389-105">EntitySAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="51389-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="51389-106">NamespaceSAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="51389-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51389-107">DESCRIPTION</span></span>
<span data-ttu-id="51389-108">Cmdleten **New-AzureSBAuthorizationRule** skapar en Service Bus-auktoriseringsregel.</span><span class="sxs-lookup"><span data-stu-id="51389-108">The **New-AzureSBAuthorizationRule** cmdlet creates a Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="51389-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51389-109">EXAMPLES</span></span>

### <span data-ttu-id="51389-110">Exempel 1: skapa en auktoriseringsregel med genererad primär Key</span><span class="sxs-lookup"><span data-stu-id="51389-110">Example 1: Create an authorization rule with generated primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="51389-111">Skapar en ny auktoriseringsregel på namn områdes nivå med Send-behörighet.</span><span class="sxs-lookup"><span data-stu-id="51389-111">Creates new authorization rule on namespace level with Send permission.</span></span>

### <span data-ttu-id="51389-112">Exempel 2: skapar en auktoriseringsregel genom att ange primär nycklar</span><span class="sxs-lookup"><span data-stu-id="51389-112">Example 2: Creates an authorization rule by providing the primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Manage", "Listen", "Send") -EntityName MyEntity -EntityType Queue -PrimaryKey P+lL/Mnd2Z9sj5hwMrRyAxQDdX8RHfbdqU2eIAqs1rc=
```

<span data-ttu-id="51389-113">Skapar en ny auktoriseringsregel på kön med alla behörigheter.</span><span class="sxs-lookup"><span data-stu-id="51389-113">Creates new authorization rule on MyEntity Queue level with all permissions.</span></span>

## <span data-ttu-id="51389-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51389-114">PARAMETERS</span></span>

### <span data-ttu-id="51389-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="51389-115">-EntityName</span></span>
<span data-ttu-id="51389-116">Anger entitetsnamnet som regeln ska tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="51389-116">Specifies the entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51389-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="51389-117">-EntityType</span></span>
<span data-ttu-id="51389-118">Anger entitetstypen.</span><span class="sxs-lookup"><span data-stu-id="51389-118">Specifies the entity type.</span></span>
<span data-ttu-id="51389-119">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="51389-119">Valid values are:</span></span>
  
- <span data-ttu-id="51389-120">Svarskö</span><span class="sxs-lookup"><span data-stu-id="51389-120">Queue</span></span>
- <span data-ttu-id="51389-121">Ämnes</span><span class="sxs-lookup"><span data-stu-id="51389-121">Topic</span></span>
- <span data-ttu-id="51389-122">Relayrouter</span><span class="sxs-lookup"><span data-stu-id="51389-122">Relay</span></span>
- <span data-ttu-id="51389-123">NotificationHub</span><span class="sxs-lookup"><span data-stu-id="51389-123">NotificationHub</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51389-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="51389-124">-Name</span></span>
<span data-ttu-id="51389-125">Anger namnet på den unika auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="51389-125">Specifies the unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51389-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="51389-126">-Namespace</span></span>
<span data-ttu-id="51389-127">Anger namn området för att tillämpa auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="51389-127">Specifies the namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="51389-128">Om inget *EntityName* anges kommer regeln att finnas på namn områdes nivån.</span><span class="sxs-lookup"><span data-stu-id="51389-128">If no *EntityName* provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="51389-129">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="51389-129">-Permission</span></span>
<span data-ttu-id="51389-130">Behörighets behörigheter (skicka, hantera, lyssna).</span><span class="sxs-lookup"><span data-stu-id="51389-130">The authorization permissions (Send, Manage, Listen).</span></span>

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

### <span data-ttu-id="51389-131">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="51389-131">-PrimaryKey</span></span>
<span data-ttu-id="51389-132">Anger primär nycklarna för signaturen för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="51389-132">Specifies the Shared Access Signature primary key.</span></span>
<span data-ttu-id="51389-133">Kommer att genereras om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="51389-133">Will be generated if not provided.</span></span>

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

### <span data-ttu-id="51389-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="51389-134">-Profile</span></span>
<span data-ttu-id="51389-135">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="51389-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51389-136">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="51389-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51389-137">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="51389-137">-SecondaryKey</span></span>
<span data-ttu-id="51389-138">Anger den sekundära tangenten för signaturen för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="51389-138">Specifies the Shared Access Signature secondary key.</span></span>

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

### <span data-ttu-id="51389-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51389-139">CommonParameters</span></span>
<span data-ttu-id="51389-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51389-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51389-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51389-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51389-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51389-142">INPUTS</span></span>

## <span data-ttu-id="51389-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51389-143">OUTPUTS</span></span>

## <span data-ttu-id="51389-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51389-144">NOTES</span></span>

## <span data-ttu-id="51389-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51389-145">RELATED LINKS</span></span>

[<span data-ttu-id="51389-146">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="51389-146">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="51389-147">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="51389-147">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="51389-148">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="51389-148">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


