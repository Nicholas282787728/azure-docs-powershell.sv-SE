---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: f268c4171be78265843d5a04291bf430dc4f19b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922016"
---
# <span data-ttu-id="a075c-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="a075c-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="a075c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a075c-102">SYNOPSIS</span></span>
<span data-ttu-id="a075c-103">Inaktivera Spara autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="a075c-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="a075c-104">Din inloggnings information blir glömt nästa gång du öppnar ett PowerShell-fönster</span><span class="sxs-lookup"><span data-stu-id="a075c-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="a075c-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a075c-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a075c-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a075c-106">DESCRIPTION</span></span>
<span data-ttu-id="a075c-107">Inaktivera Spara autentiseringsuppgifter för Azure.</span><span class="sxs-lookup"><span data-stu-id="a075c-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="a075c-108">Din inloggnings information blir glömt nästa gång du öppnar ett PowerShell-fönster</span><span class="sxs-lookup"><span data-stu-id="a075c-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="a075c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a075c-109">EXAMPLES</span></span>

### <span data-ttu-id="a075c-110">Inaktivera autosparande av kontexten</span><span class="sxs-lookup"><span data-stu-id="a075c-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="a075c-111">Inaktivera Spara automatiskt för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="a075c-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="a075c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a075c-112">PARAMETERS</span></span>

### <span data-ttu-id="a075c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a075c-113">-DefaultProfile</span></span>
<span data-ttu-id="a075c-114">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a075c-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a075c-115">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="a075c-115">-Scope</span></span>
<span data-ttu-id="a075c-116">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som startas av den här användaren</span><span class="sxs-lookup"><span data-stu-id="a075c-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="a075c-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a075c-117">-Confirm</span></span>
<span data-ttu-id="a075c-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a075c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a075c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a075c-119">-WhatIf</span></span>
<span data-ttu-id="a075c-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a075c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a075c-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a075c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a075c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a075c-122">CommonParameters</span></span>
<span data-ttu-id="a075c-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a075c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a075c-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a075c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a075c-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a075c-125">INPUTS</span></span>

### <span data-ttu-id="a075c-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="a075c-126">None</span></span>

## <span data-ttu-id="a075c-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a075c-127">OUTPUTS</span></span>

### <span data-ttu-id="a075c-128">Microsoft. Azure. kommandon. Common. inloggningsautentisering. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="a075c-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="a075c-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a075c-129">NOTES</span></span>

## <span data-ttu-id="a075c-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a075c-130">RELATED LINKS</span></span>