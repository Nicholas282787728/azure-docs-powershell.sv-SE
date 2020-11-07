---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: b3983d63beecb7d5a45f31409758b98aa64786a3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923926"
---
# <span data-ttu-id="91ecf-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="91ecf-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="91ecf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="91ecf-103">Lägger till ett abonnemang i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="91ecf-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="91ecf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91ecf-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91ecf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="91ecf-106">Cmdleten **New-AzManagementGroupSubscription** lägger till en prenumeration i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="91ecf-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="91ecf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91ecf-107">EXAMPLES</span></span>

### <span data-ttu-id="91ecf-108">Exempel 1: lägga till ett abonnemang i en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="91ecf-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="91ecf-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91ecf-109">PARAMETERS</span></span>

### <span data-ttu-id="91ecf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ecf-110">-DefaultProfile</span></span>
<span data-ttu-id="91ecf-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91ecf-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ecf-112">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="91ecf-112">-GroupName</span></span>
<span data-ttu-id="91ecf-113">Hanterings grupp-ID</span><span class="sxs-lookup"><span data-stu-id="91ecf-113">Management Group Id</span></span>

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

### <span data-ttu-id="91ecf-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91ecf-114">-PassThru</span></span>
<span data-ttu-id="91ecf-115">Retur `true` vid lyckad körning</span><span class="sxs-lookup"><span data-stu-id="91ecf-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="91ecf-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91ecf-116">-SubscriptionId</span></span>
<span data-ttu-id="91ecf-117">Abonnemangs-ID för abonnemanget som är kopplat till hanteringen</span><span class="sxs-lookup"><span data-stu-id="91ecf-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="91ecf-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="91ecf-118">-Confirm</span></span>
<span data-ttu-id="91ecf-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="91ecf-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91ecf-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91ecf-120">-WhatIf</span></span>
<span data-ttu-id="91ecf-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="91ecf-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91ecf-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="91ecf-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91ecf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ecf-123">CommonParameters</span></span>
<span data-ttu-id="91ecf-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91ecf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ecf-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91ecf-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ecf-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91ecf-126">INPUTS</span></span>

### <span data-ttu-id="91ecf-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="91ecf-127">None</span></span>

## <span data-ttu-id="91ecf-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91ecf-128">OUTPUTS</span></span>

### <span data-ttu-id="91ecf-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91ecf-129">System.Boolean</span></span>

## <span data-ttu-id="91ecf-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91ecf-130">NOTES</span></span>

## <span data-ttu-id="91ecf-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91ecf-131">RELATED LINKS</span></span>
