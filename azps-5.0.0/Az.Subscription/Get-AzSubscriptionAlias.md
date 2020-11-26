---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271208"
---
# <span data-ttu-id="fe2f7-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="fe2f7-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="fe2f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe2f7-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2f7-103">Får information om prenumerations Ali Aset</span><span class="sxs-lookup"><span data-stu-id="fe2f7-103">Gets subscription alias details</span></span>

## <span data-ttu-id="fe2f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe2f7-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe2f7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe2f7-105">DESCRIPTION</span></span>
<span data-ttu-id="fe2f7-106">Cmdleten **Get-AzSubscriptionAlias** får information om prenumerations Ali Aset.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="fe2f7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe2f7-107">EXAMPLES</span></span>

### <span data-ttu-id="fe2f7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fe2f7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="fe2f7-109">Får information om prenumerations Ali Aset</span><span class="sxs-lookup"><span data-stu-id="fe2f7-109">Gets subscription alias details</span></span>

## <span data-ttu-id="fe2f7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe2f7-110">PARAMETERS</span></span>

### <span data-ttu-id="fe2f7-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="fe2f7-111">-AliasName</span></span>
<span data-ttu-id="fe2f7-112">Alias för abonnemanget</span><span class="sxs-lookup"><span data-stu-id="fe2f7-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2f7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe2f7-113">-AsJob</span></span>
<span data-ttu-id="fe2f7-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="fe2f7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe2f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2f7-115">-DefaultProfile</span></span>
<span data-ttu-id="fe2f7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe2f7-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe2f7-117">-Confirm</span></span>
<span data-ttu-id="fe2f7-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe2f7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe2f7-119">-WhatIf</span></span>
<span data-ttu-id="fe2f7-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe2f7-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe2f7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2f7-122">CommonParameters</span></span>
<span data-ttu-id="fe2f7-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe2f7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2f7-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe2f7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2f7-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe2f7-125">INPUTS</span></span>

### <span data-ttu-id="fe2f7-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="fe2f7-126">None</span></span>

## <span data-ttu-id="fe2f7-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe2f7-127">OUTPUTS</span></span>

### <span data-ttu-id="fe2f7-128">Microsoft. Azure. commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="fe2f7-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="fe2f7-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe2f7-129">NOTES</span></span>

## <span data-ttu-id="fe2f7-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe2f7-130">RELATED LINKS</span></span>