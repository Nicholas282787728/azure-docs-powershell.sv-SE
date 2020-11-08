---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D08CB0A0-A0A9-4E0A-B1AB-A19A655B501B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5fd66813dcfc08f5e2f5276c4019443f9166945d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093322"
---
# <span data-ttu-id="89393-101">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="89393-101">Get-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="89393-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89393-102">SYNOPSIS</span></span>
<span data-ttu-id="89393-103">Den här cmdleten får tillägget fjärr skrivbord för moln tjänsten installerat på alla roller eller med namngivna roller på en viss distributions plats.</span><span class="sxs-lookup"><span data-stu-id="89393-103">This cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="89393-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89393-104">SYNTAX</span></span>

```
Get-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="89393-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89393-105">DESCRIPTION</span></span>
<span data-ttu-id="89393-106">Cmdleten **Get-AzureServiceRemoteDesktopExtension** får till gång till moln tjänstens fil namns tillägg på alla roller eller med namngivna roller på en viss distributions plats.</span><span class="sxs-lookup"><span data-stu-id="89393-106">The **Get-AzureServiceRemoteDesktopExtension** cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="89393-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89393-107">EXAMPLES</span></span>

### <span data-ttu-id="89393-108">Exempel 1: Hämta fjärr skrivbords tillägget för den angivna tjänsten</span><span class="sxs-lookup"><span data-stu-id="89393-108">Example 1: Get remote desktop extension for the specified service</span></span>
```
PS C:\> Get-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="89393-109">Det här kommandot får tillägget fjärr skrivbord för den angivna tjänsten.</span><span class="sxs-lookup"><span data-stu-id="89393-109">This command gets the remote desktop extension for the specified service.</span></span>

## <span data-ttu-id="89393-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89393-110">PARAMETERS</span></span>

### <span data-ttu-id="89393-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="89393-111">-InformationAction</span></span>
<span data-ttu-id="89393-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="89393-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="89393-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="89393-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89393-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="89393-114">Continue</span></span>
- <span data-ttu-id="89393-115">Över</span><span class="sxs-lookup"><span data-stu-id="89393-115">Ignore</span></span>
- <span data-ttu-id="89393-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="89393-116">Inquire</span></span>
- <span data-ttu-id="89393-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="89393-117">SilentlyContinue</span></span>
- <span data-ttu-id="89393-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="89393-118">Stop</span></span>
- <span data-ttu-id="89393-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="89393-119">Suspend</span></span>

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

### <span data-ttu-id="89393-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="89393-120">-InformationVariable</span></span>
<span data-ttu-id="89393-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="89393-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="89393-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="89393-122">-Profile</span></span>
<span data-ttu-id="89393-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="89393-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89393-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="89393-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89393-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="89393-125">-ServiceName</span></span>
<span data-ttu-id="89393-126">Anger namnet på distributionen av Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="89393-126">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="89393-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="89393-127">-Slot</span></span>
<span data-ttu-id="89393-128">Anger miljön för distributionen som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="89393-128">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="89393-129">De acceptabla värdena för denna parameter är: produktion eller mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="89393-129">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89393-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89393-130">CommonParameters</span></span>
<span data-ttu-id="89393-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89393-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89393-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89393-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89393-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89393-133">INPUTS</span></span>

## <span data-ttu-id="89393-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89393-134">OUTPUTS</span></span>

## <span data-ttu-id="89393-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89393-135">NOTES</span></span>

## <span data-ttu-id="89393-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89393-136">RELATED LINKS</span></span>

[<span data-ttu-id="89393-137">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="89393-137">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


