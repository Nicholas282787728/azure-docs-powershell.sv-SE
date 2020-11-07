---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: e7ce712102ffbb74fd8f19eed544642af5a6ebce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747471"
---
# <span data-ttu-id="94ff6-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="94ff6-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="94ff6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="94ff6-103">Hämtar de konfigurerade aviserings inställningarna för Azure Site Recovery för valvet.</span><span class="sxs-lookup"><span data-stu-id="94ff6-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="94ff6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94ff6-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94ff6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94ff6-105">DESCRIPTION</span></span>
<span data-ttu-id="94ff6-106">Cmdleten **Get-AzRecoveryServicesAsrAlertSetting** hämtar de konfigurerade aviserings inställningarna för Azure Site Recovery för valvet.</span><span class="sxs-lookup"><span data-stu-id="94ff6-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="94ff6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94ff6-107">EXAMPLES</span></span>

### <span data-ttu-id="94ff6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="94ff6-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="94ff6-109">Få aviserings-och aviserings inställningar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="94ff6-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="94ff6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94ff6-110">PARAMETERS</span></span>

### <span data-ttu-id="94ff6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ff6-111">-DefaultProfile</span></span>
<span data-ttu-id="94ff6-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94ff6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94ff6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ff6-113">CommonParameters</span></span>
<span data-ttu-id="94ff6-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ff6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ff6-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94ff6-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ff6-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94ff6-116">INPUTS</span></span>

### <span data-ttu-id="94ff6-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="94ff6-117">None</span></span>

## <span data-ttu-id="94ff6-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94ff6-118">OUTPUTS</span></span>

### <span data-ttu-id="94ff6-119">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="94ff6-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="94ff6-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94ff6-120">NOTES</span></span>

## <span data-ttu-id="94ff6-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94ff6-121">RELATED LINKS</span></span>
