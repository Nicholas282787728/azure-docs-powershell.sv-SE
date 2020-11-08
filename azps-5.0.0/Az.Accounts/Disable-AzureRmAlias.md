---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 749507ba0bc0eec8aac7600c5262533ceb02a46b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271500"
---
# <span data-ttu-id="54165-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="54165-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="54165-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54165-102">SYNOPSIS</span></span>
<span data-ttu-id="54165-103">Inaktiverar alias för AzureRm prefix för AZ-moduler.</span><span class="sxs-lookup"><span data-stu-id="54165-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="54165-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54165-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54165-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54165-105">DESCRIPTION</span></span>
<span data-ttu-id="54165-106">Inaktiverar alias för AzureRm prefix för AZ-moduler.</span><span class="sxs-lookup"><span data-stu-id="54165-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="54165-107">Om-modul anges har alias inaktiverats för moduler som visas.</span><span class="sxs-lookup"><span data-stu-id="54165-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="54165-108">Annars är alla AzureRm-alias inaktiverade.</span><span class="sxs-lookup"><span data-stu-id="54165-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="54165-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54165-109">EXAMPLES</span></span>

### <span data-ttu-id="54165-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54165-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="54165-111">Inaktiverar alla AzureRm-prefix för den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="54165-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="54165-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54165-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="54165-113">Inaktiverar AzureRm-alias för AZ. accounts för både den aktuella processen och för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="54165-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="54165-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54165-114">PARAMETERS</span></span>

### <span data-ttu-id="54165-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54165-115">-DefaultProfile</span></span>
<span data-ttu-id="54165-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54165-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54165-117">-Modul</span><span class="sxs-lookup"><span data-stu-id="54165-117">-Module</span></span>
<span data-ttu-id="54165-118">Anger vilka moduler du vill inaktivera alias för.</span><span class="sxs-lookup"><span data-stu-id="54165-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="54165-119">Om ingen anges används alla aktiverade moduler.</span><span class="sxs-lookup"><span data-stu-id="54165-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="54165-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54165-120">-PassThru</span></span>
<span data-ttu-id="54165-121">Om det anges returnerar cmdlet alla inaktiverade alias</span><span class="sxs-lookup"><span data-stu-id="54165-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="54165-122">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="54165-122">-Scope</span></span>
<span data-ttu-id="54165-123">Anger vilka scope-alias som ska inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="54165-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="54165-124">Standard är "process"</span><span class="sxs-lookup"><span data-stu-id="54165-124">Default is 'Process'</span></span>

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

### <span data-ttu-id="54165-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54165-125">-Confirm</span></span>
<span data-ttu-id="54165-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54165-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54165-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54165-127">-WhatIf</span></span>
<span data-ttu-id="54165-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54165-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54165-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54165-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54165-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54165-130">CommonParameters</span></span>
<span data-ttu-id="54165-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54165-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54165-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54165-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54165-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54165-133">INPUTS</span></span>

### <span data-ttu-id="54165-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="54165-134">None</span></span>

## <span data-ttu-id="54165-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54165-135">OUTPUTS</span></span>

### <span data-ttu-id="54165-136">System. String</span><span class="sxs-lookup"><span data-stu-id="54165-136">System.String</span></span>

## <span data-ttu-id="54165-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54165-137">NOTES</span></span>

## <span data-ttu-id="54165-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54165-138">RELATED LINKS</span></span>
