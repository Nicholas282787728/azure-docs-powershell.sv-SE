---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: c5d01fcc7ba007a0336fac5c08db44b840e75806
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090756"
---
# <span data-ttu-id="c3d46-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="c3d46-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="c3d46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3d46-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d46-103">Inaktivera Spara autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d46-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="c3d46-104">Din inloggnings information blir glömt nästa gång du öppnar ett PowerShell-fönster</span><span class="sxs-lookup"><span data-stu-id="c3d46-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="c3d46-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3d46-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3d46-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3d46-106">DESCRIPTION</span></span>
<span data-ttu-id="c3d46-107">Inaktivera Spara autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d46-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="c3d46-108">Din inloggnings information blir glömt nästa gång du öppnar ett PowerShell-fönster</span><span class="sxs-lookup"><span data-stu-id="c3d46-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="c3d46-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3d46-109">EXAMPLES</span></span>

### <span data-ttu-id="c3d46-110">Inaktivera autosparande av kontexten</span><span class="sxs-lookup"><span data-stu-id="c3d46-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="c3d46-111">Inaktivera Spara automatiskt för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="c3d46-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="c3d46-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3d46-112">PARAMETERS</span></span>

### <span data-ttu-id="c3d46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d46-113">-DefaultProfile</span></span>
<span data-ttu-id="c3d46-114">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c3d46-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d46-115">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="c3d46-115">-Scope</span></span>
<span data-ttu-id="c3d46-116">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som startas av den här användaren</span><span class="sxs-lookup"><span data-stu-id="c3d46-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="c3d46-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3d46-117">-Confirm</span></span>
<span data-ttu-id="c3d46-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3d46-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3d46-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3d46-119">-WhatIf</span></span>
<span data-ttu-id="c3d46-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3d46-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3d46-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3d46-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3d46-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d46-122">CommonParameters</span></span>
<span data-ttu-id="c3d46-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d46-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d46-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3d46-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d46-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3d46-125">INPUTS</span></span>

### <span data-ttu-id="c3d46-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="c3d46-126">None</span></span>

## <span data-ttu-id="c3d46-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3d46-127">OUTPUTS</span></span>

### <span data-ttu-id="c3d46-128">Microsoft. Azure. kommandon. Common. inloggningsautentisering. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="c3d46-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="c3d46-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3d46-129">NOTES</span></span>

## <span data-ttu-id="c3d46-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3d46-130">RELATED LINKS</span></span>
