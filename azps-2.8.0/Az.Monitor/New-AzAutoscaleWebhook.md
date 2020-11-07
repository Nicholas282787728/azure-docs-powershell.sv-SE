---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: 4f2e7ea3293c9ca40271b9092673f33108a9f1be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918599"
---
# <span data-ttu-id="e5173-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="e5173-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="e5173-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5173-102">SYNOPSIS</span></span>
<span data-ttu-id="e5173-103">Skapar en Autoskala-webhook.</span><span class="sxs-lookup"><span data-stu-id="e5173-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="e5173-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5173-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5173-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5173-105">DESCRIPTION</span></span>
<span data-ttu-id="e5173-106">Cmdleten **New-AzAutoscaleWebhook** skapar en Autoskala-webhook.</span><span class="sxs-lookup"><span data-stu-id="e5173-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="e5173-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5173-107">EXAMPLES</span></span>

## <span data-ttu-id="e5173-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5173-108">PARAMETERS</span></span>

### <span data-ttu-id="e5173-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5173-109">-DefaultProfile</span></span>
<span data-ttu-id="e5173-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e5173-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5173-111">-Egenskap</span><span class="sxs-lookup"><span data-stu-id="e5173-111">-Property</span></span>
<span data-ttu-id="e5173-112">Anger listan över egenskaper i formatet @ (property1 = ' värde1 ',....).</span><span class="sxs-lookup"><span data-stu-id="e5173-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="e5173-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="e5173-113">-ServiceUri</span></span>
<span data-ttu-id="e5173-114">Anger tjänste-URI.</span><span class="sxs-lookup"><span data-stu-id="e5173-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="e5173-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5173-115">CommonParameters</span></span>
<span data-ttu-id="e5173-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5173-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5173-117">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5173-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5173-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5173-118">INPUTS</span></span>

### <span data-ttu-id="e5173-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e5173-119">System.String</span></span>

### <span data-ttu-id="e5173-120">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="e5173-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e5173-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5173-121">OUTPUTS</span></span>

### <span data-ttu-id="e5173-122">Microsoft. Azure. Management. Monitoring. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="e5173-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="e5173-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5173-123">NOTES</span></span>

## <span data-ttu-id="e5173-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5173-124">RELATED LINKS</span></span>

[<span data-ttu-id="e5173-125">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e5173-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


