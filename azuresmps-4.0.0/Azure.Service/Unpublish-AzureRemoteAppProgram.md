---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DB3F85D6-5962-4288-AD75-0C30448B769C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88438fa66e39b5ad63db7b6d2609107d224f7faf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099250"
---
# <span data-ttu-id="0b772-101">Unpublish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="0b772-101">Unpublish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="0b772-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b772-102">SYNOPSIS</span></span>
<span data-ttu-id="0b772-103">Avpublicerar ett Azure RemoteApp-program.</span><span class="sxs-lookup"><span data-stu-id="0b772-103">Unpublishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="0b772-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b772-104">SYNTAX</span></span>

```
Unpublish-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String[]>] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b772-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b772-105">DESCRIPTION</span></span>
<span data-ttu-id="0b772-106">Cmdleten **unpublishing-AzureRemoteAppProgram** avpublicerar ett Azure RemoteApp-program.</span><span class="sxs-lookup"><span data-stu-id="0b772-106">The **Unpublish-AzureRemoteAppProgram** cmdlet unpublishes an Azure RemoteApp program.</span></span>
<span data-ttu-id="0b772-107">När du har avpublicerat ett program är det inte längre tillgängligt för användarna av en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="0b772-107">After you unpublish a program, it is no longer available to the users of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="0b772-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b772-108">EXAMPLES</span></span>

## <span data-ttu-id="0b772-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b772-109">PARAMETERS</span></span>

### <span data-ttu-id="0b772-110">-Alias</span><span class="sxs-lookup"><span data-stu-id="0b772-110">-Alias</span></span>
<span data-ttu-id="0b772-111">Anger en matris med alias för de program som ska avpubliceras.</span><span class="sxs-lookup"><span data-stu-id="0b772-111">Specifies an array of aliases of the programs to unpublish.</span></span>
<span data-ttu-id="0b772-112">Använd **Get-AzureRemoteAppProgram** för att hämta alias för ett program som ska avpubliceras.</span><span class="sxs-lookup"><span data-stu-id="0b772-112">Use **Get-AzureRemoteAppProgram** to retrieve the alias of a program to unpublish.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b772-113">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="0b772-113">-CollectionName</span></span>
<span data-ttu-id="0b772-114">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="0b772-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="0b772-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="0b772-115">-Profile</span></span>
<span data-ttu-id="0b772-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0b772-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b772-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0b772-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0b772-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0b772-118">-Confirm</span></span>
<span data-ttu-id="0b772-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0b772-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b772-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b772-120">-WhatIf</span></span>
<span data-ttu-id="0b772-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0b772-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b772-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0b772-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b772-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b772-123">CommonParameters</span></span>
<span data-ttu-id="0b772-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b772-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b772-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b772-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b772-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b772-126">INPUTS</span></span>

## <span data-ttu-id="0b772-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b772-127">OUTPUTS</span></span>

## <span data-ttu-id="0b772-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b772-128">NOTES</span></span>

## <span data-ttu-id="0b772-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b772-129">RELATED LINKS</span></span>

[<span data-ttu-id="0b772-130">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="0b772-130">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="0b772-131">Publicera – AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="0b772-131">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)


