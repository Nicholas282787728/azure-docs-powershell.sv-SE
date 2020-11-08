---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8E67D1A4-4247-4603-8D26-42D6D48FE686
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90c654432760061d5c2ba36675c958135329b225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099098"
---
# <span data-ttu-id="0eb9f-101">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="0eb9f-101">Remove-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="0eb9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0eb9f-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb9f-103">Tar bort en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="0eb9f-103">Removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="0eb9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0eb9f-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppCollection [-CollectionName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0eb9f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0eb9f-105">DESCRIPTION</span></span>
<span data-ttu-id="0eb9f-106">Cmdleten **Remove-AzureRemoteAppCollection** tar bort en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="0eb9f-106">The **Remove-AzureRemoteAppCollection** cmdlet removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="0eb9f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0eb9f-107">EXAMPLES</span></span>

## <span data-ttu-id="0eb9f-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0eb9f-108">PARAMETERS</span></span>

### <span data-ttu-id="0eb9f-109">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="0eb9f-109">-CollectionName</span></span>
<span data-ttu-id="0eb9f-110">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="0eb9f-110">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb9f-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="0eb9f-111">-Profile</span></span>
<span data-ttu-id="0eb9f-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0eb9f-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0eb9f-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0eb9f-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0eb9f-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0eb9f-114">-Confirm</span></span>
<span data-ttu-id="0eb9f-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0eb9f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb9f-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb9f-116">-WhatIf</span></span>
<span data-ttu-id="0eb9f-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0eb9f-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eb9f-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0eb9f-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb9f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb9f-119">CommonParameters</span></span>
<span data-ttu-id="0eb9f-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb9f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb9f-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eb9f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb9f-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0eb9f-122">INPUTS</span></span>

## <span data-ttu-id="0eb9f-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0eb9f-123">OUTPUTS</span></span>

## <span data-ttu-id="0eb9f-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0eb9f-124">NOTES</span></span>

## <span data-ttu-id="0eb9f-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0eb9f-125">RELATED LINKS</span></span>

[<span data-ttu-id="0eb9f-126">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="0eb9f-126">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="0eb9f-127">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="0eb9f-127">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="0eb9f-128">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="0eb9f-128">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="0eb9f-129">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="0eb9f-129">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


