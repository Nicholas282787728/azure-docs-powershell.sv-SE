---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 8b94ad5728e7852bb3cd834e7479a29cc11c1698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581172"
---
# <span data-ttu-id="4dbd3-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="4dbd3-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="4dbd3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4dbd3-102">SYNOPSIS</span></span>
<span data-ttu-id="4dbd3-103">Skapar en Autoskala-webhook.</span><span class="sxs-lookup"><span data-stu-id="4dbd3-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dbd3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4dbd3-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dbd3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4dbd3-105">DESCRIPTION</span></span>
<span data-ttu-id="4dbd3-106">Cmdleten **New-AzureRmAutoscaleWebhook** skapar en Autoskala-webhook.</span><span class="sxs-lookup"><span data-stu-id="4dbd3-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="4dbd3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4dbd3-107">EXAMPLES</span></span>

## <span data-ttu-id="4dbd3-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4dbd3-108">PARAMETERS</span></span>

### <span data-ttu-id="4dbd3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dbd3-109">-DefaultProfile</span></span>
<span data-ttu-id="4dbd3-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4dbd3-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4dbd3-111">-Egenskap</span><span class="sxs-lookup"><span data-stu-id="4dbd3-111">-Property</span></span>
<span data-ttu-id="4dbd3-112">Anger listan över egenskaper i formatet @ (property1 = ' värde1 ',....).</span><span class="sxs-lookup"><span data-stu-id="4dbd3-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Properties

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dbd3-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="4dbd3-113">-ServiceUri</span></span>
<span data-ttu-id="4dbd3-114">Anger tjänste-URI.</span><span class="sxs-lookup"><span data-stu-id="4dbd3-114">Specifies the service URI.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dbd3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dbd3-115">CommonParameters</span></span>
<span data-ttu-id="4dbd3-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dbd3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dbd3-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dbd3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dbd3-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4dbd3-118">INPUTS</span></span>

### <span data-ttu-id="4dbd3-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="4dbd3-119">None</span></span>
<span data-ttu-id="4dbd3-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4dbd3-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4dbd3-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4dbd3-121">OUTPUTS</span></span>

### <span data-ttu-id="4dbd3-122">Microsoft. Azure. Management. Monitoring. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="4dbd3-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="4dbd3-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4dbd3-123">NOTES</span></span>

## <span data-ttu-id="4dbd3-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4dbd3-124">RELATED LINKS</span></span>

[<span data-ttu-id="4dbd3-125">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="4dbd3-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


