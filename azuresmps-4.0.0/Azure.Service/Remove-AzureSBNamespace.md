---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6E369BDF-AE3C-416B-81B7-097C20147CBE
online version: ''
schema: 2.0.0
ms.openlocfilehash: bb48f7412c957ceefb7df03d79e57ce8e75447d5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099360"
---
# <span data-ttu-id="fd9f9-101">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="fd9f9-101">Remove-AzureSBNamespace</span></span>

## <span data-ttu-id="fd9f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd9f9-102">SYNOPSIS</span></span>
<span data-ttu-id="fd9f9-103">Tar bort ett namn område.</span><span class="sxs-lookup"><span data-stu-id="fd9f9-103">Removes a namespace.</span></span>

## <span data-ttu-id="fd9f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd9f9-104">SYNTAX</span></span>

```
Remove-AzureSBNamespace -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd9f9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd9f9-105">DESCRIPTION</span></span>
<span data-ttu-id="fd9f9-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="fd9f9-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fd9f9-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="fd9f9-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fd9f9-108">Cmdleten **Remove-AzureSBNamespace** tar bort ett tjänst namn område för Service Bus.</span><span class="sxs-lookup"><span data-stu-id="fd9f9-108">The **Remove-AzureSBNamespace** cmdlet removes a service namespace for Service Bus.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="fd9f9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd9f9-109">EXAMPLES</span></span>

## <span data-ttu-id="fd9f9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd9f9-110">PARAMETERS</span></span>

### <span data-ttu-id="fd9f9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fd9f9-111">-Force</span></span>
<span data-ttu-id="fd9f9-112">Om den är aktive rad tar du bort namn området utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="fd9f9-112">If enabled, removes the namespace without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fd9f9-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="fd9f9-113">-Name</span></span>
<span data-ttu-id="fd9f9-114">Anger namnet på namn området som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="fd9f9-114">Specifies the name of the namespace to be removed.</span></span>

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

### <span data-ttu-id="fd9f9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd9f9-115">-PassThru</span></span>
<span data-ttu-id="fd9f9-116">Gör att åtgärden returnerar true om den lyckas.</span><span class="sxs-lookup"><span data-stu-id="fd9f9-116">Causes the operation to return true if it succeeds.</span></span>

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

### <span data-ttu-id="fd9f9-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="fd9f9-117">-Profile</span></span>
<span data-ttu-id="fd9f9-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="fd9f9-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fd9f9-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="fd9f9-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fd9f9-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fd9f9-120">-Confirm</span></span>
<span data-ttu-id="fd9f9-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fd9f9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd9f9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd9f9-122">-WhatIf</span></span>
<span data-ttu-id="fd9f9-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fd9f9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd9f9-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fd9f9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd9f9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd9f9-125">CommonParameters</span></span>
<span data-ttu-id="fd9f9-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd9f9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd9f9-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd9f9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd9f9-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd9f9-128">INPUTS</span></span>

## <span data-ttu-id="fd9f9-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd9f9-129">OUTPUTS</span></span>

## <span data-ttu-id="fd9f9-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd9f9-130">NOTES</span></span>

## <span data-ttu-id="fd9f9-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd9f9-131">RELATED LINKS</span></span>

[<span data-ttu-id="fd9f9-132">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="fd9f9-132">New-AzureSBNamespace</span></span>](./New-AzureSBNamespace.md)


