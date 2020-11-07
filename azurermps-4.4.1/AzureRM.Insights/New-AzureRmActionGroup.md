---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: d4afe709d70872c1d7fb59e99f2f98d3dfe19d6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756605"
---
# <span data-ttu-id="bf18e-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="bf18e-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="bf18e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf18e-102">SYNOPSIS</span></span>
<span data-ttu-id="bf18e-103">Skapar ett ActionGroup-referens objekt i minnet.</span><span class="sxs-lookup"><span data-stu-id="bf18e-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf18e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf18e-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf18e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf18e-105">DESCRIPTION</span></span>
<span data-ttu-id="bf18e-106">Cmdleten **New-AzureRmActionGroup** skapar ett referens objekt i minnet.</span><span class="sxs-lookup"><span data-stu-id="bf18e-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="bf18e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf18e-107">EXAMPLES</span></span>

### <span data-ttu-id="bf18e-108">Exempel 1: skapa ett referens objekt för åtgärds grupper i minnet</span><span class="sxs-lookup"><span data-stu-id="bf18e-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="bf18e-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf18e-109">PARAMETERS</span></span>

### <span data-ttu-id="bf18e-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="bf18e-110">-ActionGroupId</span></span>
<span data-ttu-id="bf18e-111">ID/namn på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="bf18e-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="bf18e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf18e-112">-DefaultProfile</span></span>
<span data-ttu-id="bf18e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bf18e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf18e-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="bf18e-114">-WebhookProperty</span></span>
<span data-ttu-id="bf18e-115">Webhook-egenskaper för åtgärds gruppen</span><span class="sxs-lookup"><span data-stu-id="bf18e-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="bf18e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf18e-116">CommonParameters</span></span>
<span data-ttu-id="bf18e-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf18e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf18e-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf18e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf18e-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf18e-119">INPUTS</span></span>

## <span data-ttu-id="bf18e-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf18e-120">OUTPUTS</span></span>

### <span data-ttu-id="bf18e-121">Microsoft. Azure. Management. Monitoring. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="bf18e-121">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="bf18e-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf18e-122">NOTES</span></span>

## <span data-ttu-id="bf18e-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf18e-123">RELATED LINKS</span></span>

[<span data-ttu-id="bf18e-124">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bf18e-124">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="bf18e-125">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bf18e-125">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="bf18e-126">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bf18e-126">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="bf18e-127">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bf18e-127">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="bf18e-128">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bf18e-128">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="bf18e-129">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="bf18e-129">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

