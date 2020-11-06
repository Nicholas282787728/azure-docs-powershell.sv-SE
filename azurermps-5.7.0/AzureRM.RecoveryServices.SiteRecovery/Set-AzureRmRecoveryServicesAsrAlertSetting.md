---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 4e51cd90e490442c36b5864e53b4bb7a36e41e80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576458"
---
# <span data-ttu-id="0aa2a-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="0aa2a-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="0aa2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0aa2a-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa2a-103">Konfigurera aviserings inställningar för Azure Site Recovery (e-postmeddelande) för valvet.</span><span class="sxs-lookup"><span data-stu-id="0aa2a-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aa2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0aa2a-104">SYNTAX</span></span>

### <span data-ttu-id="0aa2a-105">Ange (standard)</span><span class="sxs-lookup"><span data-stu-id="0aa2a-105">Set (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa2a-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="0aa2a-106">EmailToSubscriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa2a-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="0aa2a-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa2a-108">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="0aa2a-108">Disable</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aa2a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0aa2a-109">DESCRIPTION</span></span>
<span data-ttu-id="0aa2a-110">Cmdleten **set-AzureRmRecoveryServicesAsrNotificationSetting** konfigurerar meddelande inställningar för Azure Site Recovery (e-postmeddelande) för valvet.</span><span class="sxs-lookup"><span data-stu-id="0aa2a-110">The **Set-AzureRmRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="0aa2a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0aa2a-111">EXAMPLES</span></span>

### <span data-ttu-id="0aa2a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0aa2a-112">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="0aa2a-113">Inaktivera meddelande.</span><span class="sxs-lookup"><span data-stu-id="0aa2a-113">Disable notification.</span></span>

### <span data-ttu-id="0aa2a-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0aa2a-114">Example 2</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="0aa2a-115">Ange meddelande för egna e-postadresser och för abonnemangs ägaren.</span><span class="sxs-lookup"><span data-stu-id="0aa2a-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="0aa2a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0aa2a-116">PARAMETERS</span></span>

### <span data-ttu-id="0aa2a-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0aa2a-117">-Confirm</span></span>
<span data-ttu-id="0aa2a-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0aa2a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa2a-119">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="0aa2a-119">-CustomEmailAddress</span></span>
<span data-ttu-id="0aa2a-120">Avisering/avisering skickades till e-post.</span><span class="sxs-lookup"><span data-stu-id="0aa2a-120">Alert / Notification sent to emails.</span></span>

```yaml
Type: String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa2a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa2a-121">-DefaultProfile</span></span>
<span data-ttu-id="0aa2a-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0aa2a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aa2a-123">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="0aa2a-123">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="0aa2a-124">Byt parameter anger att Prenumerationens ägare ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="0aa2a-124">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa2a-125">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="0aa2a-125">-DisableNotification</span></span>
<span data-ttu-id="0aa2a-126">Flagga för att inaktivera all avisering.</span><span class="sxs-lookup"><span data-stu-id="0aa2a-126">Flag to disable all notification.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa2a-127">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="0aa2a-127">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="0aa2a-128">Växla parameter anger aktivera Prenumerationens ägare.</span><span class="sxs-lookup"><span data-stu-id="0aa2a-128">Switch paramter specifies enable notification to subscription owner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa2a-129">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="0aa2a-129">-LocaleID</span></span>
<span data-ttu-id="0aa2a-130">E-postspråk för Alert/notifcation till användare (kultur koder som stöds från Microsoft).</span><span class="sxs-lookup"><span data-stu-id="0aa2a-130">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa2a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aa2a-131">-WhatIf</span></span>
<span data-ttu-id="0aa2a-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0aa2a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0aa2a-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0aa2a-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa2a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa2a-134">CommonParameters</span></span>
<span data-ttu-id="0aa2a-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aa2a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa2a-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aa2a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa2a-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0aa2a-137">INPUTS</span></span>

### <span data-ttu-id="0aa2a-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="0aa2a-138">None</span></span>

## <span data-ttu-id="0aa2a-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0aa2a-139">OUTPUTS</span></span>

### <span data-ttu-id="0aa2a-140">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 0.1.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0aa2a-140">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0aa2a-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0aa2a-141">NOTES</span></span>

## <span data-ttu-id="0aa2a-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0aa2a-142">RELATED LINKS</span></span>
