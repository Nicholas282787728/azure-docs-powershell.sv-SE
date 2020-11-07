---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroupreceiver
schema: 2.0.0
ms.openlocfilehash: 0f452818db1af3f3a69db58f82b89e6cfa8ee461
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928866"
---
# <span data-ttu-id="2463a-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="2463a-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="2463a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2463a-102">SYNOPSIS</span></span>
<span data-ttu-id="2463a-103">Skapar en ny mottagare av åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="2463a-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2463a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2463a-104">SYNTAX</span></span>

### <span data-ttu-id="2463a-105">NewEmailReceiver (standard)</span><span class="sxs-lookup"><span data-stu-id="2463a-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2463a-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="2463a-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2463a-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="2463a-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2463a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2463a-108">DESCRIPTION</span></span>
<span data-ttu-id="2463a-109">Cmdleten **New-AzureRmActionGroupReceiver** skapar en ny grupp mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="2463a-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="2463a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2463a-110">EXAMPLES</span></span>

### <span data-ttu-id="2463a-111">Exempel 1: skapa en ny e-postmottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="2463a-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="2463a-112">Det här kommandot skapar en ny e-postmottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="2463a-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="2463a-113">Exempel 2: skapa en ny SMS-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="2463a-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="2463a-114">Det här kommandot skapar en ny SMS-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="2463a-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="2463a-115">Exempel 3: skapa en ny webhook-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="2463a-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="2463a-116">Det här kommandot skapar en ny webhook-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="2463a-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="2463a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2463a-117">PARAMETERS</span></span>

### <span data-ttu-id="2463a-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="2463a-118">-CountryCode</span></span>
<span data-ttu-id="2463a-119">Anger lands koden för SMS-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="2463a-119">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2463a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2463a-120">-DefaultProfile</span></span>
<span data-ttu-id="2463a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2463a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2463a-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="2463a-122">-EmailAddress</span></span>
<span data-ttu-id="2463a-123">Anger adressen för e-postmottagaren.</span><span class="sxs-lookup"><span data-stu-id="2463a-123">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2463a-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="2463a-124">-EmailReceiver</span></span>
<span data-ttu-id="2463a-125">Anger att du vill skapa en e-postmottagare</span><span class="sxs-lookup"><span data-stu-id="2463a-125">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2463a-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="2463a-126">-Name</span></span>
<span data-ttu-id="2463a-127">Anger namnet på mottagaren.</span><span class="sxs-lookup"><span data-stu-id="2463a-127">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="2463a-128">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="2463a-128">-PhoneNumber</span></span>
<span data-ttu-id="2463a-129">Anger telefonnumret för SMS-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="2463a-129">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2463a-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="2463a-130">-ServiceUri</span></span>
<span data-ttu-id="2463a-131">Anger URI för webhook-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="2463a-131">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2463a-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="2463a-132">-SmsReceiver</span></span>
<span data-ttu-id="2463a-133">Anger att SMS-mottagare ska skapas</span><span class="sxs-lookup"><span data-stu-id="2463a-133">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2463a-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="2463a-134">-WebhookReceiver</span></span>
<span data-ttu-id="2463a-135">Anger att du vill skapa en webhook-mottagare</span><span class="sxs-lookup"><span data-stu-id="2463a-135">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2463a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2463a-136">CommonParameters</span></span>
<span data-ttu-id="2463a-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2463a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2463a-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2463a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2463a-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2463a-139">INPUTS</span></span>

### <span data-ttu-id="2463a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2463a-140">System.String</span></span>

### <span data-ttu-id="2463a-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2463a-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2463a-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2463a-142">OUTPUTS</span></span>

### <span data-ttu-id="2463a-143">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="2463a-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="2463a-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2463a-144">NOTES</span></span>

## <span data-ttu-id="2463a-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2463a-145">RELATED LINKS</span></span>

<span data-ttu-id="2463a-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="2463a-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>
