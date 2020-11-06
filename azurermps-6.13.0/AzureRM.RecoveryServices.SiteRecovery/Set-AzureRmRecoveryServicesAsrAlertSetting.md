---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 70816649b33cd91c7d378b3588b443e4dd5b8fe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576811"
---
# <span data-ttu-id="86fdc-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="86fdc-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="86fdc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="86fdc-103">Konfigurera aviserings inställningar för Azure Site Recovery (e-postmeddelande) för valvet.</span><span class="sxs-lookup"><span data-stu-id="86fdc-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86fdc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86fdc-104">SYNTAX</span></span>

### <span data-ttu-id="86fdc-105">Ange (standard)</span><span class="sxs-lookup"><span data-stu-id="86fdc-105">Set (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86fdc-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="86fdc-106">EmailToSubscriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86fdc-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="86fdc-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86fdc-108">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="86fdc-108">Disable</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86fdc-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86fdc-109">DESCRIPTION</span></span>
<span data-ttu-id="86fdc-110">Cmdleten **set-AzureRmRecoveryServicesAsrNotificationSetting** konfigurerar meddelande inställningar för Azure Site Recovery (e-postmeddelande) för valvet.</span><span class="sxs-lookup"><span data-stu-id="86fdc-110">The **Set-AzureRmRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="86fdc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86fdc-111">EXAMPLES</span></span>

### <span data-ttu-id="86fdc-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="86fdc-112">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="86fdc-113">Inaktivera meddelande.</span><span class="sxs-lookup"><span data-stu-id="86fdc-113">Disable notification.</span></span>

### <span data-ttu-id="86fdc-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="86fdc-114">Example 2</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="86fdc-115">Ange meddelande för egna e-postadresser och för abonnemangs ägaren.</span><span class="sxs-lookup"><span data-stu-id="86fdc-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="86fdc-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86fdc-116">PARAMETERS</span></span>

### <span data-ttu-id="86fdc-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="86fdc-117">-CustomEmailAddress</span></span>
<span data-ttu-id="86fdc-118">Avisering/avisering skickades till e-post.</span><span class="sxs-lookup"><span data-stu-id="86fdc-118">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="86fdc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86fdc-119">-DefaultProfile</span></span>
<span data-ttu-id="86fdc-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="86fdc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86fdc-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="86fdc-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="86fdc-122">Byt parameter anger att Prenumerationens ägare ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="86fdc-122">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="86fdc-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="86fdc-123">-DisableNotification</span></span>
<span data-ttu-id="86fdc-124">Flagga för att inaktivera all avisering.</span><span class="sxs-lookup"><span data-stu-id="86fdc-124">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="86fdc-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="86fdc-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="86fdc-126">Växla parameter anger aktivera Prenumerationens ägare.</span><span class="sxs-lookup"><span data-stu-id="86fdc-126">Switch paramter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="86fdc-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="86fdc-127">-LocaleID</span></span>
<span data-ttu-id="86fdc-128">E-postspråk för Alert/notifcation till användare (kultur koder som stöds från Microsoft).</span><span class="sxs-lookup"><span data-stu-id="86fdc-128">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="86fdc-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="86fdc-129">-Confirm</span></span>
<span data-ttu-id="86fdc-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="86fdc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86fdc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86fdc-131">-WhatIf</span></span>
<span data-ttu-id="86fdc-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="86fdc-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86fdc-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="86fdc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86fdc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86fdc-134">CommonParameters</span></span>
<span data-ttu-id="86fdc-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86fdc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86fdc-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86fdc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86fdc-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86fdc-137">INPUTS</span></span>

### <span data-ttu-id="86fdc-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="86fdc-138">None</span></span>

## <span data-ttu-id="86fdc-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86fdc-139">OUTPUTS</span></span>

### <span data-ttu-id="86fdc-140">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 0.1.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="86fdc-140">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="86fdc-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86fdc-141">NOTES</span></span>

## <span data-ttu-id="86fdc-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86fdc-142">RELATED LINKS</span></span>
