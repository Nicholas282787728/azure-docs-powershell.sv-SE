---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 496ABC97-A493-4E42-B998-28A907DFBC19
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0641fd7bc8dcfa5048ac3e9d922bade199af2bab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099169"
---
# <span data-ttu-id="d9986-101">Switch-AzureWebsiteSlot</span><span class="sxs-lookup"><span data-stu-id="d9986-101">Switch-AzureWebsiteSlot</span></span>

## <span data-ttu-id="d9986-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9986-102">SYNOPSIS</span></span>
<span data-ttu-id="d9986-103">Byter plats på en webbplats till en annan plats.</span><span class="sxs-lookup"><span data-stu-id="d9986-103">Swaps the production slot for a website with another slot.</span></span>

## <span data-ttu-id="d9986-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9986-104">SYNTAX</span></span>

```
Switch-AzureWebsiteSlot [-Name <String>] [-Slot1 <String>] [-Slot2 <String>] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9986-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9986-105">DESCRIPTION</span></span>
<span data-ttu-id="d9986-106">Cmdleten **switch-AzureWebsiteSlot** byter plats på en webbplats med en annan plats.</span><span class="sxs-lookup"><span data-stu-id="d9986-106">The **Switch-AzureWebsiteSlot** cmdlet swaps the production slot for a website with another slot.</span></span>
<span data-ttu-id="d9986-107">Det här fungerar bara på webbplatser med två platser.</span><span class="sxs-lookup"><span data-stu-id="d9986-107">This works on websites with two slots only.</span></span>

## <span data-ttu-id="d9986-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9986-108">EXAMPLES</span></span>

### <span data-ttu-id="d9986-109">Exempel 1: byta plats på webbplatsen</span><span class="sxs-lookup"><span data-stu-id="d9986-109">Example 1: Switch Website Slot</span></span>
```
PS C:\> Switch-AzureWebsiteSlot -Name MyWebsite
```

<span data-ttu-id="d9986-110">Växla till webbplatsen Azure webbplats för säkerhets kopiering med produktions platsen.</span><span class="sxs-lookup"><span data-stu-id="d9986-110">Switch the azure website MyWebsite backup slot with production slot.</span></span>

## <span data-ttu-id="d9986-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9986-111">PARAMETERS</span></span>

### <span data-ttu-id="d9986-112">-Force</span><span class="sxs-lookup"><span data-stu-id="d9986-112">-Force</span></span>
<span data-ttu-id="d9986-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d9986-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9986-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9986-114">-Name</span></span>
<span data-ttu-id="d9986-115">Webbplatsens namn.</span><span class="sxs-lookup"><span data-stu-id="d9986-115">The name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9986-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="d9986-116">-Profile</span></span>
<span data-ttu-id="d9986-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d9986-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d9986-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d9986-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d9986-119">-Slot1</span><span class="sxs-lookup"><span data-stu-id="d9986-119">-Slot1</span></span>
<span data-ttu-id="d9986-120">Anger den första platsen.</span><span class="sxs-lookup"><span data-stu-id="d9986-120">Specifies the first slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9986-121">-Slot2</span><span class="sxs-lookup"><span data-stu-id="d9986-121">-Slot2</span></span>
<span data-ttu-id="d9986-122">Anger den andra platsen.</span><span class="sxs-lookup"><span data-stu-id="d9986-122">Specifies the second slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9986-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d9986-123">-Confirm</span></span>
<span data-ttu-id="d9986-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9986-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9986-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9986-125">-WhatIf</span></span>
<span data-ttu-id="d9986-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d9986-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9986-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d9986-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9986-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9986-128">CommonParameters</span></span>
<span data-ttu-id="d9986-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9986-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9986-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9986-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9986-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9986-131">INPUTS</span></span>

## <span data-ttu-id="d9986-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9986-132">OUTPUTS</span></span>

## <span data-ttu-id="d9986-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9986-133">NOTES</span></span>

## <span data-ttu-id="d9986-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9986-134">RELATED LINKS</span></span>

[<span data-ttu-id="d9986-135">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d9986-135">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="d9986-136">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d9986-136">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="d9986-137">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d9986-137">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="d9986-138">Stopp-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d9986-138">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


