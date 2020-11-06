---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: ee95455b5081105ec4e28a4811e46ca92bfbc240
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577209"
---
# <span data-ttu-id="f3e8a-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="f3e8a-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="f3e8a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e8a-103">Skapar ett e-postmeddelande med Autoskala.</span><span class="sxs-lookup"><span data-stu-id="f3e8a-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3e8a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3e8a-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator] 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3e8a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3e8a-105">DESCRIPTION</span></span>
<span data-ttu-id="f3e8a-106">Cmdleten **New-AzureRmAutoscaleNotification** skapar ett e-postmeddelande för Autoskala.</span><span class="sxs-lookup"><span data-stu-id="f3e8a-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="f3e8a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3e8a-107">EXAMPLES</span></span>

### <span data-ttu-id="f3e8a-108">Exempel 1: skapa ett e-postmeddelande med Autoskala</span><span class="sxs-lookup"><span data-stu-id="f3e8a-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="f3e8a-109">Det här kommandot skapar ett Autosacale-e-postmeddelande för två angivna adresser.</span><span class="sxs-lookup"><span data-stu-id="f3e8a-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="f3e8a-110">Exempel 2: skapa ett e-postmeddelande för en Autoskala för abonnemangs administratören</span><span class="sxs-lookup"><span data-stu-id="f3e8a-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="f3e8a-111">Det här kommandot skapar ett Autosacale-e-postmeddelande för prenumerations administratören.</span><span class="sxs-lookup"><span data-stu-id="f3e8a-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="f3e8a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3e8a-112">PARAMETERS</span></span>

### <span data-ttu-id="f3e8a-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="f3e8a-113">-CustomEmail</span></span>
<span data-ttu-id="f3e8a-114">Anger en kommaavgränsad lista med e-postadresser.</span><span class="sxs-lookup"><span data-stu-id="f3e8a-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CustomEmails

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e8a-115">-DefaultProfile</span></span>
<span data-ttu-id="f3e8a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f3e8a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3e8a-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="f3e8a-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="f3e8a-118">Anger att den här åtgärden skickar ett e-postmeddelande till prenumerations administratören.</span><span class="sxs-lookup"><span data-stu-id="f3e8a-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e8a-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="f3e8a-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="f3e8a-120">Indikerar att den här åtgärden skickar ett e-postmeddelande till medarbetarna för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f3e8a-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: SendEmailToSubscriptionCoAdministrators

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e8a-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="f3e8a-121">-Webhook</span></span>
<span data-ttu-id="f3e8a-122">Anger en kommaavgränsad lista med Autoskala-webhookar.</span><span class="sxs-lookup"><span data-stu-id="f3e8a-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: WebhookNotification[]
Parameter Sets: (All)
Aliases: Webhooks

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3e8a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e8a-123">CommonParameters</span></span>
<span data-ttu-id="f3e8a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3e8a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e8a-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3e8a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e8a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3e8a-126">INPUTS</span></span>

### <span data-ttu-id="f3e8a-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="f3e8a-127">None</span></span>
<span data-ttu-id="f3e8a-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f3e8a-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3e8a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3e8a-129">OUTPUTS</span></span>

### <span data-ttu-id="f3e8a-130">Microsoft. Azure. Management. Monitoring. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="f3e8a-130">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="f3e8a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3e8a-131">NOTES</span></span>

## <span data-ttu-id="f3e8a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3e8a-132">RELATED LINKS</span></span>

[<span data-ttu-id="f3e8a-133">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="f3e8a-133">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


