---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8062D57E-8381-4715-9AA8-551F15DCC492
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2627bdb2f098d5b09851ec5970dd2a73840d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093209"
---
# <span data-ttu-id="dce3a-101">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="dce3a-101">Remove-AzureWebsite</span></span>

## <span data-ttu-id="dce3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dce3a-102">SYNOPSIS</span></span>
<span data-ttu-id="dce3a-103">Tar bort den angivna webbplatsen från Azure.</span><span class="sxs-lookup"><span data-stu-id="dce3a-103">Removes the specified website from Azure.</span></span>

## <span data-ttu-id="dce3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dce3a-104">SYNTAX</span></span>

```
Remove-AzureWebsite [-Force] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dce3a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dce3a-105">DESCRIPTION</span></span>
<span data-ttu-id="dce3a-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="dce3a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="dce3a-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="dce3a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="dce3a-108">Cmdleten **Remove-AzureWebsite** tar bort den angivna webbplatsen från Azure, med eller utan en uppmaning om att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="dce3a-108">The **Remove-AzureWebsite** cmdlet removes the specified website from Azure, either with or without a prompt for confirmation.</span></span>

## <span data-ttu-id="dce3a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dce3a-109">EXAMPLES</span></span>

### <span data-ttu-id="dce3a-110">Exempel 1: ta bort den aktuella webbplatsen</span><span class="sxs-lookup"><span data-stu-id="dce3a-110">Example 1: Remove the current website</span></span>
```
PS C:\> Remove-AzureWebsite
```

<span data-ttu-id="dce3a-111">Det här exemplet tar bort webbplatsen i Azure som är associerad med den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="dce3a-111">This example removes the website in Azure associated with the current directory.</span></span>

### <span data-ttu-id="dce3a-112">Exempel 2: ta bort en webbplats utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="dce3a-112">Example 2: Remove a website without confirmation</span></span>
```
PS C:\> Remove-AzureWebsite -Name mySite -Force
```

<span data-ttu-id="dce3a-113">Det här exemplet tar bort webbplatsen som heter min webbplats utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="dce3a-113">This example deletes the website named mySite without prompting for confirmation.</span></span>

## <span data-ttu-id="dce3a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dce3a-114">PARAMETERS</span></span>

### <span data-ttu-id="dce3a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dce3a-115">-Force</span></span>
<span data-ttu-id="dce3a-116">Om den anges tar du bort angiven webbplats utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="dce3a-116">If specified, deletes the specified website without prompting for confirmation.</span></span>

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

### <span data-ttu-id="dce3a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="dce3a-117">-Name</span></span>
<span data-ttu-id="dce3a-118">Anger namnet på den webbplats som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="dce3a-118">Specifies the name of the website to delete.</span></span>

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

### <span data-ttu-id="dce3a-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="dce3a-119">-Profile</span></span>
<span data-ttu-id="dce3a-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="dce3a-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dce3a-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="dce3a-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dce3a-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="dce3a-122">-Slot</span></span>
<span data-ttu-id="dce3a-123">Anger webbplatsens namn.</span><span class="sxs-lookup"><span data-stu-id="dce3a-123">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="dce3a-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dce3a-124">-Confirm</span></span>
<span data-ttu-id="dce3a-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dce3a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dce3a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dce3a-126">-WhatIf</span></span>
<span data-ttu-id="dce3a-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dce3a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dce3a-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dce3a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dce3a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce3a-129">CommonParameters</span></span>
<span data-ttu-id="dce3a-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dce3a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce3a-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce3a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce3a-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dce3a-132">INPUTS</span></span>

## <span data-ttu-id="dce3a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dce3a-133">OUTPUTS</span></span>

## <span data-ttu-id="dce3a-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dce3a-134">NOTES</span></span>

## <span data-ttu-id="dce3a-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dce3a-135">RELATED LINKS</span></span>

[<span data-ttu-id="dce3a-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="dce3a-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


