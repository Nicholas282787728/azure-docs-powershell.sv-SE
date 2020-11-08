---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: EFBC8DCD-00CC-4BBF-9383-EA15376535F3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42780f62bc68659874f7aae1e64ad5ce89038fdf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099073"
---
# <span data-ttu-id="150dd-101">Update-AzureWebsiteRepository</span><span class="sxs-lookup"><span data-stu-id="150dd-101">Update-AzureWebsiteRepository</span></span>

## <span data-ttu-id="150dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="150dd-102">SYNOPSIS</span></span>
<span data-ttu-id="150dd-103">Uppdaterar fjärrdatabaserna till en lokal Git-databas för alla platser.</span><span class="sxs-lookup"><span data-stu-id="150dd-103">Updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="150dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="150dd-104">SYNTAX</span></span>

```
Update-AzureWebsiteRepository [-Name <String>] -PublishingUsername <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="150dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="150dd-105">DESCRIPTION</span></span>
<span data-ttu-id="150dd-106">Cmdleten **Update-AzureWebsiteRepository** uppdaterar fjärrdatabaserna för en lokal git-lagringsplats för alla platser.</span><span class="sxs-lookup"><span data-stu-id="150dd-106">The **Update-AzureWebsiteRepository** cmdlet updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="150dd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="150dd-107">EXAMPLES</span></span>

### <span data-ttu-id="150dd-108">Exempel 1: uppdatera webbplatsens fjärrdatabaser</span><span class="sxs-lookup"><span data-stu-id="150dd-108">Example 1: Update Website Remote Repositories</span></span>
```
PS C:\> Update-AzureWebsiteRepository -Name MyWebsite
```

<span data-ttu-id="150dd-109">Uppdaterar fjärrdatabaserna för en lokal git-lagringsplats för alla platser för webbplatsen webbplats.</span><span class="sxs-lookup"><span data-stu-id="150dd-109">Updates the remote repositories of a local git repository for all the slots for website MyWebsite.</span></span>

## <span data-ttu-id="150dd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="150dd-110">PARAMETERS</span></span>

### <span data-ttu-id="150dd-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="150dd-111">-Name</span></span>
<span data-ttu-id="150dd-112">Webbplatsens namn.</span><span class="sxs-lookup"><span data-stu-id="150dd-112">The name of the website.</span></span>

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

### <span data-ttu-id="150dd-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="150dd-113">-Profile</span></span>
<span data-ttu-id="150dd-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="150dd-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="150dd-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="150dd-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="150dd-116">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="150dd-116">-PublishingUsername</span></span>
<span data-ttu-id="150dd-117">Det användar namn som du har angett i Microsoft Azure-portalen för Git-distribution.</span><span class="sxs-lookup"><span data-stu-id="150dd-117">The username you have specified in the Microsoft Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="150dd-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="150dd-118">-Confirm</span></span>
<span data-ttu-id="150dd-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="150dd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="150dd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="150dd-120">-WhatIf</span></span>
<span data-ttu-id="150dd-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="150dd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="150dd-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="150dd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="150dd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150dd-123">CommonParameters</span></span>
<span data-ttu-id="150dd-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="150dd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150dd-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="150dd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150dd-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="150dd-126">INPUTS</span></span>

## <span data-ttu-id="150dd-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="150dd-127">OUTPUTS</span></span>

## <span data-ttu-id="150dd-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="150dd-128">NOTES</span></span>

## <span data-ttu-id="150dd-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="150dd-129">RELATED LINKS</span></span>

[<span data-ttu-id="150dd-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="150dd-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="150dd-131">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="150dd-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="150dd-132">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="150dd-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="150dd-133">Stopp-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="150dd-133">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


