---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: d230a00701330caee83d9db6f0a41d4e26446aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745993"
---
# <span data-ttu-id="9bd02-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="9bd02-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="9bd02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9bd02-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd02-103">Inaktiverar alias för AzureRm prefix för AZ-moduler.</span><span class="sxs-lookup"><span data-stu-id="9bd02-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="9bd02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9bd02-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bd02-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9bd02-105">DESCRIPTION</span></span>
<span data-ttu-id="9bd02-106">Inaktiverar alias för AzureRm prefix för AZ-moduler.</span><span class="sxs-lookup"><span data-stu-id="9bd02-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="9bd02-107">Om-modul anges har alias inaktiverats för moduler som visas.</span><span class="sxs-lookup"><span data-stu-id="9bd02-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="9bd02-108">Annars är alla AzureRm-alias inaktiverade.</span><span class="sxs-lookup"><span data-stu-id="9bd02-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="9bd02-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9bd02-109">EXAMPLES</span></span>

### <span data-ttu-id="9bd02-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9bd02-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="9bd02-111">Inaktiverar alla AzureRm-prefix för den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="9bd02-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="9bd02-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9bd02-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="9bd02-113">Inaktiverar AzureRm-alias för AZ. accounts för både den aktuella processen och för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="9bd02-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="9bd02-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9bd02-114">PARAMETERS</span></span>

### <span data-ttu-id="9bd02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd02-115">-DefaultProfile</span></span>
<span data-ttu-id="9bd02-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd02-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bd02-117">-Modul</span><span class="sxs-lookup"><span data-stu-id="9bd02-117">-Module</span></span>
<span data-ttu-id="9bd02-118">Anger vilka moduler du vill inaktivera alias för.</span><span class="sxs-lookup"><span data-stu-id="9bd02-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="9bd02-119">Om ingen anges används alla aktiverade moduler.</span><span class="sxs-lookup"><span data-stu-id="9bd02-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="9bd02-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bd02-120">-PassThru</span></span>
<span data-ttu-id="9bd02-121">Om det anges returnerar cmdlet alla inaktiverade alias</span><span class="sxs-lookup"><span data-stu-id="9bd02-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="9bd02-122">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="9bd02-122">-Scope</span></span>
<span data-ttu-id="9bd02-123">Anger vilka scope-alias som ska inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="9bd02-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="9bd02-124">Standard är "process"</span><span class="sxs-lookup"><span data-stu-id="9bd02-124">Default is 'Process'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd02-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9bd02-125">-Confirm</span></span>
<span data-ttu-id="9bd02-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9bd02-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bd02-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bd02-127">-WhatIf</span></span>
<span data-ttu-id="9bd02-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9bd02-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bd02-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9bd02-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bd02-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd02-130">CommonParameters</span></span>
<span data-ttu-id="9bd02-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd02-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd02-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd02-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd02-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9bd02-133">INPUTS</span></span>

### <span data-ttu-id="9bd02-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="9bd02-134">None</span></span>

## <span data-ttu-id="9bd02-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9bd02-135">OUTPUTS</span></span>

### <span data-ttu-id="9bd02-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9bd02-136">System.String</span></span>

## <span data-ttu-id="9bd02-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9bd02-137">NOTES</span></span>

## <span data-ttu-id="9bd02-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9bd02-138">RELATED LINKS</span></span>
