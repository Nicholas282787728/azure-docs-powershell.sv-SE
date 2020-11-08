---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F34910FA-B024-4C1C-B040-671C8962C49D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 558d714c432efd1dbd8f11feb09b0bbde035e2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099518"
---
# <span data-ttu-id="1e680-101">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="1e680-101">Get-AzureVNetConfig</span></span>

## <span data-ttu-id="1e680-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e680-102">SYNOPSIS</span></span>
<span data-ttu-id="1e680-103">Hämtar Azure Virtual Network-konfigurationen från det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1e680-103">Gets the Azure virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="1e680-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e680-104">SYNTAX</span></span>

```
Get-AzureVNetConfig [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1e680-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e680-105">DESCRIPTION</span></span>
<span data-ttu-id="1e680-106">Cmdleten **Get-AzureVNetConfig** hämtar den virtuella nätverks konfigurationen för det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1e680-106">The **Get-AzureVNetConfig** cmdlet retrieves the virtual network configuration of the current Azure subscription.</span></span>
<span data-ttu-id="1e680-107">Om parametern *ExportToFile* anges skapas en nätverks konfigurations fil.</span><span class="sxs-lookup"><span data-stu-id="1e680-107">If the *ExportToFile* parameter is specified, a network configuration file is created.</span></span>

## <span data-ttu-id="1e680-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e680-108">EXAMPLES</span></span>

### <span data-ttu-id="1e680-109">Exempel 1: Hämta virtuell nätverks konfiguration för ett nuvarande Azure-abonnemang</span><span class="sxs-lookup"><span data-stu-id="1e680-109">Example 1: Get the virtual network configuration of a current Azure subscription</span></span>
```
PS C:\> Get-AzureVNetConfig
```

<span data-ttu-id="1e680-110">Det här kommandot får den virtuella nätverks konfigurationen för det aktuella Azure-abonnemanget och visar det.</span><span class="sxs-lookup"><span data-stu-id="1e680-110">This command gets the virtual network configuration of the current Azure subscription and displays it.</span></span>

### <span data-ttu-id="1e680-111">Exempel 2: hämta den virtuella nätverks konfigurationen för det aktuella Azure-abonnemanget och spara den i en lokal fil</span><span class="sxs-lookup"><span data-stu-id="1e680-111">Example 2: Get the virtual network configuration of the current Azure subscription and save it to a local file</span></span>
```
PS C:\> Get-AzureVNetConfig -ExportToFile "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="1e680-112">Det här kommandot får konfigurationen för det aktuella Azure-abonnemanget och sparar den i en lokal fil.</span><span class="sxs-lookup"><span data-stu-id="1e680-112">This command gets the virtual network configuration of the current Azure subscription and then saves it to a local file.</span></span>

## <span data-ttu-id="1e680-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e680-113">PARAMETERS</span></span>

### <span data-ttu-id="1e680-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="1e680-114">-ExportToFile</span></span>
<span data-ttu-id="1e680-115">Anger sökväg och fil namn för en nätverks konfigurations fil som ska skapas från inställningarna.</span><span class="sxs-lookup"><span data-stu-id="1e680-115">Specifies the path and file name of a network configuration file to be created from the settings.</span></span>

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

### <span data-ttu-id="1e680-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1e680-116">-InformationAction</span></span>
<span data-ttu-id="1e680-117">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="1e680-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1e680-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1e680-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e680-119">Vidare</span><span class="sxs-lookup"><span data-stu-id="1e680-119">Continue</span></span>
- <span data-ttu-id="1e680-120">Över</span><span class="sxs-lookup"><span data-stu-id="1e680-120">Ignore</span></span>
- <span data-ttu-id="1e680-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="1e680-121">Inquire</span></span>
- <span data-ttu-id="1e680-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1e680-122">SilentlyContinue</span></span>
- <span data-ttu-id="1e680-123">Stanna</span><span class="sxs-lookup"><span data-stu-id="1e680-123">Stop</span></span>
- <span data-ttu-id="1e680-124">Avbryt</span><span class="sxs-lookup"><span data-stu-id="1e680-124">Suspend</span></span>

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

### <span data-ttu-id="1e680-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1e680-125">-InformationVariable</span></span>
<span data-ttu-id="1e680-126">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="1e680-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1e680-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="1e680-127">-Profile</span></span>
<span data-ttu-id="1e680-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="1e680-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e680-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="1e680-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e680-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e680-130">CommonParameters</span></span>
<span data-ttu-id="1e680-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e680-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e680-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e680-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e680-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e680-133">INPUTS</span></span>

## <span data-ttu-id="1e680-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e680-134">OUTPUTS</span></span>

## <span data-ttu-id="1e680-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e680-135">NOTES</span></span>

## <span data-ttu-id="1e680-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e680-136">RELATED LINKS</span></span>

[<span data-ttu-id="1e680-137">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="1e680-137">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="1e680-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="1e680-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="1e680-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="1e680-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


