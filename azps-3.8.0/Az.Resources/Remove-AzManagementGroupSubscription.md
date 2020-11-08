---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: 1f549f86d2fd9313b8d69f02ebcaeccf2f248d4c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089488"
---
# <span data-ttu-id="a44a4-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="a44a4-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="a44a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a44a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a44a4-103">Tar bort ett abonnemang från en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="a44a4-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="a44a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a44a4-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a44a4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a44a4-105">DESCRIPTION</span></span>
<span data-ttu-id="a44a4-106">Cmdleten **Remove-AzManagementGroupSubscription** tar bort ett abonnemang från en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="a44a4-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="a44a4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a44a4-107">EXAMPLES</span></span>

### <span data-ttu-id="a44a4-108">Exempel 1 – ta bort abonnemang från en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="a44a4-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="a44a4-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a44a4-109">PARAMETERS</span></span>

### <span data-ttu-id="a44a4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a44a4-110">-DefaultProfile</span></span>
<span data-ttu-id="a44a4-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a44a4-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a44a4-112">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="a44a4-112">-GroupName</span></span>
<span data-ttu-id="a44a4-113">Hanterings grupp-ID</span><span class="sxs-lookup"><span data-stu-id="a44a4-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a44a4-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a44a4-114">-PassThru</span></span>
<span data-ttu-id="a44a4-115">Retur `true` vid lyckad körning</span><span class="sxs-lookup"><span data-stu-id="a44a4-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="a44a4-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a44a4-116">-SubscriptionId</span></span>
<span data-ttu-id="a44a4-117">Prenumerations-ID för abonnemanget som är kopplat till hanteringen</span><span class="sxs-lookup"><span data-stu-id="a44a4-117">Subscription Id of the subscription associated with the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a44a4-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a44a4-118">-Confirm</span></span>
<span data-ttu-id="a44a4-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a44a4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a44a4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a44a4-120">-WhatIf</span></span>
<span data-ttu-id="a44a4-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a44a4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a44a4-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a44a4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a44a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a44a4-123">CommonParameters</span></span>
<span data-ttu-id="a44a4-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a44a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a44a4-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a44a4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a44a4-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a44a4-126">INPUTS</span></span>

### <span data-ttu-id="a44a4-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="a44a4-127">None</span></span>

## <span data-ttu-id="a44a4-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a44a4-128">OUTPUTS</span></span>

### <span data-ttu-id="a44a4-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a44a4-129">System.Boolean</span></span>

## <span data-ttu-id="a44a4-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a44a4-130">NOTES</span></span>

## <span data-ttu-id="a44a4-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a44a4-131">RELATED LINKS</span></span>
