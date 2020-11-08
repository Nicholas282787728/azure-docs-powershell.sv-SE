---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CFAA371E-F320-4FC3-80E0-5C857E5C0998
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fbb80550acb0c743a3134a315f790bc25fb793a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099757"
---
# <span data-ttu-id="07349-101">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="07349-101">Get-AzureVNetSite</span></span>

## <span data-ttu-id="07349-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07349-102">SYNOPSIS</span></span>
<span data-ttu-id="07349-103">Hämtar ett List objekt med information om virtuella Azure-nätverk.</span><span class="sxs-lookup"><span data-stu-id="07349-103">Gets a list object with information about Azure virtual networks.</span></span>

## <span data-ttu-id="07349-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07349-104">SYNTAX</span></span>

```
Get-AzureVNetSite [[-VNetName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="07349-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07349-105">DESCRIPTION</span></span>
<span data-ttu-id="07349-106">Cmdleten **Get-AzureVNetSite** hämtar ett List objekt med information om de virtuella Azure-nätverken för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="07349-106">The **Get-AzureVNetSite** cmdlet gets a list object with information about Azure virtual networks for the current subscription.</span></span>
<span data-ttu-id="07349-107">Om du anger ett virtuellt nätverks namn returneras bara information för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="07349-107">If you specify a virtual network name, only information for that virtual network is returned.</span></span>

## <span data-ttu-id="07349-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07349-108">EXAMPLES</span></span>

### <span data-ttu-id="07349-109">Exempel 1: få information om alla virtuella nätverk i det aktuella abonnemanget</span><span class="sxs-lookup"><span data-stu-id="07349-109">Example 1: Get information about all virtual networks in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite
```

<span data-ttu-id="07349-110">Det här kommandot får information om alla virtuella nätverk i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="07349-110">This command gets information about all the virtual networks in the current subscription.</span></span>

### <span data-ttu-id="07349-111">Exempel 2: Hämta information om ett specifikt virtuellt nätverk i den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="07349-111">Example 2: Get information about a specific virtual network in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite -VNetName "MyProductionNetwork"
```

<span data-ttu-id="07349-112">Det här kommandot hämtar endast information om det MyProductionNetwork virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="07349-112">This command retrieves information on the MyProductionNetwork virtual network only.</span></span>

## <span data-ttu-id="07349-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07349-113">PARAMETERS</span></span>

### <span data-ttu-id="07349-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="07349-114">-InformationAction</span></span>
<span data-ttu-id="07349-115">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="07349-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="07349-116">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="07349-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07349-117">Vidare</span><span class="sxs-lookup"><span data-stu-id="07349-117">Continue</span></span>
- <span data-ttu-id="07349-118">Över</span><span class="sxs-lookup"><span data-stu-id="07349-118">Ignore</span></span>
- <span data-ttu-id="07349-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="07349-119">Inquire</span></span>
- <span data-ttu-id="07349-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="07349-120">SilentlyContinue</span></span>
- <span data-ttu-id="07349-121">Stanna</span><span class="sxs-lookup"><span data-stu-id="07349-121">Stop</span></span>
- <span data-ttu-id="07349-122">Avbryt</span><span class="sxs-lookup"><span data-stu-id="07349-122">Suspend</span></span>

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

### <span data-ttu-id="07349-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="07349-123">-InformationVariable</span></span>
<span data-ttu-id="07349-124">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="07349-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="07349-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="07349-125">-Profile</span></span>
<span data-ttu-id="07349-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="07349-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="07349-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="07349-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="07349-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="07349-128">-VNetName</span></span>
<span data-ttu-id="07349-129">Anger ett virtuellt nätverks namn för att returnera information om.</span><span class="sxs-lookup"><span data-stu-id="07349-129">Specifies a virtual network name to return information about.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07349-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07349-130">CommonParameters</span></span>
<span data-ttu-id="07349-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07349-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07349-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07349-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07349-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07349-133">INPUTS</span></span>

## <span data-ttu-id="07349-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07349-134">OUTPUTS</span></span>

## <span data-ttu-id="07349-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07349-135">NOTES</span></span>

## <span data-ttu-id="07349-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07349-136">RELATED LINKS</span></span>

[<span data-ttu-id="07349-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="07349-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="07349-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="07349-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="07349-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="07349-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


