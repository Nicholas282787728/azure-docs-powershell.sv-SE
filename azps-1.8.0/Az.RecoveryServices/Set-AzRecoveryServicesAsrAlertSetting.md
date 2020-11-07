---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: ca17774085e76adad57698c2b0b5689ec1c276e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747345"
---
# <span data-ttu-id="11ac3-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="11ac3-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="11ac3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11ac3-102">SYNOPSIS</span></span>
<span data-ttu-id="11ac3-103">Konfigurera aviserings inställningar för Azure Site Recovery (e-postmeddelande) för valvet.</span><span class="sxs-lookup"><span data-stu-id="11ac3-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="11ac3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11ac3-104">SYNTAX</span></span>

### <span data-ttu-id="11ac3-105">Ange (standard)</span><span class="sxs-lookup"><span data-stu-id="11ac3-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11ac3-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="11ac3-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11ac3-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="11ac3-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11ac3-108">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="11ac3-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11ac3-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11ac3-109">DESCRIPTION</span></span>
<span data-ttu-id="11ac3-110">Cmdleten **set-AzRecoveryServicesAsrNotificationSetting** konfigurerar meddelande inställningar för Azure Site Recovery (e-postmeddelande) för valvet.</span><span class="sxs-lookup"><span data-stu-id="11ac3-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="11ac3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11ac3-111">EXAMPLES</span></span>

### <span data-ttu-id="11ac3-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="11ac3-112">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="11ac3-113">Inaktivera meddelande.</span><span class="sxs-lookup"><span data-stu-id="11ac3-113">Disable notification.</span></span>

### <span data-ttu-id="11ac3-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="11ac3-114">Example 2</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="11ac3-115">Ange meddelande för egna e-postadresser och för abonnemangs ägaren.</span><span class="sxs-lookup"><span data-stu-id="11ac3-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="11ac3-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11ac3-116">PARAMETERS</span></span>

### <span data-ttu-id="11ac3-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="11ac3-117">-CustomEmailAddress</span></span>
<span data-ttu-id="11ac3-118">Avisering/avisering skickades till e-post.</span><span class="sxs-lookup"><span data-stu-id="11ac3-118">Alert / Notification sent to emails.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ac3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ac3-119">-DefaultProfile</span></span>
<span data-ttu-id="11ac3-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11ac3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11ac3-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="11ac3-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="11ac3-122">Byt parameter anger att Prenumerationens ägare ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="11ac3-122">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ac3-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="11ac3-123">-DisableNotification</span></span>
<span data-ttu-id="11ac3-124">Flagga för att inaktivera all avisering.</span><span class="sxs-lookup"><span data-stu-id="11ac3-124">Flag to disable all notification.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ac3-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="11ac3-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="11ac3-126">Växla parameter anger aktivera Prenumerationens ägare.</span><span class="sxs-lookup"><span data-stu-id="11ac3-126">Switch paramter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ac3-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="11ac3-127">-LocaleID</span></span>
<span data-ttu-id="11ac3-128">E-postspråk för Alert/notifcation till användare (kultur koder som stöds från Microsoft).</span><span class="sxs-lookup"><span data-stu-id="11ac3-128">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: System.String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ac3-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="11ac3-129">-Confirm</span></span>
<span data-ttu-id="11ac3-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="11ac3-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ac3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11ac3-131">-WhatIf</span></span>
<span data-ttu-id="11ac3-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="11ac3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11ac3-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="11ac3-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ac3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ac3-134">CommonParameters</span></span>
<span data-ttu-id="11ac3-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11ac3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ac3-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11ac3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ac3-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11ac3-137">INPUTS</span></span>

### <span data-ttu-id="11ac3-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="11ac3-138">None</span></span>

## <span data-ttu-id="11ac3-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11ac3-139">OUTPUTS</span></span>

### <span data-ttu-id="11ac3-140">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="11ac3-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="11ac3-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11ac3-141">NOTES</span></span>

## <span data-ttu-id="11ac3-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11ac3-142">RELATED LINKS</span></span>