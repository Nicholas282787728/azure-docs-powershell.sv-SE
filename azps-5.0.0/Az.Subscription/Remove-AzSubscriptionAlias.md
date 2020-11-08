---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 02a32b3e6c39ae66aea8efc37213a6fb3bca0848
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271203"
---
# <span data-ttu-id="e8c76-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="e8c76-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="e8c76-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8c76-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c76-103">Tar bort det här abonnemangs Ali Aset</span><span class="sxs-lookup"><span data-stu-id="e8c76-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="e8c76-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8c76-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8c76-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8c76-105">DESCRIPTION</span></span>
<span data-ttu-id="e8c76-106">Cmdleten **Remove-AzSubscriptionAlias** tar bort ditt prenumerations-alias</span><span class="sxs-lookup"><span data-stu-id="e8c76-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="e8c76-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8c76-107">EXAMPLES</span></span>

### <span data-ttu-id="e8c76-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e8c76-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="e8c76-109">Tar bort det här abonnemangs Ali Aset</span><span class="sxs-lookup"><span data-stu-id="e8c76-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="e8c76-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8c76-110">PARAMETERS</span></span>

### <span data-ttu-id="e8c76-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="e8c76-111">-AliasName</span></span>
<span data-ttu-id="e8c76-112">Alias för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="e8c76-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8c76-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8c76-113">-AsJob</span></span>
<span data-ttu-id="e8c76-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e8c76-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8c76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c76-115">-DefaultProfile</span></span>
<span data-ttu-id="e8c76-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e8c76-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8c76-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e8c76-117">-Confirm</span></span>
<span data-ttu-id="e8c76-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e8c76-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8c76-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8c76-119">-WhatIf</span></span>
<span data-ttu-id="e8c76-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e8c76-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8c76-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e8c76-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8c76-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c76-122">CommonParameters</span></span>
<span data-ttu-id="e8c76-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8c76-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c76-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8c76-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c76-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8c76-125">INPUTS</span></span>

### <span data-ttu-id="e8c76-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="e8c76-126">None</span></span>

## <span data-ttu-id="e8c76-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8c76-127">OUTPUTS</span></span>

### <span data-ttu-id="e8c76-128">Microsoft. Azure. commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="e8c76-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="e8c76-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8c76-129">NOTES</span></span>

## <span data-ttu-id="e8c76-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8c76-130">RELATED LINKS</span></span>
