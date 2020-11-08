---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b808f9272c000ed0ef17079dd31800860a31449b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262844"
---
# <span data-ttu-id="46f97-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="46f97-101">Clear-AzContext</span></span>

## <span data-ttu-id="46f97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46f97-102">SYNOPSIS</span></span>
<span data-ttu-id="46f97-103">Ta bort all information om Azure-autentiseringsuppgifter,-konto och-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="46f97-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="46f97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46f97-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46f97-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46f97-105">DESCRIPTION</span></span>
<span data-ttu-id="46f97-106">Ta bort all information om Azure-autentiseringsuppgifter,-konto och-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="46f97-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="46f97-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46f97-107">EXAMPLES</span></span>

### <span data-ttu-id="46f97-108">Exempel 1: Rensa global kontext</span><span class="sxs-lookup"><span data-stu-id="46f97-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="46f97-109">Ta bort all information om konto, prenumeration och autentiseringsinformation för en PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="46f97-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="46f97-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46f97-110">PARAMETERS</span></span>

### <span data-ttu-id="46f97-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f97-111">-DefaultProfile</span></span>
<span data-ttu-id="46f97-112">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="46f97-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46f97-113">-Force</span><span class="sxs-lookup"><span data-stu-id="46f97-113">-Force</span></span>
<span data-ttu-id="46f97-114">Ta bort alla användare och grupper från globalt scope utan att fråga</span><span class="sxs-lookup"><span data-stu-id="46f97-114">Delete all users and groups from the global scope without prompting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f97-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46f97-115">-PassThru</span></span>
<span data-ttu-id="46f97-116">Returnera ett värde som anger om det lyckades eller inte</span><span class="sxs-lookup"><span data-stu-id="46f97-116">Return a value indicating success or failure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46f97-117">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="46f97-117">-Scope</span></span>
<span data-ttu-id="46f97-118">Rensa bara kontexten för den aktuella PowerShell-sessionen eller för alla sessioner.</span><span class="sxs-lookup"><span data-stu-id="46f97-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="46f97-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="46f97-119">-Confirm</span></span>
<span data-ttu-id="46f97-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="46f97-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46f97-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46f97-121">-WhatIf</span></span>
<span data-ttu-id="46f97-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="46f97-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46f97-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="46f97-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46f97-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f97-124">CommonParameters</span></span>
<span data-ttu-id="46f97-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f97-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f97-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46f97-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f97-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46f97-127">INPUTS</span></span>

### <span data-ttu-id="46f97-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="46f97-128">None</span></span>

## <span data-ttu-id="46f97-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46f97-129">OUTPUTS</span></span>

### <span data-ttu-id="46f97-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46f97-130">System.Boolean</span></span>

## <span data-ttu-id="46f97-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46f97-131">NOTES</span></span>

## <span data-ttu-id="46f97-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46f97-132">RELATED LINKS</span></span>
