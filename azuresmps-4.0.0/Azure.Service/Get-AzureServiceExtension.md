---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2664607C-FF95-4EB7-869E-A421343B0517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 231f24a20471d8a4639b091c10d0e04f65b71b76
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093325"
---
# <span data-ttu-id="d219b-101">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="d219b-101">Get-AzureServiceExtension</span></span>

## <span data-ttu-id="d219b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d219b-102">SYNOPSIS</span></span>
<span data-ttu-id="d219b-103">Hämtar moln tjänst tillägg som används vid en distribution.</span><span class="sxs-lookup"><span data-stu-id="d219b-103">Gets cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="d219b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d219b-104">SYNTAX</span></span>

```
Get-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-ExtensionName] <String>]
 [[-ProviderNamespace] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d219b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d219b-105">DESCRIPTION</span></span>
<span data-ttu-id="d219b-106">Cmdleten **Get-AzureServiceExtension** hämtar befintliga moln tjänst tillägg som tillämpas på en distribution.</span><span class="sxs-lookup"><span data-stu-id="d219b-106">The **Get-AzureServiceExtension** cmdlet gets existing cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="d219b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d219b-107">EXAMPLES</span></span>

### <span data-ttu-id="d219b-108">Exempel 1: Hämta ett angivet tillägg</span><span class="sxs-lookup"><span data-stu-id="d219b-108">Example 1: Get a specified extension</span></span>
```
PS C:\> Get-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="d219b-109">Det här kommandot får moln tjänst tillägget med det angivna namnet och namn området.</span><span class="sxs-lookup"><span data-stu-id="d219b-109">This command gets the cloud service extension with the specified name and namespace.</span></span>

## <span data-ttu-id="d219b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d219b-110">PARAMETERS</span></span>

### <span data-ttu-id="d219b-111">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="d219b-111">-ExtensionName</span></span>
<span data-ttu-id="d219b-112">Anger tillägget.</span><span class="sxs-lookup"><span data-stu-id="d219b-112">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d219b-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d219b-113">-InformationAction</span></span>
<span data-ttu-id="d219b-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="d219b-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d219b-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d219b-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d219b-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="d219b-116">Continue</span></span>
- <span data-ttu-id="d219b-117">Över</span><span class="sxs-lookup"><span data-stu-id="d219b-117">Ignore</span></span>
- <span data-ttu-id="d219b-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="d219b-118">Inquire</span></span>
- <span data-ttu-id="d219b-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d219b-119">SilentlyContinue</span></span>
- <span data-ttu-id="d219b-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="d219b-120">Stop</span></span>
- <span data-ttu-id="d219b-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="d219b-121">Suspend</span></span>

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

### <span data-ttu-id="d219b-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d219b-122">-InformationVariable</span></span>
<span data-ttu-id="d219b-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="d219b-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d219b-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="d219b-124">-Profile</span></span>
<span data-ttu-id="d219b-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d219b-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d219b-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d219b-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d219b-127">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d219b-127">-ProviderNamespace</span></span>
<span data-ttu-id="d219b-128">Anger namn området för tilläggs leverantör.</span><span class="sxs-lookup"><span data-stu-id="d219b-128">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d219b-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d219b-129">-ServiceName</span></span>
<span data-ttu-id="d219b-130">Anger namnet på distributionen av Azure-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d219b-130">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="d219b-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="d219b-131">-Slot</span></span>
<span data-ttu-id="d219b-132">Anger distributions miljön.</span><span class="sxs-lookup"><span data-stu-id="d219b-132">Specifies the deployment environment.</span></span>
<span data-ttu-id="d219b-133">De acceptabla värdena för denna parameter är: produktion eller mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="d219b-133">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="d219b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d219b-134">CommonParameters</span></span>
<span data-ttu-id="d219b-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d219b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d219b-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d219b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d219b-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d219b-137">INPUTS</span></span>

## <span data-ttu-id="d219b-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d219b-138">OUTPUTS</span></span>

## <span data-ttu-id="d219b-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d219b-139">NOTES</span></span>

## <span data-ttu-id="d219b-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d219b-140">RELATED LINKS</span></span>

[<span data-ttu-id="d219b-141">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="d219b-141">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)

[<span data-ttu-id="d219b-142">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="d219b-142">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


