---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: b2f9738518f446b9cf5bfbefe0c7025bb3351628
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928870"
---
# <span data-ttu-id="867ef-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="867ef-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="867ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="867ef-102">SYNOPSIS</span></span>
<span data-ttu-id="867ef-103">Skapar ett ActionGroup-referens objekt i minnet.</span><span class="sxs-lookup"><span data-stu-id="867ef-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="867ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="867ef-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="867ef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="867ef-105">DESCRIPTION</span></span>
<span data-ttu-id="867ef-106">Cmdleten **New-AzureRmActionGroup** skapar ett referens objekt i minnet.</span><span class="sxs-lookup"><span data-stu-id="867ef-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="867ef-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="867ef-107">EXAMPLES</span></span>

### <span data-ttu-id="867ef-108">Exempel 1: skapa ett referens objekt för åtgärds grupper i minnet</span><span class="sxs-lookup"><span data-stu-id="867ef-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="867ef-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="867ef-109">PARAMETERS</span></span>

### <span data-ttu-id="867ef-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="867ef-110">-ActionGroupId</span></span>
<span data-ttu-id="867ef-111">ID/namn på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="867ef-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="867ef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="867ef-112">-DefaultProfile</span></span>
<span data-ttu-id="867ef-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="867ef-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="867ef-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="867ef-114">-WebhookProperty</span></span>
<span data-ttu-id="867ef-115">Webhook-egenskaper för åtgärds gruppen</span><span class="sxs-lookup"><span data-stu-id="867ef-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="867ef-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="867ef-116">CommonParameters</span></span>
<span data-ttu-id="867ef-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="867ef-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="867ef-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="867ef-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="867ef-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="867ef-119">INPUTS</span></span>

### <span data-ttu-id="867ef-120">System. String</span><span class="sxs-lookup"><span data-stu-id="867ef-120">System.String</span></span>

### <span data-ttu-id="867ef-121">System. Collections. Generic. ordbok ' 2 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089], [system. String, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="867ef-121">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="867ef-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="867ef-122">OUTPUTS</span></span>

### <span data-ttu-id="867ef-123">Microsoft. Azure. Management. Monitoring. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="867ef-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="867ef-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="867ef-124">NOTES</span></span>

## <span data-ttu-id="867ef-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="867ef-125">RELATED LINKS</span></span>

[<span data-ttu-id="867ef-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="867ef-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="867ef-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="867ef-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="867ef-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="867ef-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="867ef-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="867ef-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="867ef-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="867ef-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="867ef-131">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="867ef-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

