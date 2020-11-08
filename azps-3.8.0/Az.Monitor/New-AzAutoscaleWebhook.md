---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: f9e9d9bea69944fdd6eae6c81a4472dee1816e4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088547"
---
# <span data-ttu-id="922bf-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="922bf-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="922bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="922bf-102">SYNOPSIS</span></span>
<span data-ttu-id="922bf-103">Skapar en Autoskala-webhook.</span><span class="sxs-lookup"><span data-stu-id="922bf-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="922bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="922bf-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="922bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="922bf-105">DESCRIPTION</span></span>
<span data-ttu-id="922bf-106">Cmdleten **New-AzAutoscaleWebhook** skapar en Autoskala-webhook.</span><span class="sxs-lookup"><span data-stu-id="922bf-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="922bf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="922bf-107">EXAMPLES</span></span>

## <span data-ttu-id="922bf-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="922bf-108">PARAMETERS</span></span>

### <span data-ttu-id="922bf-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922bf-109">-DefaultProfile</span></span>
<span data-ttu-id="922bf-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="922bf-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="922bf-111">-Egenskap</span><span class="sxs-lookup"><span data-stu-id="922bf-111">-Property</span></span>
<span data-ttu-id="922bf-112">Anger listan över egenskaper i formatet @ (property1 = ' värde1 ',....).</span><span class="sxs-lookup"><span data-stu-id="922bf-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="922bf-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="922bf-113">-ServiceUri</span></span>
<span data-ttu-id="922bf-114">Anger tjänste-URI.</span><span class="sxs-lookup"><span data-stu-id="922bf-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="922bf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922bf-115">CommonParameters</span></span>
<span data-ttu-id="922bf-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="922bf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922bf-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="922bf-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922bf-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="922bf-118">INPUTS</span></span>

### <span data-ttu-id="922bf-119">System. String</span><span class="sxs-lookup"><span data-stu-id="922bf-119">System.String</span></span>

### <span data-ttu-id="922bf-120">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="922bf-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="922bf-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="922bf-121">OUTPUTS</span></span>

### <span data-ttu-id="922bf-122">Microsoft. Azure. Management. Monitoring. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="922bf-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="922bf-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="922bf-123">NOTES</span></span>

## <span data-ttu-id="922bf-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="922bf-124">RELATED LINKS</span></span>

[<span data-ttu-id="922bf-125">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="922bf-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


