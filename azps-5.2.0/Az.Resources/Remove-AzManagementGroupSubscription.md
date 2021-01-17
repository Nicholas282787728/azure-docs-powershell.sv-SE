---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: 843a510376e49a1416129d719c141d72ec80df35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408144"
---
# <span data-ttu-id="fd6b3-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="fd6b3-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="fd6b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="fd6b3-103">Tar bort ett abonnemang från en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="fd6b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd6b3-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd6b3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd6b3-105">DESCRIPTION</span></span>
<span data-ttu-id="fd6b3-106">Cmdleten **Remove-AzManagementGroupSubscription** tar bort ett abonnemang från en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="fd6b3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd6b3-107">EXAMPLES</span></span>

### <span data-ttu-id="fd6b3-108">Exempel 1: ta bort abonnemang från en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="fd6b3-108">Example 1: Remove Subscription from a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="fd6b3-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd6b3-109">PARAMETERS</span></span>

### <span data-ttu-id="fd6b3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd6b3-110">-DefaultProfile</span></span>
<span data-ttu-id="fd6b3-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd6b3-112">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="fd6b3-112">-GroupName</span></span>
<span data-ttu-id="fd6b3-113">Hanterings grupp-ID</span><span class="sxs-lookup"><span data-stu-id="fd6b3-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd6b3-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd6b3-114">-PassThru</span></span>
<span data-ttu-id="fd6b3-115">Retur `true` vid lyckad körning</span><span class="sxs-lookup"><span data-stu-id="fd6b3-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="fd6b3-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd6b3-116">-SubscriptionId</span></span>
<span data-ttu-id="fd6b3-117">Prenumerations-ID för abonnemanget som är kopplat till hanteringen</span><span class="sxs-lookup"><span data-stu-id="fd6b3-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="fd6b3-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fd6b3-118">-Confirm</span></span>
<span data-ttu-id="fd6b3-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd6b3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd6b3-120">-WhatIf</span></span>
<span data-ttu-id="fd6b3-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd6b3-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd6b3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd6b3-123">CommonParameters</span></span>
<span data-ttu-id="fd6b3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd6b3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd6b3-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd6b3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd6b3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd6b3-126">INPUTS</span></span>

### <span data-ttu-id="fd6b3-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="fd6b3-127">None</span></span>

## <span data-ttu-id="fd6b3-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd6b3-128">OUTPUTS</span></span>

### <span data-ttu-id="fd6b3-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd6b3-129">System.Boolean</span></span>

## <span data-ttu-id="fd6b3-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd6b3-130">NOTES</span></span>

## <span data-ttu-id="fd6b3-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd6b3-131">RELATED LINKS</span></span>
