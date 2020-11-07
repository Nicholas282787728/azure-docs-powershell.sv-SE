---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 53b3bc017458b63433463f6560a5ed1256246208
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918606"
---
# <span data-ttu-id="85e1e-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="85e1e-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="85e1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="85e1e-103">Skapar ett e-postmeddelande med Autoskala.</span><span class="sxs-lookup"><span data-stu-id="85e1e-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="85e1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85e1e-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85e1e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85e1e-105">DESCRIPTION</span></span>
<span data-ttu-id="85e1e-106">Cmdleten **New-AzAutoscaleNotification** skapar ett e-postmeddelande för Autoskala.</span><span class="sxs-lookup"><span data-stu-id="85e1e-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="85e1e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85e1e-107">EXAMPLES</span></span>

### <span data-ttu-id="85e1e-108">Exempel 1: skapa ett e-postmeddelande med Autoskala</span><span class="sxs-lookup"><span data-stu-id="85e1e-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="85e1e-109">Det här kommandot skapar ett Autosacale-e-postmeddelande för två angivna adresser.</span><span class="sxs-lookup"><span data-stu-id="85e1e-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="85e1e-110">Exempel 2: skapa ett e-postmeddelande för en Autoskala för abonnemangs administratören</span><span class="sxs-lookup"><span data-stu-id="85e1e-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="85e1e-111">Det här kommandot skapar ett Autosacale-e-postmeddelande för prenumerations administratören.</span><span class="sxs-lookup"><span data-stu-id="85e1e-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="85e1e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85e1e-112">PARAMETERS</span></span>

### <span data-ttu-id="85e1e-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="85e1e-113">-CustomEmail</span></span>
<span data-ttu-id="85e1e-114">Anger en kommaavgränsad lista med e-postadresser.</span><span class="sxs-lookup"><span data-stu-id="85e1e-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e1e-115">-DefaultProfile</span></span>
<span data-ttu-id="85e1e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="85e1e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85e1e-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="85e1e-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="85e1e-118">Anger att den här åtgärden skickar ett e-postmeddelande till prenumerations administratören.</span><span class="sxs-lookup"><span data-stu-id="85e1e-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e1e-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="85e1e-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="85e1e-120">Indikerar att den här åtgärden skickar ett e-postmeddelande till medarbetarna för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="85e1e-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e1e-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="85e1e-121">-Webhook</span></span>
<span data-ttu-id="85e1e-122">Anger en kommaavgränsad lista med Autoskala-webhookar.</span><span class="sxs-lookup"><span data-stu-id="85e1e-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e1e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e1e-123">CommonParameters</span></span>
<span data-ttu-id="85e1e-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85e1e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e1e-125">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85e1e-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e1e-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85e1e-126">INPUTS</span></span>

### <span data-ttu-id="85e1e-127">Microsoft. Azure. Management. Monitoring. Management. Models. WebhookNotification []</span><span class="sxs-lookup"><span data-stu-id="85e1e-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="85e1e-128">System. string []</span><span class="sxs-lookup"><span data-stu-id="85e1e-128">System.String[]</span></span>

### <span data-ttu-id="85e1e-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="85e1e-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="85e1e-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85e1e-130">OUTPUTS</span></span>

### <span data-ttu-id="85e1e-131">Microsoft. Azure. Management. Monitoring. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="85e1e-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="85e1e-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85e1e-132">NOTES</span></span>

## <span data-ttu-id="85e1e-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85e1e-133">RELATED LINKS</span></span>

[<span data-ttu-id="85e1e-134">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="85e1e-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


