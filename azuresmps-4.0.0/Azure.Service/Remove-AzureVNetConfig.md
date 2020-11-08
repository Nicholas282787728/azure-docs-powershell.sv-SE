---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D903741F-1D22-48FC-BFA5-6876E557EFE5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4284d34ef5151dbcd16d9ed882dcf112abbb8ea5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093218"
---
# <span data-ttu-id="84d19-101">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="84d19-101">Remove-AzureVNetConfig</span></span>

## <span data-ttu-id="84d19-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84d19-102">SYNOPSIS</span></span>
<span data-ttu-id="84d19-103">Tar bort nätverks konfigurationen från det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="84d19-103">Deletes the network configuration from the current Azure subscription.</span></span>

## <span data-ttu-id="84d19-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84d19-104">SYNTAX</span></span>

```
Remove-AzureVNetConfig [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="84d19-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84d19-105">DESCRIPTION</span></span>
<span data-ttu-id="84d19-106">Cmdleten **Remove-AzureVNetConfig** tar bort alla inställningar för virtuella nätverk från det aktuella Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="84d19-106">The **Remove-AzureVNetConfig** cmdlet removes all virtual network settings from the current Azure subscription.</span></span>

## <span data-ttu-id="84d19-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84d19-107">EXAMPLES</span></span>

### <span data-ttu-id="84d19-108">Exempel 1: ta bort en virtuell nätverks konfiguration från den aktuella prenumerationen</span><span class="sxs-lookup"><span data-stu-id="84d19-108">Example 1: Remove a virtual network configuration from the current subscription</span></span>
```
PS C:\> Remove-AzureVNetConfig
```

<span data-ttu-id="84d19-109">Det här kommandot tar bort konfigurationen för det virtuella nätverket från nuvarande prenumeration.</span><span class="sxs-lookup"><span data-stu-id="84d19-109">This command removes the virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="84d19-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84d19-110">PARAMETERS</span></span>

### <span data-ttu-id="84d19-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="84d19-111">-InformationAction</span></span>
<span data-ttu-id="84d19-112">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="84d19-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="84d19-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="84d19-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="84d19-114">Vidare</span><span class="sxs-lookup"><span data-stu-id="84d19-114">Continue</span></span>
- <span data-ttu-id="84d19-115">Över</span><span class="sxs-lookup"><span data-stu-id="84d19-115">Ignore</span></span>
- <span data-ttu-id="84d19-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="84d19-116">Inquire</span></span>
- <span data-ttu-id="84d19-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="84d19-117">SilentlyContinue</span></span>
- <span data-ttu-id="84d19-118">Stanna</span><span class="sxs-lookup"><span data-stu-id="84d19-118">Stop</span></span>
- <span data-ttu-id="84d19-119">Avbryt</span><span class="sxs-lookup"><span data-stu-id="84d19-119">Suspend</span></span>

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

### <span data-ttu-id="84d19-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="84d19-120">-InformationVariable</span></span>
<span data-ttu-id="84d19-121">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="84d19-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="84d19-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="84d19-122">-Profile</span></span>
<span data-ttu-id="84d19-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="84d19-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="84d19-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="84d19-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="84d19-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d19-125">CommonParameters</span></span>
<span data-ttu-id="84d19-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d19-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d19-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84d19-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d19-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84d19-128">INPUTS</span></span>

## <span data-ttu-id="84d19-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84d19-129">OUTPUTS</span></span>

## <span data-ttu-id="84d19-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84d19-130">NOTES</span></span>

## <span data-ttu-id="84d19-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84d19-131">RELATED LINKS</span></span>

[<span data-ttu-id="84d19-132">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="84d19-132">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="84d19-133">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="84d19-133">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="84d19-134">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="84d19-134">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


