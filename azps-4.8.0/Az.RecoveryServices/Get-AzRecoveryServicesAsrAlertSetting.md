---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100933"
---
# <span data-ttu-id="282bd-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="282bd-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="282bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="282bd-102">SYNOPSIS</span></span>
<span data-ttu-id="282bd-103">Hämtar de konfigurerade aviserings inställningarna för Azure Site Recovery för valvet.</span><span class="sxs-lookup"><span data-stu-id="282bd-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="282bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="282bd-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="282bd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="282bd-105">DESCRIPTION</span></span>
<span data-ttu-id="282bd-106">Cmdleten **Get-AzRecoveryServicesAsrAlertSetting** hämtar de konfigurerade aviserings inställningarna för Azure Site Recovery för valvet.</span><span class="sxs-lookup"><span data-stu-id="282bd-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="282bd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="282bd-107">EXAMPLES</span></span>

### <span data-ttu-id="282bd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="282bd-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="282bd-109">Få aviserings-och aviserings inställningar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="282bd-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="282bd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="282bd-110">PARAMETERS</span></span>

### <span data-ttu-id="282bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="282bd-111">-DefaultProfile</span></span>
<span data-ttu-id="282bd-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="282bd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="282bd-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="282bd-113">CommonParameters</span></span>
<span data-ttu-id="282bd-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="282bd-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="282bd-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="282bd-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="282bd-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="282bd-116">INPUTS</span></span>

### <span data-ttu-id="282bd-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="282bd-117">None</span></span>

## <span data-ttu-id="282bd-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="282bd-118">OUTPUTS</span></span>

### <span data-ttu-id="282bd-119">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="282bd-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="282bd-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="282bd-120">NOTES</span></span>

## <span data-ttu-id="282bd-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="282bd-121">RELATED LINKS</span></span>
