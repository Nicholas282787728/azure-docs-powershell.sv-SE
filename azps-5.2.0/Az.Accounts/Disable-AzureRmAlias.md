---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 749507ba0bc0eec8aac7600c5262533ceb02a46b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414960"
---
# <span data-ttu-id="a5b57-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="a5b57-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="a5b57-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5b57-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b57-103">Inaktiverar alias för AzureRm prefix för AZ-moduler.</span><span class="sxs-lookup"><span data-stu-id="a5b57-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="a5b57-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5b57-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5b57-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5b57-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b57-106">Inaktiverar alias för AzureRm prefix för AZ-moduler.</span><span class="sxs-lookup"><span data-stu-id="a5b57-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="a5b57-107">Om-modul anges har alias inaktiverats för moduler som visas.</span><span class="sxs-lookup"><span data-stu-id="a5b57-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="a5b57-108">Annars är alla AzureRm-alias inaktiverade.</span><span class="sxs-lookup"><span data-stu-id="a5b57-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="a5b57-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5b57-109">EXAMPLES</span></span>

### <span data-ttu-id="a5b57-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a5b57-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="a5b57-111">Inaktiverar alla AzureRm-prefix för den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="a5b57-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="a5b57-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a5b57-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="a5b57-113">Inaktiverar AzureRm-alias för AZ. accounts för både den aktuella processen och för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="a5b57-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="a5b57-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5b57-114">PARAMETERS</span></span>

### <span data-ttu-id="a5b57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b57-115">-DefaultProfile</span></span>
<span data-ttu-id="a5b57-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b57-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b57-117">-Modul</span><span class="sxs-lookup"><span data-stu-id="a5b57-117">-Module</span></span>
<span data-ttu-id="a5b57-118">Anger vilka moduler du vill inaktivera alias för.</span><span class="sxs-lookup"><span data-stu-id="a5b57-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="a5b57-119">Om ingen anges används alla aktiverade moduler.</span><span class="sxs-lookup"><span data-stu-id="a5b57-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="a5b57-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5b57-120">-PassThru</span></span>
<span data-ttu-id="a5b57-121">Om det anges returnerar cmdlet alla inaktiverade alias</span><span class="sxs-lookup"><span data-stu-id="a5b57-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="a5b57-122">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="a5b57-122">-Scope</span></span>
<span data-ttu-id="a5b57-123">Anger vilka scope-alias som ska inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="a5b57-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="a5b57-124">Standard är "process"</span><span class="sxs-lookup"><span data-stu-id="a5b57-124">Default is 'Process'</span></span>

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

### <span data-ttu-id="a5b57-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5b57-125">-Confirm</span></span>
<span data-ttu-id="a5b57-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5b57-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b57-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b57-127">-WhatIf</span></span>
<span data-ttu-id="a5b57-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5b57-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b57-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5b57-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b57-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b57-130">CommonParameters</span></span>
<span data-ttu-id="a5b57-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b57-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b57-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5b57-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b57-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5b57-133">INPUTS</span></span>

### <span data-ttu-id="a5b57-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="a5b57-134">None</span></span>

## <span data-ttu-id="a5b57-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5b57-135">OUTPUTS</span></span>

### <span data-ttu-id="a5b57-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a5b57-136">System.String</span></span>

## <span data-ttu-id="a5b57-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5b57-137">NOTES</span></span>

## <span data-ttu-id="a5b57-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5b57-138">RELATED LINKS</span></span>
