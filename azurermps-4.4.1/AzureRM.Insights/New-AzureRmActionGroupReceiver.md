---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
ms.openlocfilehash: cd08e0106fe78ddae04ac4543210b310fe3aa579
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756603"
---
# <span data-ttu-id="5ba6d-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="5ba6d-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="5ba6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ba6d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba6d-103">Skapar en ny mottagare av åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ba6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ba6d-104">SYNTAX</span></span>

### <span data-ttu-id="5ba6d-105">NewEmailReceiver (standard)</span><span class="sxs-lookup"><span data-stu-id="5ba6d-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ba6d-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="5ba6d-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ba6d-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="5ba6d-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ba6d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ba6d-108">DESCRIPTION</span></span>
<span data-ttu-id="5ba6d-109">Cmdleten **New-AzureRmActionGroupReceiver** skapar en ny grupp mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="5ba6d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ba6d-110">EXAMPLES</span></span>

### <span data-ttu-id="5ba6d-111">Exempel 1: skapa en ny e-postmottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="5ba6d-112">Det här kommandot skapar en ny e-postmottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="5ba6d-113">Exempel 2: skapa en ny SMS-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="5ba6d-114">Det här kommandot skapar en ny SMS-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="5ba6d-115">Exempel 3: skapa en ny webhook-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="5ba6d-116">Det här kommandot skapar en ny webhook-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="5ba6d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ba6d-117">PARAMETERS</span></span>

### <span data-ttu-id="5ba6d-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ba6d-118">-Name</span></span>
<span data-ttu-id="5ba6d-119">Anger namnet på mottagaren.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-119">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="5ba6d-120">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="5ba6d-120">-EmailAddress</span></span>
<span data-ttu-id="5ba6d-121">Anger adressen för e-postmottagaren.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-121">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="5ba6d-122">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="5ba6d-122">-CountryCode</span></span>
<span data-ttu-id="5ba6d-123">Anger lands koden för SMS-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-123">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="5ba6d-124">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="5ba6d-124">-PhoneNumber</span></span>
<span data-ttu-id="5ba6d-125">Anger telefonnumret för SMS-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-125">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="5ba6d-126">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="5ba6d-126">-ServiceUri</span></span>
<span data-ttu-id="5ba6d-127">Anger URI för webhook-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-127">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="5ba6d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba6d-128">-DefaultProfile</span></span>
<span data-ttu-id="5ba6d-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ba6d-130">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="5ba6d-130">-EmailReceiver</span></span>
<span data-ttu-id="5ba6d-131">Anger att du vill skapa en e-postmottagare</span><span class="sxs-lookup"><span data-stu-id="5ba6d-131">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="5ba6d-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="5ba6d-132">-SmsReceiver</span></span>
<span data-ttu-id="5ba6d-133">Anger att SMS-mottagare ska skapas</span><span class="sxs-lookup"><span data-stu-id="5ba6d-133">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="5ba6d-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="5ba6d-134">-WebhookReceiver</span></span>
<span data-ttu-id="5ba6d-135">Anger att du vill skapa en webhook-mottagare</span><span class="sxs-lookup"><span data-stu-id="5ba6d-135">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="5ba6d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba6d-136">CommonParameters</span></span>
<span data-ttu-id="5ba6d-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba6d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba6d-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ba6d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba6d-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ba6d-139">INPUTS</span></span>

## <span data-ttu-id="5ba6d-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ba6d-140">OUTPUTS</span></span>

### <span data-ttu-id="5ba6d-141">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="5ba6d-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="5ba6d-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ba6d-142">NOTES</span></span>

## <span data-ttu-id="5ba6d-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ba6d-143">RELATED LINKS</span></span>

<span data-ttu-id="5ba6d-144">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="5ba6d-144">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>
