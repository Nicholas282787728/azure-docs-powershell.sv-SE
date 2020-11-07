---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 24862931e19d0e8b8c7b8568aabb6f25cf65f9c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745988"
---
# <span data-ttu-id="59506-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="59506-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="59506-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59506-102">SYNOPSIS</span></span>
<span data-ttu-id="59506-103">Aktiverar AzureRm prefix för AZ-moduler.</span><span class="sxs-lookup"><span data-stu-id="59506-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="59506-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59506-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59506-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59506-105">DESCRIPTION</span></span>
<span data-ttu-id="59506-106">Aktiverar AzureRm prefix för AZ-moduler.</span><span class="sxs-lookup"><span data-stu-id="59506-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="59506-107">IF-module anges har alias aktiverat för moduler som visas.</span><span class="sxs-lookup"><span data-stu-id="59506-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="59506-108">Annars är alla AzureRm-alias aktiverade.</span><span class="sxs-lookup"><span data-stu-id="59506-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="59506-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59506-109">EXAMPLES</span></span>

### <span data-ttu-id="59506-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="59506-110">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="59506-111">Aktiverar alla AzureRm prefix för den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="59506-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="59506-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="59506-112">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="59506-113">Aktiverar AzureRm alias för AZ. accounts för både den aktuella processen och för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="59506-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="59506-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59506-114">PARAMETERS</span></span>

### <span data-ttu-id="59506-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59506-115">-DefaultProfile</span></span>
<span data-ttu-id="59506-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59506-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59506-117">-Modul</span><span class="sxs-lookup"><span data-stu-id="59506-117">-Module</span></span>
<span data-ttu-id="59506-118">Anger vilka moduler som ska aktivera alias för.</span><span class="sxs-lookup"><span data-stu-id="59506-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="59506-119">Om ingen anges är standard alla moduler.</span><span class="sxs-lookup"><span data-stu-id="59506-119">If none are specified, default is all modules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59506-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59506-120">-PassThru</span></span>
<span data-ttu-id="59506-121">Om det här alternativet anges returnerar cmdleten alla aktiverade alias</span><span class="sxs-lookup"><span data-stu-id="59506-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="59506-122">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="59506-122">-Scope</span></span>
<span data-ttu-id="59506-123">Anger vilka scope-alias som ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="59506-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="59506-124">Standard är "lokal"</span><span class="sxs-lookup"><span data-stu-id="59506-124">Default is 'Local'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59506-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59506-125">-Confirm</span></span>
<span data-ttu-id="59506-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59506-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59506-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59506-127">-WhatIf</span></span>
<span data-ttu-id="59506-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59506-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59506-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59506-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59506-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59506-130">CommonParameters</span></span>
<span data-ttu-id="59506-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59506-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59506-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59506-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59506-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59506-133">INPUTS</span></span>

### <span data-ttu-id="59506-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="59506-134">None</span></span>

## <span data-ttu-id="59506-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59506-135">OUTPUTS</span></span>

### <span data-ttu-id="59506-136">System. String</span><span class="sxs-lookup"><span data-stu-id="59506-136">System.String</span></span>

## <span data-ttu-id="59506-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59506-137">NOTES</span></span>

## <span data-ttu-id="59506-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59506-138">RELATED LINKS</span></span>
