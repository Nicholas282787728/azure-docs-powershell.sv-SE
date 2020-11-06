---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: c421489490dcd579384b211619180209e9d71f5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584880"
---
# <span data-ttu-id="b8247-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="b8247-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="b8247-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8247-102">SYNOPSIS</span></span>
<span data-ttu-id="b8247-103">Inaktivera Spara autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="b8247-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="b8247-104">Din inloggnings information blir glömt nästa gång du öppnar ett PowerShell-fönster</span><span class="sxs-lookup"><span data-stu-id="b8247-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8247-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8247-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8247-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8247-106">DESCRIPTION</span></span>
<span data-ttu-id="b8247-107">Inaktivera Spara autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="b8247-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="b8247-108">Din inloggnings information blir glömt nästa gång du öppnar ett PowerShell-fönster</span><span class="sxs-lookup"><span data-stu-id="b8247-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="b8247-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8247-109">EXAMPLES</span></span>

### <span data-ttu-id="b8247-110">Inaktivera autosparande av kontexten</span><span class="sxs-lookup"><span data-stu-id="b8247-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="b8247-111">Inaktivera Spara automatiskt för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="b8247-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="b8247-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8247-112">PARAMETERS</span></span>

### <span data-ttu-id="b8247-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8247-113">-DefaultProfile</span></span>
<span data-ttu-id="b8247-114">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b8247-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8247-115">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="b8247-115">-Scope</span></span>
<span data-ttu-id="b8247-116">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som startas av den här användaren</span><span class="sxs-lookup"><span data-stu-id="b8247-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="b8247-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b8247-117">-Confirm</span></span>
<span data-ttu-id="b8247-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8247-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8247-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8247-119">-WhatIf</span></span>
<span data-ttu-id="b8247-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b8247-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8247-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b8247-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8247-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8247-122">CommonParameters</span></span>
<span data-ttu-id="b8247-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8247-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8247-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8247-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8247-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8247-125">INPUTS</span></span>

### <span data-ttu-id="b8247-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="b8247-126">None</span></span>

## <span data-ttu-id="b8247-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8247-127">OUTPUTS</span></span>

### <span data-ttu-id="b8247-128">Microsoft. Azure. kommandon. Common. inloggningsautentisering. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="b8247-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="b8247-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8247-129">NOTES</span></span>

## <span data-ttu-id="b8247-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8247-130">RELATED LINKS</span></span>
