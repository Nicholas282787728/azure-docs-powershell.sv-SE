---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: 41d43bcb1164907bc7a06a7de4477f8a719604eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746005"
---
# <span data-ttu-id="4f1d2-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="4f1d2-101">Clear-AzDefault</span></span>

## <span data-ttu-id="4f1d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f1d2-102">SYNOPSIS</span></span>
<span data-ttu-id="4f1d2-103">Rensar standardinställningarna som anges av användaren i den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="4f1d2-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="4f1d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f1d2-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f1d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f1d2-105">DESCRIPTION</span></span>
<span data-ttu-id="4f1d2-106">Clear-AzDefault cmdlet tar bort standardvärdena som anges av användaren, beroende på parametrarna som anges av användaren.</span><span class="sxs-lookup"><span data-stu-id="4f1d2-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="4f1d2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f1d2-107">EXAMPLES</span></span>

### <span data-ttu-id="4f1d2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4f1d2-108">Example 1</span></span>
```
PS C:\> Clear-AzDefault
```

<span data-ttu-id="4f1d2-109">Det här kommandot tar bort alla standardinställningar som anges av användaren i den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="4f1d2-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="4f1d2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4f1d2-110">Example 1</span></span>
```
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="4f1d2-111">Det här kommandot tar bort standard resurs gruppen som anges av användaren i den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="4f1d2-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="4f1d2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f1d2-112">PARAMETERS</span></span>

### <span data-ttu-id="4f1d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f1d2-113">-DefaultProfile</span></span>
<span data-ttu-id="4f1d2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f1d2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f1d2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4f1d2-115">-Force</span></span>
<span data-ttu-id="4f1d2-116">Ta bort alla standarder om inget standardvärde anges</span><span class="sxs-lookup"><span data-stu-id="4f1d2-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="4f1d2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f1d2-117">-PassThru</span></span>
<span data-ttu-id="4f1d2-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4f1d2-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4f1d2-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f1d2-119">-ResourceGroup</span></span>
<span data-ttu-id="4f1d2-120">Rensa standard resurs grupp</span><span class="sxs-lookup"><span data-stu-id="4f1d2-120">Clear Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f1d2-121">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="4f1d2-121">-Scope</span></span>
<span data-ttu-id="4f1d2-122">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="4f1d2-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="4f1d2-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f1d2-123">-Confirm</span></span>
<span data-ttu-id="4f1d2-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f1d2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f1d2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f1d2-125">-WhatIf</span></span>
<span data-ttu-id="4f1d2-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f1d2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f1d2-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f1d2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f1d2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f1d2-128">CommonParameters</span></span>
<span data-ttu-id="4f1d2-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f1d2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f1d2-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f1d2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f1d2-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f1d2-131">INPUTS</span></span>

### <span data-ttu-id="4f1d2-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4f1d2-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4f1d2-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f1d2-133">OUTPUTS</span></span>

### <span data-ttu-id="4f1d2-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f1d2-134">System.Boolean</span></span>

## <span data-ttu-id="4f1d2-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f1d2-135">NOTES</span></span>

## <span data-ttu-id="4f1d2-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f1d2-136">RELATED LINKS</span></span>
