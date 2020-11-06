---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroupSubscription.md
ms.openlocfilehash: 882583c50db8a4b4473bce829aab120a68478434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573910"
---
# <span data-ttu-id="919de-101">Remove-AzureRmManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="919de-101">Remove-AzureRmManagementGroupSubscription</span></span>

## <span data-ttu-id="919de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="919de-102">SYNOPSIS</span></span>
<span data-ttu-id="919de-103">Tar bort ett abonnemang från en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="919de-103">Removes a Subscription from a Management Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="919de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="919de-104">SYNTAX</span></span>

```
Remove-AzureRmManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="919de-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="919de-105">DESCRIPTION</span></span>
<span data-ttu-id="919de-106">Cmdleten **Remove-AzureRmManagementGroupSubscription** tar bort ett abonnemang från en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="919de-106">The **Remove-AzureRmManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="919de-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="919de-107">EXAMPLES</span></span>

### <span data-ttu-id="919de-108">Exempel 1 – ta bort abonnemang från en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="919de-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="919de-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="919de-109">PARAMETERS</span></span>

### <span data-ttu-id="919de-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="919de-110">-DefaultProfile</span></span>
<span data-ttu-id="919de-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="919de-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="919de-112">-Grupp namn</span><span class="sxs-lookup"><span data-stu-id="919de-112">-GroupName</span></span>
<span data-ttu-id="919de-113">Hanterings grupp-ID</span><span class="sxs-lookup"><span data-stu-id="919de-113">Management Group Id</span></span>

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

### <span data-ttu-id="919de-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="919de-114">-PassThru</span></span>
<span data-ttu-id="919de-115">Retur `true` vid lyckad körning</span><span class="sxs-lookup"><span data-stu-id="919de-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="919de-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="919de-116">-SubscriptionId</span></span>
<span data-ttu-id="919de-117">Abonnemangs-ID för abonnemanget som är kopplat till hanteringen</span><span class="sxs-lookup"><span data-stu-id="919de-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="919de-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="919de-118">-Confirm</span></span>
<span data-ttu-id="919de-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="919de-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="919de-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="919de-120">-WhatIf</span></span>
<span data-ttu-id="919de-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="919de-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="919de-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="919de-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="919de-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919de-123">CommonParameters</span></span>
<span data-ttu-id="919de-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="919de-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="919de-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="919de-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919de-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="919de-126">INPUTS</span></span>

### <span data-ttu-id="919de-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="919de-127">None</span></span>

## <span data-ttu-id="919de-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="919de-128">OUTPUTS</span></span>

### <span data-ttu-id="919de-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="919de-129">System.Boolean</span></span>

## <span data-ttu-id="919de-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="919de-130">NOTES</span></span>

## <span data-ttu-id="919de-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="919de-131">RELATED LINKS</span></span>
