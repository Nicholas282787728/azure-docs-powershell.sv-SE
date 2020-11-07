---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 35f540d26464b7cdc4b08916f1397b71ee7cca18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915645"
---
# <span data-ttu-id="98546-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="98546-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="98546-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98546-102">SYNOPSIS</span></span>
<span data-ttu-id="98546-103">Skapar en ny mottagare av åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="98546-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="98546-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98546-104">SYNTAX</span></span>

### <span data-ttu-id="98546-105">NewEmailReceiver (standard)</span><span class="sxs-lookup"><span data-stu-id="98546-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98546-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="98546-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98546-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="98546-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98546-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98546-108">DESCRIPTION</span></span>
<span data-ttu-id="98546-109">Cmdleten **New-AzActionGroupReceiver** skapar en ny grupp mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="98546-109">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="98546-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98546-110">EXAMPLES</span></span>

### <span data-ttu-id="98546-111">Exempel 1: skapa en ny e-postmottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="98546-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="98546-112">Det här kommandot skapar en ny e-postmottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="98546-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="98546-113">Exempel 2: skapa en ny SMS-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="98546-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="98546-114">Det här kommandot skapar en ny SMS-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="98546-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="98546-115">Exempel 3: skapa en ny webhook-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="98546-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="98546-116">Det här kommandot skapar en ny webhook-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="98546-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="98546-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98546-117">PARAMETERS</span></span>

### <span data-ttu-id="98546-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="98546-118">-CountryCode</span></span>
<span data-ttu-id="98546-119">Anger lands koden för SMS-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="98546-119">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="98546-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98546-120">-DefaultProfile</span></span>
<span data-ttu-id="98546-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="98546-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98546-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="98546-122">-EmailAddress</span></span>
<span data-ttu-id="98546-123">Anger adressen för e-postmottagaren.</span><span class="sxs-lookup"><span data-stu-id="98546-123">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="98546-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="98546-124">-EmailReceiver</span></span>
<span data-ttu-id="98546-125">Anger att du vill skapa en e-postmottagare</span><span class="sxs-lookup"><span data-stu-id="98546-125">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="98546-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="98546-126">-Name</span></span>
<span data-ttu-id="98546-127">Anger namnet på mottagaren.</span><span class="sxs-lookup"><span data-stu-id="98546-127">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="98546-128">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="98546-128">-PhoneNumber</span></span>
<span data-ttu-id="98546-129">Anger telefonnumret för SMS-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="98546-129">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="98546-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="98546-130">-ServiceUri</span></span>
<span data-ttu-id="98546-131">Anger URI för webhook-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="98546-131">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="98546-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="98546-132">-SmsReceiver</span></span>
<span data-ttu-id="98546-133">Anger att SMS-mottagare ska skapas</span><span class="sxs-lookup"><span data-stu-id="98546-133">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="98546-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="98546-134">-WebhookReceiver</span></span>
<span data-ttu-id="98546-135">Anger att du vill skapa en webhook-mottagare</span><span class="sxs-lookup"><span data-stu-id="98546-135">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="98546-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98546-136">CommonParameters</span></span>
<span data-ttu-id="98546-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98546-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98546-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98546-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98546-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98546-139">INPUTS</span></span>

### <span data-ttu-id="98546-140">System. String</span><span class="sxs-lookup"><span data-stu-id="98546-140">System.String</span></span>

### <span data-ttu-id="98546-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="98546-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="98546-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98546-142">OUTPUTS</span></span>

### <span data-ttu-id="98546-143">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="98546-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="98546-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98546-144">NOTES</span></span>

## <span data-ttu-id="98546-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98546-145">RELATED LINKS</span></span>

<span data-ttu-id="98546-146">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="98546-146">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
