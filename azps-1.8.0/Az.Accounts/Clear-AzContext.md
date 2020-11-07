---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b54cfdc68c1f6c400decdac9a1ef0f49823a1712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743548"
---
# <span data-ttu-id="27301-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="27301-101">Clear-AzContext</span></span>

## <span data-ttu-id="27301-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27301-102">SYNOPSIS</span></span>
<span data-ttu-id="27301-103">Ta bort all information om Azure-autentiseringsuppgifter,-konto och-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="27301-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="27301-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27301-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27301-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27301-105">DESCRIPTION</span></span>
<span data-ttu-id="27301-106">Ta bort all information om Azure-autentiseringsuppgifter,-konto och-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="27301-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="27301-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27301-107">EXAMPLES</span></span>

### <span data-ttu-id="27301-108">Rensa global kontext</span><span class="sxs-lookup"><span data-stu-id="27301-108">Clear global context</span></span>
```
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="27301-109">Ta bort all information om konto, prenumeration och autentiseringsinformation för en PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="27301-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="27301-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27301-110">PARAMETERS</span></span>

### <span data-ttu-id="27301-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27301-111">-DefaultProfile</span></span>
<span data-ttu-id="27301-112">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="27301-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27301-113">-Force</span><span class="sxs-lookup"><span data-stu-id="27301-113">-Force</span></span>
<span data-ttu-id="27301-114">Ta bort alla användare och grupper från globalt scope utan att fråga</span><span class="sxs-lookup"><span data-stu-id="27301-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="27301-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27301-115">-PassThru</span></span>
<span data-ttu-id="27301-116">Returnera ett värde som anger om det lyckades eller inte</span><span class="sxs-lookup"><span data-stu-id="27301-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="27301-117">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="27301-117">-Scope</span></span>
<span data-ttu-id="27301-118">Rensa bara kontexten för den aktuella PowerShell-sessionen eller för alla sessioner.</span><span class="sxs-lookup"><span data-stu-id="27301-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="27301-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="27301-119">-Confirm</span></span>
<span data-ttu-id="27301-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="27301-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27301-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27301-121">-WhatIf</span></span>
<span data-ttu-id="27301-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="27301-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27301-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="27301-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27301-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27301-124">CommonParameters</span></span>
<span data-ttu-id="27301-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27301-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27301-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27301-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27301-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27301-127">INPUTS</span></span>

### <span data-ttu-id="27301-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="27301-128">None</span></span>

## <span data-ttu-id="27301-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27301-129">OUTPUTS</span></span>

### <span data-ttu-id="27301-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27301-130">System.Boolean</span></span>

## <span data-ttu-id="27301-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27301-131">NOTES</span></span>

## <span data-ttu-id="27301-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27301-132">RELATED LINKS</span></span>
