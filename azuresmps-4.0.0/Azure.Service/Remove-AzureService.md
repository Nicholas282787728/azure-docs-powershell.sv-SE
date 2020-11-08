---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03107EA1-6ADA-4A3E-B8E1-88788E5F3F37
online version: ''
schema: 2.0.0
ms.openlocfilehash: 21892d129319977897a6855933e3e8542460a4a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099357"
---
# <span data-ttu-id="729f4-101">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="729f4-101">Remove-AzureService</span></span>

## <span data-ttu-id="729f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="729f4-102">SYNOPSIS</span></span>
<span data-ttu-id="729f4-103">Tar bort den aktuella moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="729f4-103">Removes the current cloud service.</span></span>

## <span data-ttu-id="729f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="729f4-104">SYNTAX</span></span>

```
Remove-AzureService [-ServiceName <String>] [-Force] [-PassThru] [-DeleteAll] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="729f4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="729f4-105">DESCRIPTION</span></span>
<span data-ttu-id="729f4-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="729f4-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="729f4-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="729f4-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="729f4-108">Cmdleten **Remove-AzureService** stoppar och tar bort den aktuella moln tjänsten, eller så matchar tjänsten inte den angivna tjänst-och prenumerations namnet.</span><span class="sxs-lookup"><span data-stu-id="729f4-108">The **Remove-AzureService** cmdlet stops and removes the current cloud service, or the service matching the specified service and subscription name.</span></span>

## <span data-ttu-id="729f4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="729f4-109">EXAMPLES</span></span>

## <span data-ttu-id="729f4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="729f4-110">PARAMETERS</span></span>

### <span data-ttu-id="729f4-111">-DeleteAll</span><span class="sxs-lookup"><span data-stu-id="729f4-111">-DeleteAll</span></span>
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

### <span data-ttu-id="729f4-112">-Force</span><span class="sxs-lookup"><span data-stu-id="729f4-112">-Force</span></span>
<span data-ttu-id="729f4-113">Tar bort tjänsten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="729f4-113">Removes the service without prompting for confirmation.</span></span>

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

### <span data-ttu-id="729f4-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="729f4-114">-PassThru</span></span>
<span data-ttu-id="729f4-115">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="729f4-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="729f4-116">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="729f4-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="729f4-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="729f4-117">-Profile</span></span>
<span data-ttu-id="729f4-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="729f4-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="729f4-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="729f4-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="729f4-120">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="729f4-120">-ServiceName</span></span>
<span data-ttu-id="729f4-121">Anger namnet på tjänsten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="729f4-121">Specifies the name of the service to be removed.</span></span>
<span data-ttu-id="729f4-122">Om kommandot körs från en tjänst katalog men inget namn har angetts, används det aktuella tjänst namnet.</span><span class="sxs-lookup"><span data-stu-id="729f4-122">If the command is run from a service directory and no name is specified, uses the current service name.</span></span>

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

### <span data-ttu-id="729f4-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="729f4-123">-Confirm</span></span>
<span data-ttu-id="729f4-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="729f4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="729f4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="729f4-125">-WhatIf</span></span>
<span data-ttu-id="729f4-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="729f4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="729f4-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="729f4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="729f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="729f4-128">CommonParameters</span></span>
<span data-ttu-id="729f4-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="729f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="729f4-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="729f4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="729f4-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="729f4-131">INPUTS</span></span>

## <span data-ttu-id="729f4-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="729f4-132">OUTPUTS</span></span>

## <span data-ttu-id="729f4-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="729f4-133">NOTES</span></span>

## <span data-ttu-id="729f4-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="729f4-134">RELATED LINKS</span></span>

[<span data-ttu-id="729f4-135">Publicera – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="729f4-135">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="729f4-136">Stopp-AzureService</span><span class="sxs-lookup"><span data-stu-id="729f4-136">Stop-AzureService</span></span>](./Stop-AzureService.md)

[<span data-ttu-id="729f4-137">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="729f4-137">Start-AzureService</span></span>](./Start-AzureService.md)


