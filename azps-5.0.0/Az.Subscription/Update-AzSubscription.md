---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 77e7904a83b7d14fac1379532a619547888d5542
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271201"
---
# <span data-ttu-id="0c925-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="0c925-101">Update-AzSubscription</span></span>

## <span data-ttu-id="0c925-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c925-102">SYNOPSIS</span></span>
<span data-ttu-id="0c925-103">Uppdaterar en Azure-prenumeration</span><span class="sxs-lookup"><span data-stu-id="0c925-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="0c925-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c925-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c925-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c925-105">DESCRIPTION</span></span>
<span data-ttu-id="0c925-106">Cmdleten **Update-AzSubscription** uppdaterar en Azure-prenumeration</span><span class="sxs-lookup"><span data-stu-id="0c925-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="0c925-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c925-107">EXAMPLES</span></span>

### <span data-ttu-id="0c925-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0c925-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="0c925-109">Uppdaterar abonnemanget</span><span class="sxs-lookup"><span data-stu-id="0c925-109">Updates the subscription</span></span>

## <span data-ttu-id="0c925-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c925-110">PARAMETERS</span></span>

### <span data-ttu-id="0c925-111">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="0c925-111">-Action</span></span>
<span data-ttu-id="0c925-112">Åtgärd att utföra med abonnemang</span><span class="sxs-lookup"><span data-stu-id="0c925-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="0c925-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c925-113">-AsJob</span></span>
<span data-ttu-id="0c925-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0c925-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c925-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c925-115">-DefaultProfile</span></span>
<span data-ttu-id="0c925-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c925-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c925-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="0c925-117">-Name</span></span>
<span data-ttu-id="0c925-118">Namnet på abonnemanget</span><span class="sxs-lookup"><span data-stu-id="0c925-118">Name of the subscription</span></span>

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

### <span data-ttu-id="0c925-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c925-119">-SubscriptionId</span></span>
<span data-ttu-id="0c925-120">Prenumerations-ID att uppdatera</span><span class="sxs-lookup"><span data-stu-id="0c925-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="0c925-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0c925-121">-Confirm</span></span>
<span data-ttu-id="0c925-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0c925-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c925-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c925-123">-WhatIf</span></span>
<span data-ttu-id="0c925-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0c925-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c925-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0c925-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c925-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c925-126">CommonParameters</span></span>
<span data-ttu-id="0c925-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c925-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c925-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c925-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c925-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c925-129">INPUTS</span></span>

### <span data-ttu-id="0c925-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="0c925-130">None</span></span>

## <span data-ttu-id="0c925-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c925-131">OUTPUTS</span></span>

### <span data-ttu-id="0c925-132">Microsoft. Azure. commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="0c925-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="0c925-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c925-133">NOTES</span></span>

## <span data-ttu-id="0c925-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c925-134">RELATED LINKS</span></span>
