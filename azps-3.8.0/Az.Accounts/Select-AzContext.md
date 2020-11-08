---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
ms.openlocfilehash: 6f3ff6868a34eefc9b7cd45cf371b6ef29dbf469
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089724"
---
# <span data-ttu-id="262e1-101">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="262e1-101">Select-AzContext</span></span>

## <span data-ttu-id="262e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="262e1-102">SYNOPSIS</span></span>
<span data-ttu-id="262e1-103">Välja ett abonnemang och konto för mål i Azure PowerShell-cmdletar</span><span class="sxs-lookup"><span data-stu-id="262e1-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

## <span data-ttu-id="262e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="262e1-104">SYNTAX</span></span>

### <span data-ttu-id="262e1-105">SelectByInputObject (standard)</span><span class="sxs-lookup"><span data-stu-id="262e1-105">SelectByInputObject (Default)</span></span>
```
Select-AzContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262e1-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="262e1-106">SelectByName</span></span>
```
Select-AzContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="262e1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="262e1-107">DESCRIPTION</span></span>
<span data-ttu-id="262e1-108">Välj ett abonnemang för mål (eller konto eller innehavare) i Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="262e1-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="262e1-109">Efter denna cmdlet används den valda kontexten för framtida cmdletar.</span><span class="sxs-lookup"><span data-stu-id="262e1-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="262e1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="262e1-110">EXAMPLES</span></span>

### <span data-ttu-id="262e1-111">Exempel 1: rikta en namngiven kontext</span><span class="sxs-lookup"><span data-stu-id="262e1-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzContext "Work"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="262e1-112">Mål framtida cmdlets för Azure PowerShell på kontot, innehavaren och prenumerationen i kontexten "arbete".</span><span class="sxs-lookup"><span data-stu-id="262e1-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="262e1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="262e1-113">PARAMETERS</span></span>

### <span data-ttu-id="262e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262e1-114">-DefaultProfile</span></span>
<span data-ttu-id="262e1-115">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="262e1-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="262e1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="262e1-116">-InputObject</span></span>
<span data-ttu-id="262e1-117">Ett kontext objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="262e1-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: SelectByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="262e1-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="262e1-118">-Name</span></span>
<span data-ttu-id="262e1-119">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="262e1-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: SelectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="262e1-120">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="262e1-120">-Scope</span></span>
<span data-ttu-id="262e1-121">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som startas av den här användaren</span><span class="sxs-lookup"><span data-stu-id="262e1-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="262e1-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="262e1-122">-Confirm</span></span>
<span data-ttu-id="262e1-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="262e1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="262e1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="262e1-124">-WhatIf</span></span>
<span data-ttu-id="262e1-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="262e1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="262e1-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="262e1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="262e1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262e1-127">CommonParameters</span></span>
<span data-ttu-id="262e1-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="262e1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262e1-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="262e1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262e1-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="262e1-130">INPUTS</span></span>

### <span data-ttu-id="262e1-131">Microsoft. Azure. commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="262e1-131">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="262e1-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="262e1-132">OUTPUTS</span></span>

### <span data-ttu-id="262e1-133">Microsoft. Azure. commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="262e1-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="262e1-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="262e1-134">NOTES</span></span>

## <span data-ttu-id="262e1-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="262e1-135">RELATED LINKS</span></span>