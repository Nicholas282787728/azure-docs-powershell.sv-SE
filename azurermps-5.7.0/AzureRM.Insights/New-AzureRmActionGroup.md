---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: 9428ea3c297bcdab01ee6464d38b5c20910b69d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755874"
---
# <span data-ttu-id="3479c-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="3479c-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="3479c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3479c-102">SYNOPSIS</span></span>
<span data-ttu-id="3479c-103">Skapar ett ActionGroup-referens objekt i minnet.</span><span class="sxs-lookup"><span data-stu-id="3479c-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3479c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3479c-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3479c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3479c-105">DESCRIPTION</span></span>
<span data-ttu-id="3479c-106">Cmdleten **New-AzureRmActionGroup** skapar ett referens objekt i minnet.</span><span class="sxs-lookup"><span data-stu-id="3479c-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="3479c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3479c-107">EXAMPLES</span></span>

### <span data-ttu-id="3479c-108">Exempel 1: skapa ett referens objekt för åtgärds grupper i minnet</span><span class="sxs-lookup"><span data-stu-id="3479c-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="3479c-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3479c-109">PARAMETERS</span></span>

### <span data-ttu-id="3479c-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="3479c-110">-ActionGroupId</span></span>
<span data-ttu-id="3479c-111">ID/namn på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="3479c-111">The Id/name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3479c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3479c-112">-DefaultProfile</span></span>
<span data-ttu-id="3479c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3479c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3479c-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="3479c-114">-WebhookProperty</span></span>
<span data-ttu-id="3479c-115">Webhook-egenskaper för åtgärds gruppen</span><span class="sxs-lookup"><span data-stu-id="3479c-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="3479c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3479c-116">CommonParameters</span></span>
<span data-ttu-id="3479c-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3479c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3479c-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3479c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3479c-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3479c-119">INPUTS</span></span>

### <span data-ttu-id="3479c-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="3479c-120">None</span></span>
<span data-ttu-id="3479c-121">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3479c-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3479c-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3479c-122">OUTPUTS</span></span>

### <span data-ttu-id="3479c-123">Microsoft. Azure. Management. Monitoring. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="3479c-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="3479c-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3479c-124">NOTES</span></span>

## <span data-ttu-id="3479c-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3479c-125">RELATED LINKS</span></span>

[<span data-ttu-id="3479c-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3479c-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3479c-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3479c-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3479c-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3479c-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3479c-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3479c-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3479c-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3479c-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3479c-131">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="3479c-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
