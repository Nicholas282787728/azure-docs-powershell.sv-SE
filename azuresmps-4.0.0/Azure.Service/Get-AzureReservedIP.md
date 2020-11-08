---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C0EEC51F-F8AB-4A6C-8F99-2B2DFFE9BB26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b5f4d5319e705c4f0481edcb5a44a579f4ff01d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093344"
---
# <span data-ttu-id="80321-101">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="80321-101">Get-AzureReservedIP</span></span>

## <span data-ttu-id="80321-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80321-102">SYNOPSIS</span></span>
<span data-ttu-id="80321-103">Hämtar en reserverad IP-adress utifrån dess namn eller listar alla reserverade IP-adresser i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="80321-103">Gets a reserved IP address by its name or lists all the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="80321-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80321-104">SYNTAX</span></span>

```
Get-AzureReservedIP [[-ReservedIPName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="80321-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80321-105">DESCRIPTION</span></span>
<span data-ttu-id="80321-106">Cmdleten **Get-AzureReservedIP** hämtar en reserverad IP-adress efter namnet eller listar alla reserverade IP-adresser i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="80321-106">The **Get-AzureReservedIP** cmdlet gets a reserved IP address by its name or lists all of the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="80321-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80321-107">EXAMPLES</span></span>

### <span data-ttu-id="80321-108">Exempel 1: Hämta alla reserverade IP-adresser</span><span class="sxs-lookup"><span data-stu-id="80321-108">Example 1: Get all reserved IP addresses</span></span>
```
PS C:\> Get-AzureReservedIP
```

<span data-ttu-id="80321-109">Det här kommandot får alla reserverade IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="80321-109">This command gets all reserved IP addresses.</span></span>

### <span data-ttu-id="80321-110">Exempel 2: Hämta en reserverad IP-adress med ett angivet namn</span><span class="sxs-lookup"><span data-stu-id="80321-110">Example 2: Get a reserved IP address with a specified name</span></span>
```
PS C:\> Get-AzureReservedIP -ReservedIPName $IpName
```

<span data-ttu-id="80321-111">Det här kommandot får den reserverade IP-adressen som har namnet som anges av variabeln $IpName.</span><span class="sxs-lookup"><span data-stu-id="80321-111">This command gets the reserved IP address that has the name specified by the $IpName variable.</span></span>

## <span data-ttu-id="80321-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80321-112">PARAMETERS</span></span>

### <span data-ttu-id="80321-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="80321-113">-InformationAction</span></span>
<span data-ttu-id="80321-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="80321-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="80321-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="80321-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80321-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="80321-116">Continue</span></span>
- <span data-ttu-id="80321-117">Över</span><span class="sxs-lookup"><span data-stu-id="80321-117">Ignore</span></span>
- <span data-ttu-id="80321-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="80321-118">Inquire</span></span>
- <span data-ttu-id="80321-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="80321-119">SilentlyContinue</span></span>
- <span data-ttu-id="80321-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="80321-120">Stop</span></span>
- <span data-ttu-id="80321-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="80321-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80321-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="80321-122">-InformationVariable</span></span>
<span data-ttu-id="80321-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="80321-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80321-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="80321-124">-Profile</span></span>
<span data-ttu-id="80321-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="80321-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80321-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="80321-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80321-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="80321-127">-ReservedIPName</span></span>
<span data-ttu-id="80321-128">Anger det reserverade IP-namnet.</span><span class="sxs-lookup"><span data-stu-id="80321-128">Specifies the reserved IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80321-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80321-129">CommonParameters</span></span>
<span data-ttu-id="80321-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80321-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80321-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80321-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80321-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80321-132">INPUTS</span></span>

## <span data-ttu-id="80321-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80321-133">OUTPUTS</span></span>

## <span data-ttu-id="80321-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80321-134">NOTES</span></span>

## <span data-ttu-id="80321-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80321-135">RELATED LINKS</span></span>

[<span data-ttu-id="80321-136">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="80321-136">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="80321-137">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="80321-137">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


