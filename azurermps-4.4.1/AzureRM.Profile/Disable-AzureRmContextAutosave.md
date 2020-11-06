---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: 85c3791e9947ce6f7ad2ce365239da16cec17b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584592"
---
# <span data-ttu-id="05297-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="05297-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="05297-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05297-102">SYNOPSIS</span></span>
<span data-ttu-id="05297-103">Inaktivera Spara autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="05297-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="05297-104">Din inloggnings information blir glömt nästa gång du öppnar ett PowerShell-fönster</span><span class="sxs-lookup"><span data-stu-id="05297-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05297-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05297-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05297-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05297-106">DESCRIPTION</span></span>
<span data-ttu-id="05297-107">Inaktivera Spara autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="05297-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="05297-108">Din inloggnings information blir glömt nästa gång du öppnar ett PowerShell-fönster</span><span class="sxs-lookup"><span data-stu-id="05297-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="05297-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05297-109">EXAMPLES</span></span>

### <span data-ttu-id="05297-110">Inaktivera autosparande av kontexten</span><span class="sxs-lookup"><span data-stu-id="05297-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="05297-111">Inaktivera Spara automatiskt för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="05297-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="05297-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05297-112">PARAMETERS</span></span>

### <span data-ttu-id="05297-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05297-113">-DefaultProfile</span></span>
<span data-ttu-id="05297-114">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="05297-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05297-115">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="05297-115">-Scope</span></span>
<span data-ttu-id="05297-116">Avgör omfattningen av kontext ändringar, till exempel wheher ändringar gäller endast för cusrrent-processen eller för alla sessioner som användaren startar</span><span class="sxs-lookup"><span data-stu-id="05297-116">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05297-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05297-117">-Confirm</span></span>
<span data-ttu-id="05297-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05297-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05297-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05297-119">-WhatIf</span></span>
<span data-ttu-id="05297-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05297-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05297-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05297-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05297-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05297-122">CommonParameters</span></span>
<span data-ttu-id="05297-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05297-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05297-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05297-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05297-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05297-125">INPUTS</span></span>

### <span data-ttu-id="05297-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="05297-126">None</span></span>

## <span data-ttu-id="05297-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05297-127">OUTPUTS</span></span>

### <span data-ttu-id="05297-128">Microsoft. Azure. kommandon. Common. inloggningsautentisering. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="05297-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="05297-129">Information om aktuella inställningar för autosparande, inklusive om Spara automatiskt är aktiverat för den aktuella användaren, samt var kontext och autentiseringsuppgifter sparas.</span><span class="sxs-lookup"><span data-stu-id="05297-129">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="05297-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05297-130">NOTES</span></span>

## <span data-ttu-id="05297-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05297-131">RELATED LINKS</span></span>

