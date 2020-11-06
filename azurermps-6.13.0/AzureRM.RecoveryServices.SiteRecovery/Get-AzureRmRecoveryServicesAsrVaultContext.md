---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 52535af7a2e7e9282a94c07f62154e42fe807a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583503"
---
# <span data-ttu-id="c7c53-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="c7c53-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="c7c53-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7c53-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c53-103">Hämtar information om inställningar för ASR-valv för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="c7c53-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7c53-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7c53-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7c53-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7c53-105">DESCRIPTION</span></span>
<span data-ttu-id="c7c53-106">Cmdleten **Get-AzureRmRecoveryServicesAsrVaultContext** hämtar information om inställningar för ASR-valv relaterade till Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="c7c53-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="c7c53-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7c53-107">EXAMPLES</span></span>

### <span data-ttu-id="c7c53-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c7c53-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="c7c53-109">Hämtar inställningar för ASR-valv för det aktiva (i PowerShell-sessionen) Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="c7c53-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="c7c53-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7c53-110">PARAMETERS</span></span>

### <span data-ttu-id="c7c53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c53-111">-DefaultProfile</span></span>
<span data-ttu-id="c7c53-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c53-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7c53-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c53-113">CommonParameters</span></span>
<span data-ttu-id="c7c53-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c53-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c53-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7c53-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c53-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7c53-116">INPUTS</span></span>

### <span data-ttu-id="c7c53-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="c7c53-117">None</span></span>

## <span data-ttu-id="c7c53-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7c53-118">OUTPUTS</span></span>

### <span data-ttu-id="c7c53-119">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c7c53-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="c7c53-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7c53-120">NOTES</span></span>

## <span data-ttu-id="c7c53-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7c53-121">RELATED LINKS</span></span>
