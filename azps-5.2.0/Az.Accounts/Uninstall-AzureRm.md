---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399520"
---
# <span data-ttu-id="8b460-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="8b460-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="8b460-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b460-102">SYNOPSIS</span></span>
<span data-ttu-id="8b460-103">Tar bort alla AzureRm-moduler från en dator.</span><span class="sxs-lookup"><span data-stu-id="8b460-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="8b460-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b460-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b460-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b460-105">DESCRIPTION</span></span>
<span data-ttu-id="8b460-106">Tar bort alla AzureRm-moduler från en dator.</span><span class="sxs-lookup"><span data-stu-id="8b460-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="8b460-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b460-107">EXAMPLES</span></span>

### <span data-ttu-id="8b460-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8b460-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="8b460-109">Om du kör det här kommandot tas alla AzureRm-moduler bort från datorn för den version av PowerShell som cmdleten körs på.</span><span class="sxs-lookup"><span data-stu-id="8b460-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="8b460-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b460-110">PARAMETERS</span></span>

### <span data-ttu-id="8b460-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b460-111">-DefaultProfile</span></span>
<span data-ttu-id="8b460-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b460-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b460-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b460-113">-PassThru</span></span>
<span data-ttu-id="8b460-114">En lista över moduler som tagits bort om angivet.</span><span class="sxs-lookup"><span data-stu-id="8b460-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="8b460-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b460-115">-Confirm</span></span>
<span data-ttu-id="8b460-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b460-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b460-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b460-117">-WhatIf</span></span>
<span data-ttu-id="8b460-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b460-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b460-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b460-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b460-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b460-120">CommonParameters</span></span>
<span data-ttu-id="8b460-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b460-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b460-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b460-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b460-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b460-123">INPUTS</span></span>

### <span data-ttu-id="8b460-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="8b460-124">None</span></span>

## <span data-ttu-id="8b460-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b460-125">OUTPUTS</span></span>

### <span data-ttu-id="8b460-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8b460-126">System.String</span></span>

## <span data-ttu-id="8b460-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b460-127">NOTES</span></span>

## <span data-ttu-id="8b460-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b460-128">RELATED LINKS</span></span>
