---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroupSubscription.md
ms.openlocfilehash: a3c75c653d75a4fde969672a245644ee04412731
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572628"
---
# <span data-ttu-id="169a4-101">New-AzureRmManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="169a4-101">New-AzureRmManagementGroupSubscription</span></span>

## <span data-ttu-id="169a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="169a4-102">SYNOPSIS</span></span>
<span data-ttu-id="169a4-103">Lägger till ett abonnemang i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="169a4-103">Adds a Subscription to a Management Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="169a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="169a4-104">SYNTAX</span></span>

```
New-AzureRmManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="169a4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="169a4-105">DESCRIPTION</span></span>
<span data-ttu-id="169a4-106">Cmdleten **New-AzureRMManagementGroupSubscription** lägger till en prenumeration i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="169a4-106">The **New-AzureRMManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="169a4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="169a4-107">EXAMPLES</span></span>

### <span data-ttu-id="169a4-108">Exempel 1: lägga till ett abonnemang i en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="169a4-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzureRMManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="169a4-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="169a4-109">PARAMETERS</span></span>

### <span data-ttu-id="169a4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="169a4-110">-DefaultProfile</span></span>
<span data-ttu-id="169a4-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="169a4-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169a4-112">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="169a4-112">-GroupName</span></span>
<span data-ttu-id="169a4-113">Hanterings grupp-ID</span><span class="sxs-lookup"><span data-stu-id="169a4-113">Management Group Id</span></span>

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

### <span data-ttu-id="169a4-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="169a4-114">-PassThru</span></span>
<span data-ttu-id="169a4-115">Retur `true` vid lyckad körning</span><span class="sxs-lookup"><span data-stu-id="169a4-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="169a4-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="169a4-116">-SubscriptionId</span></span>
<span data-ttu-id="169a4-117">Abonnemangs-ID för abonnemanget som är kopplat till hanteringen</span><span class="sxs-lookup"><span data-stu-id="169a4-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="169a4-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="169a4-118">-Confirm</span></span>
<span data-ttu-id="169a4-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="169a4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="169a4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="169a4-120">-WhatIf</span></span>
<span data-ttu-id="169a4-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="169a4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="169a4-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="169a4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="169a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169a4-123">CommonParameters</span></span>
<span data-ttu-id="169a4-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="169a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169a4-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="169a4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169a4-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="169a4-126">INPUTS</span></span>

### <span data-ttu-id="169a4-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="169a4-127">None</span></span>

## <span data-ttu-id="169a4-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="169a4-128">OUTPUTS</span></span>

### <span data-ttu-id="169a4-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="169a4-129">System.Boolean</span></span>

## <span data-ttu-id="169a4-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="169a4-130">NOTES</span></span>

## <span data-ttu-id="169a4-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="169a4-131">RELATED LINKS</span></span>
