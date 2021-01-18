---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521744"
---
# <span data-ttu-id="ca560-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="ca560-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="ca560-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca560-102">SYNOPSIS</span></span>
<span data-ttu-id="ca560-103">Konfigurera aviserings inställningar för Azure Site Recovery (e-postmeddelande) för valvet.</span><span class="sxs-lookup"><span data-stu-id="ca560-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="ca560-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca560-104">SYNTAX</span></span>

### <span data-ttu-id="ca560-105">Ange (standard)</span><span class="sxs-lookup"><span data-stu-id="ca560-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca560-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ca560-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca560-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ca560-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca560-108">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="ca560-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca560-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca560-109">DESCRIPTION</span></span>
<span data-ttu-id="ca560-110">Cmdleten **set-AzRecoveryServicesAsrNotificationSetting** konfigurerar meddelande inställningar för Azure Site Recovery (e-postmeddelande) för valvet.</span><span class="sxs-lookup"><span data-stu-id="ca560-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="ca560-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca560-111">EXAMPLES</span></span>

### <span data-ttu-id="ca560-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ca560-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="ca560-113">Inaktivera meddelande.</span><span class="sxs-lookup"><span data-stu-id="ca560-113">Disable notification.</span></span>

### <span data-ttu-id="ca560-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ca560-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="ca560-115">Ange meddelande för egna e-postadresser och för abonnemangs ägaren.</span><span class="sxs-lookup"><span data-stu-id="ca560-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="ca560-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ca560-116">Example 3</span></span>

<span data-ttu-id="ca560-117">Konfigurera aviserings inställningar för Azure Site Recovery (e-postmeddelande) för valvet.</span><span class="sxs-lookup"><span data-stu-id="ca560-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="ca560-118">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="ca560-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="ca560-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca560-119">PARAMETERS</span></span>

### <span data-ttu-id="ca560-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ca560-120">-CustomEmailAddress</span></span>
<span data-ttu-id="ca560-121">Avisering/avisering skickades till e-post.</span><span class="sxs-lookup"><span data-stu-id="ca560-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="ca560-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca560-122">-DefaultProfile</span></span>
<span data-ttu-id="ca560-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca560-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca560-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ca560-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="ca560-125">Byt parameter anger att Prenumerationens ägare ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="ca560-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="ca560-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="ca560-126">-DisableNotification</span></span>
<span data-ttu-id="ca560-127">Flagga för att inaktivera all avisering.</span><span class="sxs-lookup"><span data-stu-id="ca560-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="ca560-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ca560-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="ca560-129">Byt parameter anger att Prenumerationens ägare ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="ca560-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="ca560-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="ca560-130">-LocaleID</span></span>
<span data-ttu-id="ca560-131">E-postspråk för Alert/Notification till användare (kultur koder som stöds från Microsoft).</span><span class="sxs-lookup"><span data-stu-id="ca560-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="ca560-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ca560-132">-Confirm</span></span>
<span data-ttu-id="ca560-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ca560-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca560-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca560-134">-WhatIf</span></span>
<span data-ttu-id="ca560-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ca560-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca560-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ca560-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca560-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca560-137">CommonParameters</span></span>
<span data-ttu-id="ca560-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca560-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca560-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca560-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca560-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca560-140">INPUTS</span></span>

### <span data-ttu-id="ca560-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="ca560-141">None</span></span>

## <span data-ttu-id="ca560-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca560-142">OUTPUTS</span></span>

### <span data-ttu-id="ca560-143">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="ca560-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="ca560-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca560-144">NOTES</span></span>

## <span data-ttu-id="ca560-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca560-145">RELATED LINKS</span></span>
