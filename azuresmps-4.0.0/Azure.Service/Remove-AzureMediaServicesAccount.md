---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5B255D11-0A9B-4679-A2AC-4357B293EE96
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4eee130312ae52e95b020151750d46144bc3685
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099701"
---
# <span data-ttu-id="e0eda-101">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e0eda-101">Remove-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="e0eda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0eda-102">SYNOPSIS</span></span>
<span data-ttu-id="e0eda-103">Tar bort angivet Azure Media Services-konto.</span><span class="sxs-lookup"><span data-stu-id="e0eda-103">Removes the specified Azure Media Services account.</span></span>

<span data-ttu-id="e0eda-104">**Obs!**  Den här versionen är föråldrad, se den [senaste versionen](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="e0eda-104">**Note:**  This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="e0eda-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0eda-105">SYNTAX</span></span>

```
Remove-AzureMediaServicesAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0eda-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0eda-106">DESCRIPTION</span></span>
<span data-ttu-id="e0eda-107">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="e0eda-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e0eda-108">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e0eda-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e0eda-109">Cmdleten **Remove-AzureMediaServicesAccount** tar bort ett Media Services-konto.</span><span class="sxs-lookup"><span data-stu-id="e0eda-109">The **Remove-AzureMediaServicesAccount** cmdlet removes a Media Services account.</span></span>

## <span data-ttu-id="e0eda-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0eda-110">EXAMPLES</span></span>

### <span data-ttu-id="e0eda-111">Exempel 1: ta bort ett medie tjänst konto</span><span class="sxs-lookup"><span data-stu-id="e0eda-111">Example 1: Delete a Media Services account</span></span>
```
PS C:\> Remove-AzureMediaServicesAccount -Name "mediaservicesaccount" -Force
```

## <span data-ttu-id="e0eda-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0eda-112">PARAMETERS</span></span>

### <span data-ttu-id="e0eda-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e0eda-113">-Force</span></span>
<span data-ttu-id="e0eda-114">Om växeln *Force* har angetts bekräftas inte borttagningen.</span><span class="sxs-lookup"><span data-stu-id="e0eda-114">If the *Force* switch is specified, the deletion is not confirmed.</span></span>

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

### <span data-ttu-id="e0eda-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0eda-115">-Name</span></span>
<span data-ttu-id="e0eda-116">Medie tjänstens konto namn.</span><span class="sxs-lookup"><span data-stu-id="e0eda-116">The Media Services account name.</span></span>

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

### <span data-ttu-id="e0eda-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="e0eda-117">-Profile</span></span>
<span data-ttu-id="e0eda-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e0eda-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0eda-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e0eda-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0eda-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e0eda-120">-Confirm</span></span>
<span data-ttu-id="e0eda-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e0eda-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0eda-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0eda-122">-WhatIf</span></span>
<span data-ttu-id="e0eda-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e0eda-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0eda-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e0eda-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0eda-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0eda-125">CommonParameters</span></span>
<span data-ttu-id="e0eda-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0eda-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0eda-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0eda-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0eda-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0eda-128">INPUTS</span></span>

## <span data-ttu-id="e0eda-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0eda-129">OUTPUTS</span></span>

## <span data-ttu-id="e0eda-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0eda-130">NOTES</span></span>

## <span data-ttu-id="e0eda-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0eda-131">RELATED LINKS</span></span>

[<span data-ttu-id="e0eda-132">Använda Azure PowerShell för medie tjänster</span><span class="sxs-lookup"><span data-stu-id="e0eda-132">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="e0eda-133">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e0eda-133">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="e0eda-134">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e0eda-134">New-AzureMediaServicesAccount</span></span>](./New-AzureMediaServicesAccount.md)


