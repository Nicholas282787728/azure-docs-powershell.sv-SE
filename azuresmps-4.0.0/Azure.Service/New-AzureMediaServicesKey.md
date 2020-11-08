---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 756F757C-8CDE-43A5-A8A6-D55EF9C66183
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71402e56251e2632c73a9185a1e70b4e3de8d770
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099231"
---
# <span data-ttu-id="b967e-101">New-AzureMediaServicesKey</span><span class="sxs-lookup"><span data-stu-id="b967e-101">New-AzureMediaServicesKey</span></span>

## <span data-ttu-id="b967e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b967e-102">SYNOPSIS</span></span>
<span data-ttu-id="b967e-103">Uppdaterar nyckel nycklar för Azure Media Services.</span><span class="sxs-lookup"><span data-stu-id="b967e-103">Updates Azure Media Services account keys.</span></span>

<span data-ttu-id="b967e-104">**Obs!** Den här versionen är föråldrad, se den [senaste versionen](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="b967e-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="b967e-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b967e-105">SYNTAX</span></span>

```
New-AzureMediaServicesKey -Name <String> -KeyType <MediaServicesKeyType> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b967e-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b967e-106">DESCRIPTION</span></span>
<span data-ttu-id="b967e-107">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="b967e-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b967e-108">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b967e-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b967e-109">Cmdleten **New-AzureMediaServicesKey** uppdaterar den primära eller sekundära tangenten för det angivna medie tjänst kontot.</span><span class="sxs-lookup"><span data-stu-id="b967e-109">The **New-AzureMediaServicesKey** cmdlet updates the Primary or Secondary key for the specified Media Services account.</span></span>

## <span data-ttu-id="b967e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b967e-110">EXAMPLES</span></span>

### <span data-ttu-id="b967e-111">Exempel 1: uppdatera en medie tjänsts konto-profil</span><span class="sxs-lookup"><span data-stu-id="b967e-111">Example 1: Update a Media Services account key</span></span>
```
PS C:\> New-AzureMediaServicesKey -Name "mediaservicesaccount" -KeyType "Primary" -Force
```

## <span data-ttu-id="b967e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b967e-112">PARAMETERS</span></span>

### <span data-ttu-id="b967e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b967e-113">-Force</span></span>
<span data-ttu-id="b967e-114">Anger att den inte har bekräftats.</span><span class="sxs-lookup"><span data-stu-id="b967e-114">Indicates that the key generation is not confirmed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b967e-115">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="b967e-115">-KeyType</span></span>
<span data-ttu-id="b967e-116">Anger medie tjänstens typ, Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="b967e-116">Specifies the Media Services key type; Valid values are:</span></span>
  
- <span data-ttu-id="b967e-117">Första</span><span class="sxs-lookup"><span data-stu-id="b967e-117">Primary</span></span>
- <span data-ttu-id="b967e-118">Sekundär</span><span class="sxs-lookup"><span data-stu-id="b967e-118">Secondary</span></span>

```yaml
Type: MediaServicesKeyType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b967e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b967e-119">-Name</span></span>
<span data-ttu-id="b967e-120">Anger namnet på medie tjänst kontot.</span><span class="sxs-lookup"><span data-stu-id="b967e-120">Specifies the name of the Media Services account.</span></span>

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

### <span data-ttu-id="b967e-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="b967e-121">-Profile</span></span>
<span data-ttu-id="b967e-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b967e-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b967e-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b967e-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b967e-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b967e-124">-Confirm</span></span>
<span data-ttu-id="b967e-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b967e-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b967e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b967e-126">-WhatIf</span></span>
<span data-ttu-id="b967e-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b967e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b967e-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b967e-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b967e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b967e-129">CommonParameters</span></span>
<span data-ttu-id="b967e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b967e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b967e-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b967e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b967e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b967e-132">INPUTS</span></span>

## <span data-ttu-id="b967e-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b967e-133">OUTPUTS</span></span>

## <span data-ttu-id="b967e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b967e-134">NOTES</span></span>

## <span data-ttu-id="b967e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b967e-135">RELATED LINKS</span></span>

[<span data-ttu-id="b967e-136">Använda Azure PowerShell för medie tjänster</span><span class="sxs-lookup"><span data-stu-id="b967e-136">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


