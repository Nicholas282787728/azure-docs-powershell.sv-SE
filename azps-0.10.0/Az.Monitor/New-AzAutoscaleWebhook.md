---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: a719d841df2d3f211fdb2592ed2a96b507c51e10
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922557"
---
# <span data-ttu-id="bb26f-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="bb26f-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="bb26f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb26f-102">SYNOPSIS</span></span>
<span data-ttu-id="bb26f-103">Skapar en Autoskala-webhook.</span><span class="sxs-lookup"><span data-stu-id="bb26f-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="bb26f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb26f-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb26f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb26f-105">DESCRIPTION</span></span>
<span data-ttu-id="bb26f-106">Cmdleten **New-AzAutoscaleWebhook** skapar en Autoskala-webhook.</span><span class="sxs-lookup"><span data-stu-id="bb26f-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="bb26f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb26f-107">EXAMPLES</span></span>

## <span data-ttu-id="bb26f-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb26f-108">PARAMETERS</span></span>

### <span data-ttu-id="bb26f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb26f-109">-DefaultProfile</span></span>
<span data-ttu-id="bb26f-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bb26f-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb26f-111">-Egenskap</span><span class="sxs-lookup"><span data-stu-id="bb26f-111">-Property</span></span>
<span data-ttu-id="bb26f-112">Anger listan över egenskaper i formatet @ (property1 = ' värde1 ',....).</span><span class="sxs-lookup"><span data-stu-id="bb26f-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="bb26f-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="bb26f-113">-ServiceUri</span></span>
<span data-ttu-id="bb26f-114">Anger tjänste-URI.</span><span class="sxs-lookup"><span data-stu-id="bb26f-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="bb26f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb26f-115">CommonParameters</span></span>
<span data-ttu-id="bb26f-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb26f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb26f-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb26f-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb26f-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb26f-118">INPUTS</span></span>

### <span data-ttu-id="bb26f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="bb26f-119">System.String</span></span>

### <span data-ttu-id="bb26f-120">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="bb26f-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bb26f-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb26f-121">OUTPUTS</span></span>

### <span data-ttu-id="bb26f-122">Microsoft. Azure. Management. Monitoring. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="bb26f-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="bb26f-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb26f-123">NOTES</span></span>

## <span data-ttu-id="bb26f-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb26f-124">RELATED LINKS</span></span>

[<span data-ttu-id="bb26f-125">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="bb26f-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


