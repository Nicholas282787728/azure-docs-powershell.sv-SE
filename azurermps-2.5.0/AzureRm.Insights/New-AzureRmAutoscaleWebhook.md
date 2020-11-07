---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
ms.openlocfilehash: fe6170842bcacf4d7fb0c8e442dc988c03c67e35
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929906"
---
# <span data-ttu-id="16f1b-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="16f1b-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="16f1b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="16f1b-103">Skapar en Autoskala-webhook.</span><span class="sxs-lookup"><span data-stu-id="16f1b-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16f1b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16f1b-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16f1b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16f1b-105">DESCRIPTION</span></span>
<span data-ttu-id="16f1b-106">Cmdleten **New-AzureRmAutoscaleWebhook** skapar en Autoskala-webhook.</span><span class="sxs-lookup"><span data-stu-id="16f1b-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="16f1b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16f1b-107">EXAMPLES</span></span>

## <span data-ttu-id="16f1b-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16f1b-108">PARAMETERS</span></span>

### <span data-ttu-id="16f1b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f1b-109">-DefaultProfile</span></span>
<span data-ttu-id="16f1b-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="16f1b-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16f1b-111">-Egenskap</span><span class="sxs-lookup"><span data-stu-id="16f1b-111">-Property</span></span>
<span data-ttu-id="16f1b-112">Anger listan över egenskaper i formatet @ (property1 = ' värde1 ',....).</span><span class="sxs-lookup"><span data-stu-id="16f1b-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f1b-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="16f1b-113">-ServiceUri</span></span>
<span data-ttu-id="16f1b-114">Anger tjänste-URI.</span><span class="sxs-lookup"><span data-stu-id="16f1b-114">Specifies the service URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f1b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f1b-115">CommonParameters</span></span>
<span data-ttu-id="16f1b-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16f1b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f1b-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16f1b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f1b-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16f1b-118">INPUTS</span></span>

### <span data-ttu-id="16f1b-119">System. String</span><span class="sxs-lookup"><span data-stu-id="16f1b-119">System.String</span></span>

### <span data-ttu-id="16f1b-120">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="16f1b-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="16f1b-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16f1b-121">OUTPUTS</span></span>

### <span data-ttu-id="16f1b-122">Microsoft. Azure. Management. Monitoring. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="16f1b-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="16f1b-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16f1b-123">NOTES</span></span>

## <span data-ttu-id="16f1b-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16f1b-124">RELATED LINKS</span></span>

[<span data-ttu-id="16f1b-125">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="16f1b-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


