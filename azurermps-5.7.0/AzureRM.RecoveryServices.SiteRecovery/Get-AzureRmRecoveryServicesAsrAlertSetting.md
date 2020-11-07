---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: d1da03455fad47d889269c0d961def70df6837e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756477"
---
# <span data-ttu-id="3f8d5-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="3f8d5-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="3f8d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f8d5-102">SYNOPSIS</span></span>
<span data-ttu-id="3f8d5-103">Hämtar de konfigurerade aviserings inställningarna för Azure Site Recovery för valvet.</span><span class="sxs-lookup"><span data-stu-id="3f8d5-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f8d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f8d5-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f8d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f8d5-105">DESCRIPTION</span></span>
<span data-ttu-id="3f8d5-106">Cmdleten **Get-AzureRmRecoveryServicesAsrAlertSetting** hämtar de konfigurerade aviserings inställningarna för Azure Site Recovery för valvet.</span><span class="sxs-lookup"><span data-stu-id="3f8d5-106">The **Get-AzureRmRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="3f8d5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f8d5-107">EXAMPLES</span></span>

### <span data-ttu-id="3f8d5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f8d5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="3f8d5-109">Få aviserings-och aviserings inställningar för Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3f8d5-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="3f8d5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f8d5-110">PARAMETERS</span></span>

### <span data-ttu-id="3f8d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f8d5-111">-DefaultProfile</span></span>
<span data-ttu-id="3f8d5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f8d5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f8d5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f8d5-113">CommonParameters</span></span>
<span data-ttu-id="3f8d5-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f8d5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f8d5-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f8d5-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f8d5-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f8d5-116">INPUTS</span></span>

### <span data-ttu-id="3f8d5-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="3f8d5-117">None</span></span>

## <span data-ttu-id="3f8d5-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f8d5-118">OUTPUTS</span></span>

### <span data-ttu-id="3f8d5-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. commands. RecoveryServices. SiteRecovery, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3f8d5-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3f8d5-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f8d5-120">NOTES</span></span>

## <span data-ttu-id="3f8d5-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f8d5-121">RELATED LINKS</span></span>
