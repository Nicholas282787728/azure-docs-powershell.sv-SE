---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 99fb63a5dd4ba60b44e96139418a76701334444e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102227"
---
# <span data-ttu-id="dbd7f-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="dbd7f-101">New-AzActionGroup</span></span>

## <span data-ttu-id="dbd7f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbd7f-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd7f-103">Skapar ett ActionGroup-referens objekt i minnet.</span><span class="sxs-lookup"><span data-stu-id="dbd7f-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="dbd7f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbd7f-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbd7f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbd7f-105">DESCRIPTION</span></span>
<span data-ttu-id="dbd7f-106">Cmdleten **New-AzActionGroup** skapar ett referens objekt i minnet.</span><span class="sxs-lookup"><span data-stu-id="dbd7f-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="dbd7f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbd7f-107">EXAMPLES</span></span>

### <span data-ttu-id="dbd7f-108">Exempel 1: skapa ett referens objekt för åtgärds grupper i minnet</span><span class="sxs-lookup"><span data-stu-id="dbd7f-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="dbd7f-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbd7f-109">PARAMETERS</span></span>

### <span data-ttu-id="dbd7f-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="dbd7f-110">-ActionGroupId</span></span>
<span data-ttu-id="dbd7f-111">ID/namn på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="dbd7f-111">The Id/name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd7f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd7f-112">-DefaultProfile</span></span>
<span data-ttu-id="dbd7f-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dbd7f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbd7f-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="dbd7f-114">-WebhookProperty</span></span>
<span data-ttu-id="dbd7f-115">Webhook-egenskaper för åtgärds gruppen</span><span class="sxs-lookup"><span data-stu-id="dbd7f-115">The webhook properties of the action group</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd7f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd7f-116">CommonParameters</span></span>
<span data-ttu-id="dbd7f-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd7f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd7f-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbd7f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd7f-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbd7f-119">INPUTS</span></span>

### <span data-ttu-id="dbd7f-120">System. String</span><span class="sxs-lookup"><span data-stu-id="dbd7f-120">System.String</span></span>

### <span data-ttu-id="dbd7f-121">System. Collections. Generic. ordbok ' 2 [[system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e], [system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dbd7f-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="dbd7f-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbd7f-122">OUTPUTS</span></span>

### <span data-ttu-id="dbd7f-123">Microsoft. Azure. Management. Monitoring. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="dbd7f-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="dbd7f-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbd7f-124">NOTES</span></span>

## <span data-ttu-id="dbd7f-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbd7f-125">RELATED LINKS</span></span>

[<span data-ttu-id="dbd7f-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="dbd7f-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="dbd7f-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="dbd7f-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="dbd7f-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="dbd7f-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="dbd7f-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="dbd7f-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="dbd7f-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="dbd7f-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="dbd7f-131">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="dbd7f-131">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

