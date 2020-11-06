---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: f6791d2cc962f0bb0db038ad8c5391425c09bfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584735"
---
# <span data-ttu-id="ef57b-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="ef57b-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="ef57b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef57b-102">SYNOPSIS</span></span>
<span data-ttu-id="ef57b-103">Skapar ett e-postmeddelande med Autoskala.</span><span class="sxs-lookup"><span data-stu-id="ef57b-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef57b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef57b-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhooks] <WebhookNotification[]>] [[-CustomEmails] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef57b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef57b-105">DESCRIPTION</span></span>
<span data-ttu-id="ef57b-106">Cmdleten **New-AzureRmAutoscaleNotification** skapar ett e-postmeddelande för Autoskala.</span><span class="sxs-lookup"><span data-stu-id="ef57b-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="ef57b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef57b-107">EXAMPLES</span></span>

### <span data-ttu-id="ef57b-108">Exempel 1: skapa ett e-postmeddelande med Autoskala</span><span class="sxs-lookup"><span data-stu-id="ef57b-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="ef57b-109">Det här kommandot skapar ett Autosacale-e-postmeddelande för två angivna adresser.</span><span class="sxs-lookup"><span data-stu-id="ef57b-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="ef57b-110">Exempel 2: skapa ett e-postmeddelande för en Autoskala för abonnemangs administratören</span><span class="sxs-lookup"><span data-stu-id="ef57b-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="ef57b-111">Det här kommandot skapar ett Autosacale-e-postmeddelande för prenumerations administratören.</span><span class="sxs-lookup"><span data-stu-id="ef57b-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="ef57b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef57b-112">PARAMETERS</span></span>

### <span data-ttu-id="ef57b-113">-CustomEmails</span><span class="sxs-lookup"><span data-stu-id="ef57b-113">-CustomEmails</span></span>
<span data-ttu-id="ef57b-114">Anger en kommaavgränsad lista med e-postadresser.</span><span class="sxs-lookup"><span data-stu-id="ef57b-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="ef57b-115">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="ef57b-115">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="ef57b-116">Anger att den här åtgärden skickar ett e-postmeddelande till prenumerations administratören.</span><span class="sxs-lookup"><span data-stu-id="ef57b-116">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="ef57b-117">-SendEmailToSubscriptionCoAdministrators</span><span class="sxs-lookup"><span data-stu-id="ef57b-117">-SendEmailToSubscriptionCoAdministrators</span></span>
<span data-ttu-id="ef57b-118">Indikerar att den här åtgärden skickar ett e-postmeddelande till medarbetarna för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ef57b-118">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="ef57b-119">– Webhookar</span><span class="sxs-lookup"><span data-stu-id="ef57b-119">-Webhooks</span></span>
<span data-ttu-id="ef57b-120">Anger en kommaavgränsad lista med Autoskala-webhookar.</span><span class="sxs-lookup"><span data-stu-id="ef57b-120">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="ef57b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef57b-121">-DefaultProfile</span></span>
<span data-ttu-id="ef57b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef57b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef57b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef57b-123">CommonParameters</span></span>
<span data-ttu-id="ef57b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef57b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef57b-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef57b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef57b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef57b-126">INPUTS</span></span>

## <span data-ttu-id="ef57b-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef57b-127">OUTPUTS</span></span>

### <span data-ttu-id="ef57b-128">Microsoft. Azure. Management. Monitoring. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="ef57b-128">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="ef57b-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef57b-129">NOTES</span></span>

## <span data-ttu-id="ef57b-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef57b-130">RELATED LINKS</span></span>

[<span data-ttu-id="ef57b-131">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="ef57b-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


