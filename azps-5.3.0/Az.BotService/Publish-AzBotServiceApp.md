---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 4ef38ab40f90024124f7d5f09f1a55c16520dd6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527171"
---
# <span data-ttu-id="706b0-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="706b0-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="706b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="706b0-102">SYNOPSIS</span></span>
<span data-ttu-id="706b0-103">Returnerar en BotService som anges av parametrarna.</span><span class="sxs-lookup"><span data-stu-id="706b0-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="706b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="706b0-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="706b0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="706b0-105">DESCRIPTION</span></span>
<span data-ttu-id="706b0-106">Returnerar en BotService som anges av parametrarna.</span><span class="sxs-lookup"><span data-stu-id="706b0-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="706b0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="706b0-107">EXAMPLES</span></span>

### <span data-ttu-id="706b0-108">Exempel 1: publicera din BotService i Azure</span><span class="sxs-lookup"><span data-stu-id="706b0-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="706b0-109">Publicera din BotService till Azure by-kod</span><span class="sxs-lookup"><span data-stu-id="706b0-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="706b0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="706b0-110">PARAMETERS</span></span>

### <span data-ttu-id="706b0-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="706b0-111">-CodeDir</span></span>
<span data-ttu-id="706b0-112">Den här parametern anger sökvägen till ZIP-filen</span><span class="sxs-lookup"><span data-stu-id="706b0-112">This parameter defines the Path of the ZIP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706b0-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="706b0-113">-Name</span></span>
<span data-ttu-id="706b0-114">Den här parametern definierar namnet på bot.</span><span class="sxs-lookup"><span data-stu-id="706b0-114">This parameter defines the name of the bot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706b0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="706b0-115">-ResourceGroupName</span></span>
<span data-ttu-id="706b0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="706b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706b0-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="706b0-117">-Confirm</span></span>
<span data-ttu-id="706b0-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="706b0-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706b0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="706b0-119">-WhatIf</span></span>
<span data-ttu-id="706b0-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="706b0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="706b0-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="706b0-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="706b0-122">CommonParameters</span></span>
<span data-ttu-id="706b0-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="706b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="706b0-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="706b0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="706b0-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="706b0-125">INPUTS</span></span>

## <span data-ttu-id="706b0-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="706b0-126">OUTPUTS</span></span>

## <span data-ttu-id="706b0-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="706b0-127">NOTES</span></span>

<span data-ttu-id="706b0-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="706b0-128">ALIASES</span></span>

## <span data-ttu-id="706b0-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="706b0-129">RELATED LINKS</span></span>

