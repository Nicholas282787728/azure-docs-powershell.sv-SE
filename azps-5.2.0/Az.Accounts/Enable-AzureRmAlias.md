---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 6a530a0e20f3e69540320ad3eab8b8cc7f37b5af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393248"
---
# <span data-ttu-id="6e3b4-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="6e3b4-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="6e3b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="6e3b4-103">Aktiverar AzureRm prefix för AZ-moduler.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="6e3b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e3b4-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e3b4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e3b4-105">DESCRIPTION</span></span>
<span data-ttu-id="6e3b4-106">Aktiverar AzureRm prefix för AZ-moduler.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="6e3b4-107">IF-module anges har alias aktiverat för moduler som visas.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="6e3b4-108">Annars är alla AzureRm-alias aktiverade.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="6e3b4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e3b4-109">EXAMPLES</span></span>

### <span data-ttu-id="6e3b4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6e3b4-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="6e3b4-111">Aktiverar alla AzureRm prefix för den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="6e3b4-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6e3b4-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="6e3b4-113">Aktiverar AzureRm alias för AZ. accounts för både den aktuella processen och för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="6e3b4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e3b4-114">PARAMETERS</span></span>

### <span data-ttu-id="6e3b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e3b4-115">-DefaultProfile</span></span>
<span data-ttu-id="6e3b4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e3b4-117">-Modul</span><span class="sxs-lookup"><span data-stu-id="6e3b4-117">-Module</span></span>
<span data-ttu-id="6e3b4-118">Anger vilka moduler som ska aktivera alias för.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="6e3b4-119">Om ingen anges är standard alla moduler.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="6e3b4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e3b4-120">-PassThru</span></span>
<span data-ttu-id="6e3b4-121">Om det här alternativet anges returnerar cmdleten alla aktiverade alias</span><span class="sxs-lookup"><span data-stu-id="6e3b4-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="6e3b4-122">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="6e3b4-122">-Scope</span></span>
<span data-ttu-id="6e3b4-123">Anger vilka scope-alias som ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="6e3b4-124">Standard är "lokal"</span><span class="sxs-lookup"><span data-stu-id="6e3b4-124">Default is 'Local'</span></span>

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

### <span data-ttu-id="6e3b4-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6e3b4-125">-Confirm</span></span>
<span data-ttu-id="6e3b4-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e3b4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e3b4-127">-WhatIf</span></span>
<span data-ttu-id="6e3b4-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e3b4-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e3b4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e3b4-130">CommonParameters</span></span>
<span data-ttu-id="6e3b4-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e3b4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e3b4-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e3b4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e3b4-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e3b4-133">INPUTS</span></span>

### <span data-ttu-id="6e3b4-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="6e3b4-134">None</span></span>

## <span data-ttu-id="6e3b4-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e3b4-135">OUTPUTS</span></span>

### <span data-ttu-id="6e3b4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6e3b4-136">System.String</span></span>

## <span data-ttu-id="6e3b4-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e3b4-137">NOTES</span></span>

## <span data-ttu-id="6e3b4-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e3b4-138">RELATED LINKS</span></span>
