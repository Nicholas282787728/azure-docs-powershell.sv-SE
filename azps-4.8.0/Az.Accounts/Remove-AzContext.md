---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: d5c31519ba55babb79e3e902a01e46746c5b70f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259634"
---
# <span data-ttu-id="22428-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="22428-101">Remove-AzContext</span></span>

## <span data-ttu-id="22428-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22428-102">SYNOPSIS</span></span>
<span data-ttu-id="22428-103">Ta bort en kontext från uppsättningen tillgängliga kontexter</span><span class="sxs-lookup"><span data-stu-id="22428-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="22428-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22428-104">SYNTAX</span></span>

### <span data-ttu-id="22428-105">RemoveByInputObject (standard)</span><span class="sxs-lookup"><span data-stu-id="22428-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22428-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="22428-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="22428-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22428-107">DESCRIPTION</span></span>
<span data-ttu-id="22428-108">Ta bort en Azure-kontext från uppsättningen kontexter</span><span class="sxs-lookup"><span data-stu-id="22428-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="22428-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22428-109">EXAMPLES</span></span>

### <span data-ttu-id="22428-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="22428-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="22428-111">Ta bort kontexten som standard</span><span class="sxs-lookup"><span data-stu-id="22428-111">Remove the context named default</span></span>

## <span data-ttu-id="22428-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22428-112">PARAMETERS</span></span>

### <span data-ttu-id="22428-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22428-113">-DefaultProfile</span></span>
<span data-ttu-id="22428-114">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22428-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22428-115">-Force</span><span class="sxs-lookup"><span data-stu-id="22428-115">-Force</span></span>
<span data-ttu-id="22428-116">Ta bort kontext även om den är standard</span><span class="sxs-lookup"><span data-stu-id="22428-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="22428-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22428-117">-InputObject</span></span>
<span data-ttu-id="22428-118">Ett kontext objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="22428-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22428-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="22428-119">-Name</span></span>
<span data-ttu-id="22428-120">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="22428-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22428-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22428-121">-PassThru</span></span>
<span data-ttu-id="22428-122">Returnera den borttagna kontexten</span><span class="sxs-lookup"><span data-stu-id="22428-122">Return the removed context</span></span>

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

### <span data-ttu-id="22428-123">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="22428-123">-Scope</span></span>
<span data-ttu-id="22428-124">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som startas av den här användaren</span><span class="sxs-lookup"><span data-stu-id="22428-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="22428-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22428-125">-Confirm</span></span>
<span data-ttu-id="22428-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22428-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22428-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22428-127">-WhatIf</span></span>
<span data-ttu-id="22428-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22428-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22428-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22428-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22428-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22428-130">CommonParameters</span></span>
<span data-ttu-id="22428-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22428-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22428-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22428-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22428-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22428-133">INPUTS</span></span>

### <span data-ttu-id="22428-134">Microsoft. Azure. commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="22428-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="22428-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22428-135">OUTPUTS</span></span>

### <span data-ttu-id="22428-136">Microsoft. Azure. commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="22428-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="22428-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22428-137">NOTES</span></span>

## <span data-ttu-id="22428-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22428-138">RELATED LINKS</span></span>