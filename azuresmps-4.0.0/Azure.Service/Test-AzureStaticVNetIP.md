---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E059EF1-740C-4AEB-AF41-BF6003BE15F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: a52f2585771ec10d6acf52b14c88bd1ed0af0427
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099166"
---
# <span data-ttu-id="91c09-101">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="91c09-101">Test-AzureStaticVNetIP</span></span>

## <span data-ttu-id="91c09-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91c09-102">SYNOPSIS</span></span>
<span data-ttu-id="91c09-103">Testar tillgänglighet för en statisk virtuell nätverks-IP-adress och får en lista med förslag om den efterfrågade adressen inte är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="91c09-103">Tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="91c09-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91c09-104">SYNTAX</span></span>

```
Test-AzureStaticVNetIP [-VNetName] <String> [-IPAddress] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="91c09-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91c09-105">DESCRIPTION</span></span>
<span data-ttu-id="91c09-106">**Test-AzureStaticVNetIP** cmdlet testar tillgänglighet för en statisk virtuell nätverks-IP-adress och får en lista med förslag om den efterfrågade adressen inte är tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="91c09-106">The **Test-AzureStaticVNetIP** cmdlet tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="91c09-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91c09-107">EXAMPLES</span></span>

### <span data-ttu-id="91c09-108">9.1</span><span class="sxs-lookup"><span data-stu-id="91c09-108">1:</span></span>
```

```

## <span data-ttu-id="91c09-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91c09-109">PARAMETERS</span></span>

### <span data-ttu-id="91c09-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="91c09-110">-InformationAction</span></span>
<span data-ttu-id="91c09-111">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="91c09-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="91c09-112">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="91c09-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91c09-113">Vidare</span><span class="sxs-lookup"><span data-stu-id="91c09-113">Continue</span></span>
- <span data-ttu-id="91c09-114">Över</span><span class="sxs-lookup"><span data-stu-id="91c09-114">Ignore</span></span>
- <span data-ttu-id="91c09-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="91c09-115">Inquire</span></span>
- <span data-ttu-id="91c09-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="91c09-116">SilentlyContinue</span></span>
- <span data-ttu-id="91c09-117">Stanna</span><span class="sxs-lookup"><span data-stu-id="91c09-117">Stop</span></span>
- <span data-ttu-id="91c09-118">Avbryt</span><span class="sxs-lookup"><span data-stu-id="91c09-118">Suspend</span></span>

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

### <span data-ttu-id="91c09-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="91c09-119">-InformationVariable</span></span>
<span data-ttu-id="91c09-120">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="91c09-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="91c09-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="91c09-121">-IPAddress</span></span>
<span data-ttu-id="91c09-122">Anger det statiska virtuella nätverks-IP-adressen som ska frågas.</span><span class="sxs-lookup"><span data-stu-id="91c09-122">Specifies the static virtual network IP address to query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c09-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="91c09-123">-Profile</span></span>
<span data-ttu-id="91c09-124">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="91c09-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="91c09-125">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="91c09-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="91c09-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="91c09-126">-VNetName</span></span>
<span data-ttu-id="91c09-127">Anger namnet på det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="91c09-127">Specifies the Name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c09-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c09-128">CommonParameters</span></span>
<span data-ttu-id="91c09-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c09-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c09-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91c09-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c09-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91c09-131">INPUTS</span></span>

## <span data-ttu-id="91c09-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91c09-132">OUTPUTS</span></span>

## <span data-ttu-id="91c09-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91c09-133">NOTES</span></span>

## <span data-ttu-id="91c09-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91c09-134">RELATED LINKS</span></span>

[<span data-ttu-id="91c09-135">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="91c09-135">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="91c09-136">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="91c09-136">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


